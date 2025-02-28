# Common Lisp 面向对象基础

> Lisp 新人有时会惊奇地发现, Common Lisp 还是一门彻底的面向对象语言.<br>
> New Lispers are sometimes surprised to discover what a thoroughly object-oriented language Common Lisp is.
>
> <p align="right">Peter Seibel</p>

使用 Lisp, 你可以不会函数式编程, 可以不会写递归, 当成过程式写是完全没有问题的;<br>
你也未必需要理解一些很复杂的宏, 毕竟那是库的作者才需要考虑的事情;<br>
但是, 你不能不懂 OOP. 无法原生支持 OO 的语言的表达力非常无力. C 的效率往往高于 Lisp, 抛弃 OO 的需求, 更合适的语言是 C.

好 下面开始讲 CLOS (Common Lisp Object System).<br>
Common Lisp 中的面向对象系统 将类的定义分成两部分:

1. 设计一种数据**类型**
2. 定义特化在类之上的**方法**

这样做的好处是, 你可以为已有的类定义新的方法, 从而扩展这个类的行为.<br>
本文要讲的就是第一部分: *如何设计类*.

___

## `DEFCLASS` 宏

先看一个简单的类定义:

```commonlisp
(defclass coffee ()
  ;; ...
  )
```

首先是符号 `coffee`, 这是类的名字. 可以选取任何符号作为类名, 因为类名与其它符号是互不干扰的.

在 `... coffee () ...` 中, 后面的列表将会列出这个类将从哪些类继承, 也即**基类**. 有两点需要注意:

- 基类列表为空, 表示这个类的基类是 `standard-object`.
- 用户不能创建内置类的子类. 只能创建用户自定义类的子类, 或是 `standard-object` 的子类.

后面会讲如何用 `make-instance` 创建类的实例的多种方式.

___

## Slot (槽位)

Slot 相当于 C++ 中的成员变量 或者 Rust 中的字段, 字面意思 —— 槽位. 下面借此来扩充一下 `coffee` 的定义.

```commonlisp
(defclass coffee ()
  (volume
   temperature))
```

它的意思是: 咖啡有体积和温度两个字段. 你可以这样创建一个实例:

`(defvar cup-of-coffee (make-instance 'coffee)) ;`

槽位保存的值可以用 `slot-value` 来访问. 但在此之前, **应当先**给槽位绑定一个值:

1. `(setf (slot-value cup-of-coffee 'temperature) 40)`
2. `(slot-value cup-of-coffee 'temperature) ; ==> 40`

(一个用户自定义类也从所有基类中继承槽位, 这个以后再说)

___

## Initialization (初始化)

```commonlisp
(defclass coffee ()
  ((volume
     :initarg :vol)
   ;; new slot
   cup-size ; small:0~300mL, medium:300~700mL, large:700mL~
   (temperature
     :initform 40
     :initarg  :temp)))

(defparameter cup-of-coffee (make-instance 'coffee
                                           :vol 400))
```

- `initarg`: 引入一个别名 `:vol`, 也就是出现在 `make-instance` 中的关键字. 这个别名仅供 `make-instance` 使用.
- `initform`: 如果调用 `make-instance` 时, 没有提供对应的槽位的值, 那么就求值这个关键字后面的形式作为这个槽位的值 (这里是 $40$).

不过, 仅仅是这样的初始化过程仍然太过简陋. 我们还可以在这个类之上**特化**一个方法, 使它的构造过程就像 C++ 和 Java 中定义的构造函数 或者是 Python 中的 `__init__` 方法一样. 下面是一个模板:

```commonlisp
(defmethod initialize-instance :after ((obj you-defined-class) &key)
  ;; ...
  )
```

(为什么模板长这个样子? 这是 CLOS 中有关 method 的部分, 以后可能会讲)

#### 如何应用这个模板?

没有需求创造需求. 现在 `coffee` 的定义中多了一个槽位 `cup-size`. 我们希望:

1. 创建实例时, 咖啡能够根据自己的容量, 判断自己是 大杯, 中杯, 还是 小(烧)杯.
2. 现在有购买优惠. 额外赠送一定比例 (该值为 `additional-ratio`, 默认是 $0$) 的容量.

```commonlisp
(defmethod initialize-instance :after ((cup-of-coffee coffee) &key (additional-ratio 0))
  (let ((volume (* (slot-value cup-of-coffee 'volume) (1+ additional-ratio))))
    (setf (slot-value cup-of-coffee 'volume) volume) ; set the new value of volume first
    (setf (slot-value cup-of-coffee 'cup-size)
          (cond                                      ; which size?
            ((< volume 300) :small)
            ((< volume 700) :medium)
            (t              :large)))))
```

```commonlisp
(make-instance 'coffee :vol 600
                       :additional-ratio 20/100)
;; ==> volume:720mL, cup-size:large, temperature:40°C
```

___

## Accessor Functions and Macros

### 自动生成的访问函数

可是, 你是一个一个一个 lazy cat, 用 ` slot-value` 和 `(setf slot-value)` 函数来读取和写入槽位的值实在太麻烦了.<br>
这就对了, CLOS 提供了三个参数用来生成某个槽位对应的访问函数:

- `:reader`
- `:writer`
- `:accessor`

当然, 需要额外说明的是: 由 CLOS 自动生成的访问函数 并不会对原本通过 `slot-value` 进行访问的方式有任何限制. Common Lisp 根本没有提供像 C++ 这样的严格的对象封装.<br>
不过, 你还是可以通过管理你的 `package` 选择不将哪些槽位的符号导出, 以增加直接通过 `slot-value` 进行访问的难度.

```commonlisp
(defclass coffee ()
  ((volume
     :initarg  :vol
     :accessor v) ; new
   (cup-size
     :reader size ; new
     :documentation "small:0~300mL, medium:300~700mL, large:700mL~") ; doc-string
   (temperature
     :initform 40
     :initarg  :temp
     :writer   (setf temperature)))) ; new
```

(另外将 `cup-size` 字段的注释改成了**文档字符串**的形式)

现在 看看怎么使用规范的方式来读取和设置槽位:

```commonlisp
(defparameter cup-of-coffee (make-instance 'coffee :vol  450
                                                   :temp 35))
(setf (v cup-of-coffee) (- (v cup-of-coffee) 100)) ; ==> 350mL
(size cup-of-coffee) ; ==> :medium
(incf (temperature cup-of-coffee) 5) ; ==> 40°C
```

### 标准宏 `WITH-SLOTS` 和 `WITH-ACCESSORS`

在某块词法域中频繁的访问槽位时可能需要写出较多的代码.<br>
具体地说, 在 C++ 中, 直接这么写就可以了: `auto& v{cup_of_coffee.v()}; do_this(v), do_that(v);`<br>
而在 CL 中, 却不得不这样: `(do-this (v cup-of-coffee)) (do-that (v cup-of-coffee)) ;` 更麻烦的是, 这种写法很不易读.

有两个标准宏 通过使用 `symbol macro`, 简化了上一段的写法. 但也仅仅是写法, 实际上, **每一次对槽位的访问都需要函数调用**.

```commonlisp
(with-slots (volume
             (size cup-size)) cup-of-coffee
  (format t "~d~%" volume) ; ==> 350
  (format t "~a~%" size))  ; ==> medium
```

唯一要注意的就是: `with-slots` 后接的第一个列表, 其元素

- 要么是一个槽位的名字, 在 `with-slots` 之后所创建的词法域中, 它就用来表示对象的对应槽位;
- 要么是一个二元列表, 后项是槽位的名字, 而指代槽位的责任则由前项承担.

`with-accessors` 的用法与之类似, 将上一段提到的那个列表中的槽位的名字都修改为对应的访问函数的名字即可.<br>
这样, 在 `with-accessors` 的词法域中, 对应的符号将展开成对对应的访问函数的调用, 而非 `slot-value`.

___

## 更多有关 Slots 的事情

### 为类分配的 Slots (而不是为单个实例分配)

类似于 C++ 和 Python 中的静态变量, 或是 Java 中的类字段. 但这种 slots 更加简陋, 因为它只能通过具体的实例去访问.<br>
换言之, 无法像 C++ 那样通过类的名字去访问: `Coffee::some_static_var;`

下面举个简单的例子, 以说明 class-allocated slots 与其它 slots 之间在用法上的差异.<br>
令 `profit-rate` 作为 `coffee` 的利润率. 粗略地讲, 它可以 与咖啡的品种, 杯容量 无关, 但又不是一个常量.

```commonlisp
(defclass coffee ()
  ((...) ...
   (profit-rate
     :allocation :class ; defaults to :instance if not specified
     :initform   30/100
     :initarg    :profit-rate)))
```

- `:initform` 后接的形式 (这里是 $\frac{30}{100}$) 只会求值一次. 创建实例时并不会涉及到它.
- `:initarg` 用法不变, 即, 可以在调用 `make-instance` 时顺便修改分配给类的槽位的值.

想要修改默认的 $\frac{30}{100}$ 的利润率, 你需要先制作出一杯咖啡.<br>
不过, 多数厂商提供了语言标准之外的 MOP (*元对象协议, Meta Object Protocol*), 其中的函数 `class-prototype` 可以返回某个类的实例的引用 而不需要真正地创建一个实例.

### Inheritance (继承)

**一个类不会拥有重名的槽位**.

在继承时, 首先考虑槽位的名字. CLOS 将 一个类自己定义的槽位 和 它的所有的基类们所定义的槽位 的名字取**并集**.<br>
于是, 只需要在遇到同名槽位时, 解决它们的 `:initform, :allocation, ...` 等指示符如何取舍的问题.

这里定义一种奶咖, 作为 `coffee` 的子类:

```commonlisp
(defclass café-au-lait (coffee milk) ; MILK is another user-defined class
  ((temperature
     :allocation :class
     :initform   60
     :initarg    :t)))
```

1. 基类的 `:initarg` 不会被抛弃. 甚至这样写也是可以的: `(make-instance 'café-au-lait :temp 55 :t 50) ;` 这个形式中的 `:temp` 和 `:t` 都指代 *café au lait* 的温度, 只是 `make-instance` 永远只会使用 相对而言**最靠左**的 那个求值结果.
2. `:allocation, :initform` 将由继承体系中 类的位次 (见下文) 唯一决定. *café au lait* 的温度槽位是分配给类的, 这个位置的初始值是 $60$ 而不是 $40$, 因为毫无疑问, 它自己就是这个继承体系中位次最高的类.

___

## Multiple Inheritance (多重继承)

由于 CLOS 保证一个类的槽位的每个名字在这个类中是独一无二的, 所以即使遇到了菱形继承的问题, 也不会有任何概念上的模糊性; 相反, Java 通过禁止多重继承的方式, 来回避这个问题.

有关多重继承, 唯一需要理解的就是继承体系中类的**位次**.<br>
简而言之, 两条规则:

- 子类的位次必然高于它的基类;
- 基类列表中, 左边的类的位次高于它右边的类 (上一个例子中, `coffee` 优先于 `milk`). 

根据这两条规则, 很容易就能证明, 这样的位次**存在且唯一**.<br>
另外, 位次只适用于评估某个类的继承体系中, 相对那个类而言, 它的基类们的优先次序. 所以不存在一种能够描述所有类之间的全序关系的位次.

___

&copy; 2022 小烧杯 \<<one.last.kiss@outlook.com>\>. All rights reserved.
