# Part I

## Chapter I 微积分的概念

### 1 函数与极限

#### 1.1

无穷数列的极限, 记作 $\lim\limits_{n\to\infty}a_n=A$[^1.1.1.1].

函数的极限, 记作 $\lim\limits_{x\to a}f(x)=A$[^1.1.1.2], 这里 $a$ 可以是有限数, 也可以是无穷大.

#### 1.2

一般来说, 函数 $f(x)$ 在 $t=t_0$ 点处连续, 是指 $\lim\limits_{t\to t_0}f(t)=f(t_0)$ 成立, 否则称为间断.

### 2 定积分

#### 2.1

使用将小区间 $\{\Delta x_i\}$ 分成等比数列的方法, 可以计算曲线 $y=x^m$ ($m$ 为任意整数, 但 $m\neq-1$) 与 $x$ 轴之间的面积.  从 $x=a$ 到 $x=b$ 之间的面积是 $\frac{b^{m+1}-a^{m+1}}{m+1}$.

#### 2.3

记 $\int_1^x\frac{1}{s}{\mathrm{d}s}=\ln x$, 存在某个数 $e$ 使得 $\ln e=1$.<br>
可以证明 $\ln{x_1 x_2}=\ln x_1+\ln x_2$[^1.2.3.1], 继续证明可以 (由前式很容易地) 得出 $\ln x$ 是一个以 $e$ 为底的对数函数, 即 $\ln x=\int_1^x\frac{1}{s}{\mathrm{d}s}=\log_e x$.

### 3 微商与微分

#### 3.3

如果极限 $\lim\limits_{\Delta x\to0}\frac{f(x_0+\Delta x)-f(x)}{\Delta x}$ 存在, 我们就说 $f(x)$ 在 $x_0$ 处可微, 并称这极限为 $f(x)$ 在 $x_0$ 处的微商 (或导数), 记为 $f'(x_0)$ 或 $\frac{\mathrm{d}y}{\mathrm{d}x}\big|_{x=x_0}$.

如果函数 $y=f(x)$ 在 $x=x_0$ 处可微, 则一定在这一点连续[^1.3.3.1].

$\lim\limits_{n\to\infty}{(1+\frac{1}{n})^n}=e$[^1.3.3.2].

#### 3.4

函数 $y=f(x)$ 在点 $x$ 的微分, 记作 $\mathrm{d}y=f'(x)\Delta x$.<br>
可以用微分 $\mathrm{d}y$ 近似地代替差分 $\Delta y$[^1.3.4.1].

可以把 $\mathrm{d}y=f'(x)\Delta x$ 改写成 $\mathrm{d}y=f'(x)\mathrm{d}x$[^1.3.4.2],<br>
这就是微商这个名称的由来.

#### 3.5

Fermat 定理[^1.3.5.1]<br>
Rolle 定理[^1.3.5.2]

微分中值定理<br>
    Lagrange 中值定理 (微分中值定理)<br>
    ***Cauchy 中值定理***[^1.3.5.3]

## Chapter II 微积分的运算

### 1 微分法

#### 1.1

若 $y=f(u),u=\varphi (x)$, 则 $\frac{\mathrm{d}y}{\mathrm{d}x}=f'(u)\varphi'(x)$[^2.1.1.1].

若 $x=g(y)$ 是 $y=f(x)$ 的反函数, 且 $f'(x)\neq0$, 则 $g'(y)=\frac{1}{f'(x)}$[^2.1.1.2].

> $(\tan x)'=\sec^2x$<br>
> $(\cot x)'=-\csc^2x$<br>
> $(\sec x)'=\sec x\tan x$<br>
> $(\csc x)'=-\csc x\cot x$<br>
> $(\arcsin x)'=\frac{1}{\sqrt{1-x^2}}$[^2.1.1.3]<br>
> $(\arccos x)'=\frac{-1}{\sqrt{1-x^2}}$<br>
> $(\arctan x)'=\frac{1}{1+x^2}$<br>
> $(\mathrm{arccot}\,x)'=\frac{-1}{1+x^2}$
> 
> *…more*[^2.1.1.4]

一阶微分形式的不变性[^2.1.1.5]

#### 1.2

如果 $f^{(n-1)}(x)$ 的微商存在, 就称它为 $f(x)$ 的 $n$ 阶微商, 记为 $f^{(n)}(x)$ 或 $\frac{\mathrm{d}^nf(x)}{\mathrm{d}x^n}$[^2.1.2.1].

***Leibnitz 公式***[^2.1.2.2]

由参数方程 $\left\{\begin{array}\\x=\varphi(t)\\y=\psi(t)\end{array}\right.$ 所确定的函数的微分法[^2.1.2.3]

### 2 积分法

#### 2.1

> $\int\frac{1}{x^2-a^2}\mathrm{d}x=\frac{1}{2a}\ln|\frac{x-a}{x+a}|$<br>
> $\int\sec x\mathrm{d}x=\ln|\sec x+\tan x|$<br>
> $\int\sqrt{a^2-x^2}\mathrm{d}x=\frac{a^2}{2}\arcsin\frac{x}{a}+\frac{x}{2}\sqrt{a^2-x^2}$<br>
> $\int\sqrt{x^2+a^2}\mathrm{d}x=\frac{x}{2}\sqrt{x^2+a^2}+\frac{a^2}{2}\ln(x+\sqrt{x^2+a^2})$<br>
> $\int\frac{\mathrm{d}x}{\sqrt{x^2\pm1}}=\ln(x+\sqrt{1\pm x^2})$<br>
> $\int\arctan x\mathrm{d}x=x\arctan x-\frac{1}{2}\ln(x^2+1)$<br>
> $\int e^{ax}\cos bx\mathrm{d}x=\frac{b\sin bx+a\cos bx}{a^2+b^2}e^{ax}$<br>
> $\int e^{ax}\sin bx\mathrm{d}x=\frac{a\sin bx-b\cos bx}{a^2+b^2}e^{ax}$<br>
> $J_n=\int\frac{\mathrm{d}x}{(x^2+a^2)^n},J_1=\frac{1}{a}\arctan\frac{x}{a},J_{n+1}=\frac{1}{2na^2}\frac{x}{(x^2+a^2)^n}+\frac{2n-1}{2n}\frac{1}{a^2}J_n$<br>
> $\int_0^{\frac{\pi}{2}}\sin^mx\mathrm{d}x=\int_0^{\frac{\pi}{2}}\cos^mx\mathrm{d}x=\left\{\begin{array}\\\frac{(m-1)!!}{m!!}\frac{\pi}{2}&(\text{even}\,m)\\\frac{(m-1)!!}{m!!}&(\text{odd}\,m)\end{array}\right.$

有理分式的积分 $\int\frac{mx+n}{(x^2+px+q)^k}\mathrm{d}x=\int\frac{mx+n}{((x+\xi)^2+\eta)^k}\mathrm{d}x=a\int\frac{t\mathrm{d}t}{(t^2+\eta)^k}+b\int\frac{\mathrm{d}t}{(t^2+\eta)^k}$, 查表易得.

#### 2.2

- 换元法

    $$
    \int_a^bf(x)\mathrm{d}x=
    \int_{\varphi^{-1}(a)}^{\varphi^{-1}(b)}f[\varphi(t)]\varphi'(t)\mathrm{d}t
    $$

- 分部积分法

## Chapter III 微积分的一些应用

### 2 曲线的描绘

#### 2.5

曲线 $y=f(x)$ 的曲率 $k=\lim\limits_{\Delta s\to0}\frac{\Delta\varphi}{\Delta s}=\frac{|y''|}{(1+y'^2)^{3/2}}$;<br>
参数方程 $\left\{\begin{array}\\x=\varphi(t)\\y=\psi(t)\end{array}\right.$ 的曲率 $k=\frac{|\psi''\varphi'-\psi'\varphi''|}{[\varphi'^2+\psi'^2]^{3/2}}$.

### 3 Taylor 展开与极值问题

#### 3.1

函数 $f(x)$ 在 $x=x_0$ 的泰勒展开式[^3.3.1.1]为

$$
\begin{split}
f(x)=
&f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2\\
&+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n+\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1},
\end{split}
$$

其中 $\xi=x_0+\theta(x-x_0),0<\theta<1$.  (显然, Lagrange 中值定理只是它的一个最简单的特例)

> $e^x=\sum\frac{x^n}{n!}$<br>
> $\sin x\approx x-\frac{x^3}{3!}+\frac{x^5}{5!}-\cdots+(-1)^n\frac{x^{2n+1}}{(2n+1)!}$

***L' Hospital 法则***[^3.3.1.2]

## Chapter IV 常微分方程

### 1 一阶微分方程

#### 1.1

关于 $y$ 的 $n$ 阶线性微分方程的一般形式[^4.1.1.1]

#### 1.2

分离变量法[^4.1.2.1]<br>
形如 $y'=f(\frac{y}{x})$ 的方程经过变换可以变成可分离变量的[^4.1.2.2]

#### 1.3

一阶线性微分方程 $\frac{\mathrm{d}y}{\mathrm{d}x}+P(x)y=Q(x)$ 的解[^4.1.3.1]为

$$
e^{-\int P(x)\mathrm{d}x}\int Q(x)e^{\int P(x)\mathrm{d}x}\mathrm{d}x
$$

这里 $\int P(x)\mathrm{d}x$ 仅表示 $P(x)$ 的一个原函数.

常数变易法[^4.1.3.2]

### 2 二阶微分方程

#### 2.1

可降价的方程 $y''=f(x,y')$[^4.2.1.1] 与 $y''=f(y,y')$[^4.2.1.2]

#### 2.2

二阶线性常微分方程的一般形状是

$$
y''+p(x)y'+q(x)y=f(x)  \quad(2.2.1).
$$

如果 $f(x)\equiv0$, 则方程称为齐次的, 此时方程的初值问题是指

$$
\left\{
\begin{array}\\
y''+p(x)y'+q(x)y=0&(2.2.2)\\
y(x_0)=\alpha,y'(x_0)=\beta
\end{array}
\right.,
$$

它的解是存在且唯一的 (假定已证), 由此可以得到 (2.2.2) 的解的结构定理: 任意解可表成一对线性无关解的线性组合.  下面来证明这条结构定理:

> 如果函数 $\varphi(x),\psi(x)$ 线性相关, 则它们的 Wronski 行列式[^4.2.2.1]
>
> $$
> W(\varphi,\psi)=\left|\begin{array}\\
> \varphi(x)&\psi(x)\\
> \varphi'(x)&\psi'(x)
> \end{array}\right|\equiv0,
> $$
>
> 但必须指出, 由 $W(\varphi,\psi)\equiv0$ 却未必能说这两个函数线性相关[^4.2.2.2]; 如果 $\varphi(x),\psi(x)$ 是齐次线性方程 (2.2.2) 的两个解, 则情况就不同, 即 存在某点 $x_0$ 使 $W(\varphi(x_0),\psi(x_0))=0\Leftrightarrow$ $\varphi(x)$ 与 $\psi(x)$ 线性相关[^4.2.2.3].
>
> 当 $y_1(x),y_2(x)$ 都是 (2.2.2) 的解时, $W(y_1(x),y_2(x))=W(x)$ 有一个很好的性质[^4.2.2.4], 即 Liouville 公式 $W(x)=e^{-\int P(x)\mathrm{d}x}$.  从这里也可以看出, $W(x)$ 在某点为零, 与处处为零是等价的.
>
> ___
>
> 已知 $y_1(x),y_2(x)$ 是线性无关的解, 则存在 $x_0$, 使得 $W(x_0)=\left|\begin{array}\\y_1(x_0)&y_2(x_0)\\y_1'(x_0)&y_2'(x_0)\end{array}\right|\neq0$.
>
> $y(x)$ 是任意一个解, 由 $W(x_0)\neq0$, 一定存在
> 
> $$
> \begin{split}
> C_1y_1(x_0)+C_2y_2(x_0)=y(x_0),\\
> C_1y_2'(x_0)+C_2y_2'(x_0)=y'(x_0).
> \end{split}
> $$
> 
> 由上式知, $y(x)$ 与 $C_1y_1(x)+C_2y_2(x)$ 有相同的初始条件, 根据唯一性定理, 故 $y(x)=C_1y_1(x)+C_2y_2(x)$ 成立.  这就证明了齐次二阶线性常微分方程的解的结构定理.

已知 (2.2.2) 的一个解 $y_1(x)(\not\equiv0)$,<br>
则可借助 Liouville 公式得出另一个与之线性无关的解 $y_2=y_1\cdot\int\frac{1}{y_1^2}e^{-\int P(x)\mathrm{d}x}\mathrm{d}x$[^4.2.2.5].

可以用常数变易法求出非齐次方程 (2.2.1) 的特解[^4.2.2.6]

$$
y^\ast(x)=-y_1\int\frac{y_2f\mathrm{d}x}{W(y_1,y_2)}+y_2\int\frac{y_1f\mathrm{d}x}{W(y_1,y_2)},
$$

与 (2.2.2) 的通解相加, 得出 (2.2.1) 的通解.

#### 2.3

二阶常系数线性微分方程形如

$$
y''+ay'+by=f(x),
$$

求解它的问题归结于求解它相应的齐次方程.  这是容易做到的, 如下:

> 观察发现, $y''+ay'+by=0$ 可能有 $y=e^{\lambda x}$ 形式的解, 回代这个形式, 得出特征方程
>
> $$
> \lambda^2+a\lambda+b=0.
> $$
>
> 1. 若特征方程有两个相异的实根 $\lambda_1,\lambda_2$, 易得 $y=C_1e^{\lambda_1x}+C_2e^{\lambda_2x}$.
> 2. 若方程有重根 $\lambda=-\frac{a}{2}$, 于是 $y_1=e^{-\frac{a}{2}x},y_2=xe^{-\frac{a}{2}x}$[^4.2.3.1], $y=e^{-\frac{a}{2}x}(C_1+C_2x)$.
> 3. 若方程有共轭复根 $\lambda=\alpha\pm\mathrm{i}\beta$, 易得 $y=e^{ax}(C_1\cos\beta x+C_2\sin\beta x)$[^4.2.3.2].

# Part II

## Chapter VI 重积分与偏微商

### 1 重积分

#### 1.1

当点 $P(x,y)$ 在定义域内不论沿着哪一条途径趋向点 $A(a,b)$ 时, $f(x,y)$ 总是趋向于同一个数值 $l$, 则称 $l$ 为函数 $f(x,y)$ 当 $P(x,y)$ 趋于 $A(a,b)$ 时的极限, 记作 $\lim\limits_{x\to a\atop y\to b}f(x,y)=l$, 或 $\lim\limits_{P\to A}f(x,y)=l$.<br>
若 $\lim\limits_{(x,y)\to(a,b)}f(x,y)=f(a,b)$, 则称 $f(x,y)$ 在 $(a,b)$ 处是连续的.

#### 1.2

$f(x,y)$ 是在 $D$ 上的连续函数.  如果 $\varphi(x,y)$ 在 $D$ 上可积, 且不变号, 则在 $D$ 中有一点 $(\xi,\eta)$, 使得 $\iint\limits_{D}f(x,y)\varphi(x,y)\mathrm{d}A=f(\xi,\eta)\iint\limits_{D}\varphi(x,y)\mathrm{d}A$.

#### 1.3

$$
\begin{split}
&\iint\limits_{D}f(x,y)\mathrm{d}A=\int_a^b\left(\int_{\varphi_1(x)}^{\varphi_2(x)}f(x,y)\mathrm{d}y\right)\mathrm{d}x=\int_a^b\mathrm{d}x\int_{\varphi_1(x)}^{\varphi_2(x)}f(x,y)\mathrm{d}y=\iint\limits_{D}f(x,y)\mathrm{d}x\mathrm{d}y.\\
&\iiint\limits_Vf(x,y,z)\mathrm{d}V=\iiint\limits_Vf(x,y,z)\mathrm{d}x\mathrm{d}y\mathrm{d}z\\
&\qquad\qquad\qquad\quad\;\;\,=\iint\limits_D\mathrm{d}x\mathrm{d}y\int_{z_1(x,y)}^{z_2(x,y)}f(x,y,z)\mathrm{d}z=\int_g^h\mathrm{d}z\iint\limits_{D_z}f(x,y,z)\mathrm{d}x\mathrm{d}y.
\end{split}
$$

### 2 偏微商

#### 2.1

定义 $\lim\limits_{\Delta x\to0}\frac{f(x+\Delta x,y)-f(x,y)}{\Delta x}=\frac{\partial f}{\partial x}=f'_x(x,y)$ 为 $f(x,y)$ 对 $x$ 的偏微商, $\frac{\partial f}{\partial x}\mathrm{d}x$ 称为 $f(x,y)$ 对 $x$ 的偏微分.  $f(x,y)$ 在点 $(x,y)$ 的全微分 $\mathrm{d}f=\frac{\partial f}{\partial x}\mathrm{d}x+\frac{\partial f}{\partial y}\mathrm{d}y$.

全微分除了有一些与单变量函数的微分法则在形式上一致的性质[^6.2.1.1], 还有了新的内容.  简单地说, 与 Jacobi 矩阵有关, 并由此可以推出微分的不变性[^6.2.1.2].

二阶偏微商 $\frac{\partial }{\partial y}(\frac{\partial f}{\partial x})$ 记作 $\frac{\partial^2f}{\partial y\partial x}$ 或 $f''_{xy}$.<br>
若 $\frac{\partial^2f}{\partial x\partial y}$ 与 $\frac{\partial^2f}{\partial y\partial x}$ 在点 $(x,y)$ 不但存在而且连续, 则 $\frac{\partial^2f}{\partial x\partial y}=\frac{\partial^2f}{\partial y\partial x}$, 即微商的次序可以交换[^6.2.1.3].

注意, 在 $z=f(x,y),y=y(x)$ 中, $\frac{\partial z}{\partial x}$ 与 $\frac{\partial f}{\partial x}$ 是不同的.

#### 2.2

若 $F(x,y,z)=0$, 将 $z$ 看作 $x,y$ 的函数即 $z=z(x,y)$, 则 $z$ 关于 $x$ 的偏微商 $\frac{\partial z}{\partial x}=-F'_x/F'_z$[^6.2.2.1].<br>
由方程组 $\left\{\begin{array}\\F(x,y,\cdots,u,v)=0\\G(x,y,\cdots,u,v)=0\end{array}\right.$ 确定的以 $u,v$ 为因变量的隐函数, $\frac{\partial u}{\partial x}=-\frac{\partial (F,G)}{\partial (x,v)}/\frac{\partial (F,G)}{\partial (u,v)}$[^6.2.2.2].

### 3 Jacobi 行列式, 面积元素与体积元素

#### 3.1

两个二元函数 $u=u(x,y),v=v(x,y)$ 的四个一阶偏微商组成的矩阵 $\left[\begin{array}\\\frac{\partial u}{\partial x}&\frac{\partial v}{\partial x}\\\frac{\partial u}{\partial y}&\frac{\partial v}{\partial y}\end{array}\right]$ 称为函数 $u$ 和 $v$ 的 Jacobi 矩阵; 其行列式称为 Jacobi 行列式, 记作 $\frac{\partial(u,v)}{\partial(x,y)}$.  多余两个变量的函数也可类似地定义 Jacobi 矩阵.

在多元函数的情形, Jacobi 矩阵相当于单变量函数的微商.  下面列举的一些 Jacobi 行列式的性质可以进一步说明这个问题 (设 $\left\{\begin{array}\\u=u(x,y)\\v=v(x,y)\end{array}\right.,\left\{\begin{array}\\x=x(s,t)\\y=y(s,t)\end{array}\right.$):

> 1. 复合函数的微商法则 $\frac{\partial(u,v)}{\partial(s,t)}=\frac{\partial(u,v)}{\partial(x,y)}\cdot\frac{\partial(x,y)}{\partial(s,t)}$.
> 2. $\frac{\partial(u,v)}{\partial(x,y)}\cdot\frac{\partial(x,y)}{\partial(u,v)}=\frac{\partial(u,v)}{\partial(u,v)}=\left|\begin{array}\\1&0\\0&1\end{array}\right|=1$, 这正好与 $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{1}{\frac{\mathrm{d}x}{\mathrm{d}y}}$ 相当.
> 3. $\frac{\partial(u,v)}{\partial(x,y)}=-\frac{\partial(v,u)}{\partial(x,y)}$.
> 4. $\frac{\partial(u,u)}{\partial(x,y)}=0$.

#### 3.2

设 $\left\{\begin{array}\\x=x(u,v)\\y=y(u,v)\end{array}\right.$, 则曲线坐标 $(u,v)$ 在平面坐标系 $xOy$ 下的面积元素为 $\mathrm{d}A=\left|\frac{\partial(x,y)}{\partial(u,v)}\right|\mathrm{d}u\mathrm{d}v$.  于是由二重积分的定义得到 $\iint\limits_Df(x,y)\mathrm{d}A=\iint\limits_\mathscr{D}f(x(u,v),y(u,v))\left|\frac{\partial(x,y)}{\partial(u,v)}\right|\mathrm{d}u\mathrm{d}v$.

- 极坐标的面素[^6.3.2.1]
- 球坐标 (空间极坐标) 的体素[^6.3.2.2]
- 柱坐标的体素[^6.3.2.3]
- 直角三棱锥的一个可行的变换[^6.3.2.4]

空间曲面 $\vec r=\vec r(u,v)$ 的面积元素 $\mathrm{d}S=\sqrt{EG-F^2}\mathrm{d}u\mathrm{d}v$[^6.3.2.5];<br>
显表示式 $z=z(x,y)$ 的情形则更简单[^6.3.2.6].

## Chapter VII 线, 面积分与外微分形式

### 1 数量场与矢量场

#### 1.1

数量场 $u=u(x,y,z),(x,y,z)\in V$.  在 $V$ 中取一点 $M_0$, 且设 $l$ 是始自 $M_0$ 的射线, 则 $u=u(M)$ 对 $l$ 的方向导数定义为 $(\frac{\partial u}{\partial l})_{M_0}=\lim\limits_{M\to M_0\atop M\in l}\frac{u(M)-u(M_0)}{|MM_0|}$.  $u$ 在 $M_0$ 的梯度 $(\mathbf{grad}\,u)_{M_0}=(\frac{\partial u}{\partial x}\vec i+\frac{\partial u}{\partial y}\vec j+\frac{\partial u}{\partial z}\vec k)_{M_0}$[^7.1.1.1].

运算符号 Nabla 表示为 $\nabla=\vec i\frac{\partial}{\partial x}+\vec j\frac{\partial}{\partial y}+\vec k\frac{\partial}{\partial z}$.  以下用此符号描述一些梯度的性质:

> 1. 方向导数与梯度的关系为: $\frac{\partial u}{\partial l}=\nabla u\cdot\boldsymbol l^0$.
>
> 2. 沿梯度方向, 数量场的变化最快, 等值面分布最 "密".
>
> 3. 梯度运算法则:
> 
>     (i) $\nabla Cu=C\nabla u$;<br>
>     (ii) $\nabla(u+v)=\nabla u+\nabla v$;<br>
>     (iii) $\nabla uv=u\nabla v+v\nabla u$;<br>
>     (iv) $\nabla f(u)=f'(u)\nabla u$.

#### 1.2

设矢量场 $\vec v=P(x,y,z)\vec i+Q(x,y,z)\vec j+R(x,y,z)\vec k$, 它的流线族由微分方程组解得[^7.1.2.1].

### 2 曲线积分

#### 2.1 关于弧长的曲线积分

设曲线 $L$ (弧长为 $s$) 的参数方程为 $\left\{\begin{split}x=x(t)\\y=y(t)\\z=z(t)\end{split}\right.,\alpha\leqslant t\leqslant\beta$ 且 $\dot x,\dot y,\dot z$ 连续, $L$ 无重点.  若 $f(M)=f(x,y,z)$ 在 $L$ 上连续, 则 $f(M)$ 在 $L$ 上的第一种曲线积分存在, 且有

$$
\int_Lf(M)\mathrm{d}s=\int_\alpha^\beta f(x,y,z)\sqrt{\dot x^2+\dot y^2+\dot z^2}\mathrm{d}t.
$$

- 若曲线 $L$ 的直角坐标方程为: $y=y(x),a\leqslant x\leqslant b$, 则<br>
  $\int_Lf(M)\mathrm{d}s=\int_Lf(x,y)\mathrm{d}s=\int_a^bf(x,y(x))\sqrt{1+y'^2}\mathrm{d}x$.
- 若曲线 $L$ 的极坐标方程为: $r=r(\theta),\alpha\leqslant\theta\leqslant\beta$, 则<br>
  $\int_Lf(M)\mathrm{d}s=\int_Lf(x,y)\mathrm{d}s=\int_\alpha^\beta f(r(\theta)\cos\theta,r(\theta)\sin\theta)\sqrt{r^2(\theta)+r'^2(\theta)}\mathrm{d}\theta$.

#### 2.3 关于弧长元素投影的积分

同第一种曲线积分的设定一样定义第二种曲线积分形如 $\int_{L_{AB}}f(M)\mathrm{d}x$ [^7.2.3.1].  以下罗列一些简单性质:

> 1. $\int_{L_{AB}}f(M)\mathrm{d}x=-\int_{L_{BA}}f(M)\mathrm{d}x$ 
> 2. $\int_{L_{AB}}f\mathrm{d}x+\int_{L_{BC}}f\mathrm{d}x=\int_{L_{AC}}f\mathrm{d}x$ 
> 3. 若 $L$ 是 $xOy$ 上平行于 $Oy$ 的直线段, 则 $\int_Lf\mathrm{d}x=0$.  同样, 若 $L$ 是 $Oxyz$ 中在平行于 $yOz$ 的平面上的曲线, 则 $L$ 上关于 $x$ 的第二种曲线积分为零.

#### 2.4

设在 $Oxyz$ 中曲线 $L$ 的参数方程为 $\left\{\begin{split}x=x(t)\\y=y(t)\\z=z(t)\end{split}\right.,\alpha\leqslant t\leqslant\beta$, $\dot x,\dot y,\dot z$ 连续, $A,B$ 的坐标分别为 $A(x(\alpha),y(\alpha),z(\alpha)),B(x(\beta),y(\beta),z(\beta))$.  若 $f(M)=f(x,y,z)$ 为 $L$ 上定义的连续函数, 则 $f(M)$ 在 $L$ 上的第二种曲线积分存在并且

$$
\int_{L_{AB}}f(M)\mathrm{d}x=\int_{L+}f(M)\mathrm{d}x=\int_\alpha^\beta f(x(t),y(t),z(t))\dot x\mathrm{d}x.
$$

同样有关于 $y$ 和 $z$ 的积分公式[^7.2.4.1].

平面封闭曲线的正向 (逆时针方向) 积分采用记号 $\ointctrclockwise$, 与它反向的采用 $\varointclockwise$.

#### 2.5 两种曲线积分的关系

$$
\int_{L+}f(M)\mathrm{d}x=\int_0^{s_0}f(x(s),y(s),z(s))x'(s)\mathrm{d}s=\int_{L+}f(M)\cos\alpha_M\mathrm{d}s.
$$

对于 $y,z$ 同理[^7.2.5.1].

#### 2.6 矢量场的环流量, 矢量的曲线积分

设空间有一 (有限长的) 有向曲线 $L$, 矢量 $\vec v(M)=P(M)\vec i+Q(M)\vec j+R(M)\vec k$ 在 $L$ 上有意义, 定义矢量 $\vec v$ 沿曲线 $L+$ 的曲线积分为

$$
\int_{L+}\vec v\cdot\mathrm{d}\vec r=\int_{L+}(P\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z)=\int_{L+}P\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z.
$$

前者称为矢量的曲线积分, 后者为矢量场的环流量.

### 3 曲面积分

#### 3.1 关于面积元素的曲面积分

设在 $Oxyz$ 中, 有一光滑的用参数表示的曲面 $\Sigma:\left\{\begin{split}x=x(u,v)\\y=y(u,v)\\z=z(u,v)\end{split}\right.,(u,v)\in\Delta$, 此处 $\Delta$ 是直角坐标 $uv$ 平面上的有界闭区域.  若函数 $f(M)=f(x,y,z)$ 在 $\Sigma$ 上连续, 则 $f(M)$ 在 $\Sigma$ 上的第一种曲面积分存在.  面积元素 $\mathrm{d}S=\sqrt{EG-F^2}\mathrm{d}u\mathrm{d}v$, 且

$$
\iint\limits_\Sigma f(M)\mathrm{d}S=\iint\limits_\Delta f(x(u,v),y(u,v),z(u,v))\sqrt{EG-F^2}\mathrm{d}u\mathrm{d}v.
$$

#### 3.2 矢量场的通量, 关于面积元素投影的积分

设在空间区域 $V$ 中有一张曲面 $\Sigma$, 可以分成两面, 一面记为 $A$, 另一面记为 $B$.  在 $\Sigma$ 的每一点 $M$ 作出曲面的单位法矢量 $\vec n=\vec n_M$, 一律指向 $B$ 侧.  设 $\vec v=\vec v(M)=P(M)\vec i+Q(M)\vec j+R(M)\vec k$ 是 $V$ 中一矢量场, 则矢量场 $\vec v$ 由曲面 $\Sigma$ 的 $A$ 侧到 $B$ 侧的通量[^7.3.2.1]为

$$
\begin{split}\\
\iint\limits_\Sigma\vec v\cdot\vec n\mathrm{d}S&=\iint\limits_\Sigma[P(M)\cos\alpha_M+Q(M)\cos\beta_M+R(M)\cos\gamma_M]\mathrm{d}S\\
&=\iint\limits_{\Sigma_B}P\mathrm{d}y\mathrm{d}z+Q\mathrm{d}z\mathrm{d}x+R\mathrm{d}x\mathrm{d}y.
\end{split}
$$

这样, 计算矢量场的通量就是要计算上式中间的三个第一种曲面积分, 但由于出现了方向余弦, 这就使得上式右端三个积分有了几何意义.  并且, 由此还可以建立新的曲面积分的概念——第二种曲面积分的概念.

#### 3.3

设有光滑的参数曲面 $\Sigma:\left\{\begin{split}x=x(u,v)\\y=y(u,v)\\z=z(u,v)\end{split}\right.,(u,v)\in\Delta$.  矢量形式为: $\vec r=\vec r(u,v),(u,v)\in\Delta$, 此处 $\Delta$ 是 $uv$ 平面上的有界闭区域.  若 $f(M)=f(x,y,z)$ 在 $\Sigma$ 上连续, 则 $f(M)$ 在 $\Sigma$ 上的三个第二种曲面积分存在.  若 $P,Q,R$ 是 $\Sigma$ 上的连续函数, 则有[^7.3.3.1]公式

$$
\iint\limits_{\Sigma_B}P\mathrm{d}y\mathrm{d}z+Q\mathrm{d}z\mathrm{d}x+R\mathrm{d}x\mathrm{d}y=\iint\limits_\Delta\pm\left|
\begin{array}\\
P&Q&R\\
x'_u&y'_u&z'_u\\
x'_v&y'_v&z'_v
\end{array}
\right|\mathrm{d}u\mathrm{d}v.
$$

右端取正号或负号视法矢量 $\vec r'_u\times\vec r'_v$ 是否指向 $\Sigma$ 的 $B$ 侧而定.

### 4 Stokes 公式

#### 4.1 Green 公式

设 $D$ 是 $xOy$ 上封闭曲线 $L$ 围成的闭区域, 且函数 $P(x,y)$ 和 $Q(x,y)$ 在 $D$ 上有一阶连续偏微商, 则[^7.4.1.1]

$$
\ointctrclockwise_LP\mathrm{d}x+Q\mathrm{d}y=\iint\limits_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y.
$$

$D$ 的面积为 $\ointctrclockwise_Lx\mathrm{d}y=-\ointctrclockwise_Ly\mathrm{d}x=\frac{1}{2}\ointctrclockwise_Lx\mathrm{d}y-y\mathrm{d}x$.

#### 4.2 Gauss 公式

设 $V$ 是空间封闭曲面 $\Sigma$ 所围成的闭区域, 函数 $P(x,y,z),Q(x,y,z),R(x,y,z)$ 在 $V$ 上有一阶连续偏微商, 则[^7.4.2.1]

$$
\oiint\limits_{\Sigma_\text{外}}P\mathrm{d}y\mathrm{d}z+Q\mathrm{d}z\mathrm{d}x+R\mathrm{d}x\mathrm{d}y=\iiint\limits_V\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V.
$$

$V$ 的体积为 $\oiint\limits_{\Sigma_\text{外}}x\mathrm{d}y\mathrm{d}z=\oiint\limits_{\Sigma_\text{外}}y\mathrm{d}z\mathrm{d}x=\oiint\limits_{\Sigma_\text{外}}z\mathrm{d}x\mathrm{d}y=\frac{1}{3}\oiint\limits_{\Sigma_\text{外}}x\mathrm{d}y\mathrm{d}z+y\mathrm{d}z\mathrm{d}x+z\mathrm{d}x\mathrm{d}y$.

___

设有矢量场 $\vec v$, $M$ 是场中一点.  围绕 $M$ 在场中作一封闭曲面 $\Sigma$, 围成闭区域 $V$, 体积也记作 $V$, $\vec n$ 是 $\Sigma$ 的单位外法矢, 定义矢量场 $\vec v$ 在点 $M$ 的散度为 $(\mathrm{div}\,\vec v)_M=\lim\limits_{\Sigma\to M}\frac{\oiint\limits_\Sigma\vec v\cdot\vec n\mathrm{d}S}{V}=(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z})_M$ [^7.4.2.2].  散度也可用 Nabla 算子写成 $\mathrm{div}\,\vec v=\nabla\cdot\vec v=\vec i\cdot\frac{\partial\vec v}{\partial x}+\vec j\cdot\frac{\partial\vec v}{\partial y}+\vec k\cdot\frac{\partial\vec v}{\partial z}$.  此外容易验证:

> $\nabla\cdot\varphi\vec v=\varphi\nabla\cdot\vec v+\vec v\cdot\nabla\varphi$

___

定义 Laplace 算子 $\Delta=\frac{\partial^2}{\partial x^2}+\frac{\partial^2}{\partial y^2}+\frac{\partial^2}{\partial z^2}=\nabla^2=\nabla\cdot\nabla$, 因此 $\mathrm{div}\,\mathbf{grad}\,u=\Delta u$.

#### 4.3 Stokes 公式

设空间曲面 $\Sigma$, 边界是封闭曲线 $L$.  若函数 $P,Q,R$ 有一阶连续偏微商, 则[^7.4.3.1]

$$
\ointctrclockwise_LP\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z=\iint\limits_{\Sigma+}\left|
\begin{array}\\
\mathrm{d}y\mathrm{d}z&\mathrm{d}z\mathrm{d}x&\mathrm{d}x\mathrm{d}y\\
\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\
P&Q&R
\end{array}\right|=\iint\limits_{\Sigma+}\left|\begin{array}\\
\cos\alpha&\cos\beta&\cos\gamma\\
\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\
P&Q&R\end{array}\right|\mathrm{d}S.
$$

___

矢量场 $\vec v$ 在一点 $M$ 的旋度 ($\mathbf{rot}\,\vec v$) 是一个矢量, 它是这样定义的: 从点 $M$ 作一单位矢量 $\vec n$, 过 $M$ 点又作一平面与 $\vec n$ 垂直, 再在平面上画一封闭曲线 $L$, 若内部面积记为 $A$, 在 $L$ 上各点作单位切矢量 $\vec t$, 使得 $\vec n$ 是在 $\vec t$ 左边, 定义[^7.4.3.2] $(\mathbf{rot}\,\vec v)_M\cdot\vec n=\lim\limits_{L\to M}\frac{\oint_L\vec v\cdot\vec t\mathrm{d}s}{A}$.  若 $\vec v=P\vec i+Q\vec j+R\vec k$, 则 $\mathbf{rot}\,\vec v=\left|\begin{array}\\\vec i&\vec j&\vec k\\\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\P&Q&R\end{array}\right|$ [^7.4.3.3].  旋度也可以用 Nabla 算子写成 $\mathbf{rot}\, \vec v=\nabla\times\vec v=\vec i\times\frac{\partial \vec v}{\partial x}+\vec j\times\frac{\partial \vec v}{\partial y}+\vec k\times\frac{\partial \vec v}{\partial z}$.  此外容易验证:

> 1. $\nabla\times\varphi\vec v=\varphi\nabla\times\vec v+\vec v\times\nabla\varphi$ 
> 2. $\nabla\cdot(\vec u\times\vec v)=\vec v\cdot\nabla\times\vec u-\vec u\cdot\nabla\times\vec v$ 
> 3. $\nabla\times(\vec u\times\vec v)=(\vec v\cdot\nabla)\vec u-(\vec u\cdot\nabla)\vec v+\vec u\nabla\cdot\vec v-\vec v\nabla\cdot\vec u$ 
> 4. $\nabla\times(\nabla\times\vec v)=\nabla(\nabla\cdot\vec v)-\Delta\vec v$ 
> 5. $\nabla\times\nabla\vec u\equiv\vec 0$ 

### 5 全微分与线积分

#### 5.1 与途径无关的曲线积分

在单连通域[^7.5.1.1] $\Sigma$ 内取两点 $A,B$.  假定 $P,Q$ 在 $\Sigma$ 内连续, 且有连续偏微商, 则 $\int_{(A)}^{(B)}P(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y$ 与途径无关的充要条件为 $\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}$.  这一条件被称为**确切微分条件**[^7.5.1.2].<br>
空间的曲线积分的确切微分条件与平面情形类似, 只是用 Stokes 公式代替 Green 公式证明就是了.

例题: 解微分方程 $(x+y+1)\mathrm{d}x+(x-y^2+3)\mathrm{d}y=0$ [^7.5.1.3].

### 6 外微分形式

#### 6.1 外乘积, 外微分形式

回忆面积元素 $\mathrm{d}x\mathrm{d}y=\left|\frac{\partial(x,y)}{\partial(u,v)}\right|\mathrm{d}u\mathrm{d}v$ 通过取绝对值来保持面积元素总是正的.  但是对于已经定向的面积元素, 则没有必要, 即此时 $\mathrm{d}x\mathrm{d}y=\frac{\partial(x,y)}{\partial(u,v)}\mathrm{d}u\mathrm{d}v$.  从这里可以得到:<br>
    (i) 如果取 $y=x$, 则 $\mathrm{d}x\mathrm{d}x=0$.<br>
    (ii) 如果将 $x,y$ 对换, 则 $\mathrm{d}y\mathrm{d}x=-\mathrm{d}x\mathrm{d}y$.<br>
满足上述两条规则的微分乘积称为***微分的外乘积***.<br>
由微分的外乘积乘上函数组成的微分形式称为***外微分形式***, 函数称为微分形式的系数.  有一些性质[^7.6.1.1].

#### 6.2 Poincaré 引理及其逆

- 若 $\omega$ 为一外微分形式, 其微分形式的系数具有二阶连续偏微商, 则 $\mathrm{d}\mathrm{d}\omega=0$.
- 若 $\omega$ 是一个 $p$ 次外微分式且 $\mathrm{d}\omega=0$, 则存在一个 $p-1$ 次外微分形式 $\alpha$, 使 $\mathrm{d}\alpha=\omega$.

#### 6.3

| 外微分形式的次数 | 对应的度[^7.6.3.1] |
| :-----------: | :---------------: |
|  0[^7.6.3.2]  |   梯度[^7.6.3.3]   |
|  1[^7.6.3.4]  |   旋度[^7.6.3.5]   |
|  2[^7.6.3.6]  |   散度[^7.6.3.7]   |

> Poincaré 引理 $\mathrm{d}\mathrm{d}\omega=0$ 有其场论意义.
>
> 当 $\omega$ 为零次外微分形式, 即 $\omega=f$, 则 $\mathrm{d}\mathrm{d}f=0$, 就是<br>
> $\mathbf{rot}\,\mathbf{grad}\,f=\mathbf{0}$.
>
> 当 $\omega$ 为一次外微分形式, 即 $\omega_1=P\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z$, 那么 $\mathrm{d}\mathrm{d}\omega_1=0$, 也就是<br>
> $\mathrm{div}\,\mathbf{rot}\,(P,Q,R)=0$.
>
> ___
>
> Poincaré 引理之逆 $\mathrm{d}\omega=0\Rightarrow\omega=\mathrm{d}\alpha$ 也有其场论意义.
>
> $\vec v$ 为有势场的充要条件是 $\vec v$ 为无旋场, 即<br>
> $\mathbf{rot}\,\vec v=\mathbf{0}\Leftrightarrow\vec v=\mathbf{grad}\,f$.<br>
> 即如果一次微分形式的外微分为零, 则此外微分形式一定是一个函数 (零次外微分形式) 的外微分.
>
> $\vec v$ 为旋度场, 当且仅当 $\vec v$ 为无源场, 即<br>
> $\mathrm{div}\,\vec v=0\Leftrightarrow\vec v=\mathbf{rot}\,\vec b$.<br>
> 即如果二次外微分形式的外微分为零, 则此外微分形式一定是一个一次外微分形式的外微分.

#### 6.4

$$
\int_{\partial\Sigma}\omega=\int_\Sigma\mathrm{d}\omega\,,
$$

这里 $\omega$ 为外微分形式, $\Sigma$ 为 $\mathrm{d}\omega$ 的封闭的积分区域, $\partial\Sigma$ 表示 $\Sigma$ 的边界, $\int$ 表示区域有多少维数就是多少重数.

| 外微分形式的次数  |  空间  |  公式名 |  公式  |
| :------------: | :----: | :----: | :---: |
| 0 | 直线段 | Newton - Leibniz 公式 | $\omega_0=\int\mathrm{d}\omega_0$ |
| 1 | 平面区域 | Green 公式 | $\oint\omega_1=\iint\mathrm{d}\omega_1$ |
| 1 | 空间曲面 | Stokes 公式 | $\oint\omega_1=\iint\mathrm{d}\omega_1$ |
| 2 | 空间中区域 | Gauss 公式 | $\oiint\omega_2=\iiint\mathrm{d}\omega_2$ |

> 最后还要强调的是: 这里所说的 Stokes 公式是微积分的顶峰.  从理论上讲, 这是微积分的终点, 也是微积分从古典走向现代的入口处.  在现代数学中, 微积分的各种定理中, 这条定理也许是用得最多的定理之一.  在数学上, 这是一条少有的简洁, 美丽而深刻的定理.

# Part III

To Be Continued ...

___

&copy; 2022 Shynur \<<one.last.kiss@outlook.com>\>.  All rights reserved.

[^7.6.3.7]: $\mathrm{d}\omega_2=\mathrm{d}A\wedge\mathrm{d}y\wedge\mathrm{d}z+\mathrm{d}B\wedge\mathrm{d}z\wedge\mathrm{d}x+\mathrm{d}C\wedge\mathrm{d}x\wedge\mathrm{d}y=(\frac{\partial A}{\partial x}+\frac{\partial B}{\partial y}+\frac{\partial C}{\partial z})\mathrm{d}x\wedge\mathrm{d}y\wedge\mathrm{d}z\Rightarrow\mathrm{div}\,(A,B,C)=\frac{\partial A}{\partial x}+\frac{\partial B}{\partial y}+\frac{\partial C}{\partial z}$ 

[^7.6.3.5]: $\mathrm{d}\omega_1=\mathrm{d}P\wedge\mathrm{d}x+\mathrm{d}Q\wedge\mathrm{d}y+\mathrm{d}R\wedge\mathrm{d}z=\left|\begin{array}\\\mathrm{d}y\wedge\mathrm{d}z&\mathrm{d}z\wedge\mathrm{d}x&\mathrm{d}x\wedge\mathrm{d}y\\\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\P&Q&R\end{array}\right|\Rightarrow\mathbf{rot}\,(P,Q,R)=\left|\begin{array}\\\vec i&\vec j&\vec k\\\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\P&Q&R\end{array}\right|$ 

[^7.6.3.3]: $\mathrm{d}\omega=\mathrm{d}f=\frac{\partial f}{\partial x}\mathrm{d}x+\frac{\partial f}{\partial y}\mathrm{d}y+\frac{\partial f}{\partial z}\mathrm{d}z\Rightarrow\mathbf{grad}\,f=\frac{\partial f}{\partial x}\vec i+\frac{\partial f}{\partial y}\vec j+\frac{\partial f}{\partial z}\vec k$ 

[^7.6.3.6]: $\omega_2=A\mathrm{d}y\wedge\mathrm{d}z+B\mathrm{d}z\wedge\mathrm{d}x+C\mathrm{d}x\wedge\mathrm{d}y$ 

[^7.6.3.4]: $\omega_1=P\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z$ 

[^7.6.3.2]: $\omega=f$ 

[^7.6.3.1]: 此处仅讨论三维空间

[^7.6.1.1]: 设 $\lambda,\mu,\nu$ 为任意三个外微分形式 (但 $\lambda,\mu$ 分别为 $p,q$ 次外微分形式), 则<br>$\mathrm{d}x\wedge\mathrm{d}y=-\mathrm{d}y\wedge\mathrm{d}x$<br>$(\lambda+\mu)\wedge\nu=\lambda\wedge\nu+\mu\wedge\nu$<br>$\lambda\wedge(\mu+\nu)=\lambda\wedge\mu+\lambda\wedge\nu$<br>$\lambda\wedge(\mu\wedge\nu)=(\lambda\wedge\mu)\wedge\nu$<br>$\mu\wedge\lambda=(-1)^{pq}\lambda\wedge\mu$ 

[^7.5.1.3]: 令 $\left\{\begin{split}&P=x+y+1\\&Q=x-y^2+3\end{split}\right.$, 因为满足确切微分条件, 所以一定有 $u$<br>使得 $\mathrm{d}u=(x+y+1)\mathrm{d}x+(x-y^2+3)\mathrm{d}y$.<br>因此, 一方面 $\mathrm{d}u=0\Rightarrow u=C$, 另一方面考虑选取途径为先 $Ox$ 再 $Oy$ 走向的折线段,<br>则 $u(x,y)=\int_{(0,0)}^{(x,y)}(x+y+1)\mathrm{d}x+(x-y^2+3)\mathrm{d}y=\int_0^x(x+1)\mathrm{d}x+\int_0^y(x-y^2+3)\mathrm{d}y=\frac{x^2}{2}+x+xy-\frac{y^3}{3}+3y$.<br>因此, 方程的解为 $3x^2+6x+6xy-2y^3+18y=C$.

[^7.5.1.1]: 单连通性是不可缺少的,<br>例如 $\Sigma:x^2+y^2>0$, 积分曲线为 $x^2+y^2=1$,<br>则 $\oint\frac{x\mathrm{d}y-y\mathrm{d}x}{x^2+y^2}=\int_0^{2\pi}(\cos^2t+\sin^2t)\mathrm{d}t=2\pi\neq0$.<br>但是却有 $\frac{\partial}{\partial x}\frac{x}{x^2+y^2}=\frac{\partial}{\partial y}\frac{-y}{x^2+y^2}$.

[^7.5.1.2]: 易知原环流量与途径无关的充要条件是在 $\Sigma$ 内部作任一闭合曲线 $l$, 皆有 $\int_lP\mathrm{d}x+Q\mathrm{d}y$.<br>由 Green 公式, 即证对任意域 $D\in\Sigma$ 皆有 $\iint\limits_D(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})\mathrm{d}x\mathrm{d}y=0$.<br>用反证法, 若存在某点使得 $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}>0$, 则由 $P,Q$ 偏微商的连续性, 存在包含该点的域 $\Sigma_0$ 使得 $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}>0$.<br>易得.

[^7.4.3.2]: 旋度 $\mathbf{rot}\,\vec v$ 有时也记成 $\mathbf{curl}\, \vec v$ 

[^7.4.3.3]: 若取 $\vec n=\cos\alpha\vec i+\cos\beta\vec j+\cos\gamma\vec k$, $L$ 的内部为平面区域, 记作 $\Sigma$,<br>则 $(\mathbf{rot}\,\vec v)_M\cdot\vec n=\left|\begin{array}\\\vec i&\vec j&\vec k\\\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\P&Q&R\end{array}\right|_M\cdot\vec n=\left|\begin{array}\\\cos\alpha&\cos\beta&\cos\gamma\\\frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\P&Q&R\end{array}\right|_M$, 右边明显是 Stokes 公式的形式, 易得.

[^7.4.3.1]: 即要证 $\ointctrclockwise_LP\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z=\iint\limits_{\Sigma+}(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z})\mathrm{d}y\mathrm{d}z+(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x})\mathrm{d}z\mathrm{d}x+(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})\mathrm{d}x\mathrm{d}y$.<br>设 $\Sigma:z=z(x,y),(x,y)\in D$, $D$ 是 $xOy$ 上的闭区域, 边界为 $L^*$.<br>设 $\Sigma$ 的边界 $L$ 的参数方程为 $\left\{\begin{split}&x=x(t)\\&y=y(t)\\&z=z(x(t),y(t))\end{split}\right.,\alpha\leqslant t\leqslant\beta$, 故 $L^*$ 的参数方程显然就是 $\left\{\begin{split}x=x(t)\\y=y(t)\end{split}\right.,\alpha\leqslant t\leqslant\beta$.<br>于是 $\ointctrclockwise_LP(x,y,z)\mathrm{d}x+Q(x,y,z)\mathrm{d}y=\ointctrclockwise_{L^*}P(x,y,z(x,y))\mathrm{d}x+Q(x,y,z(x,y))\mathrm{d}y$,<br>又 $\ointctrclockwise_LR\mathrm{d}z=\int_\alpha^\beta R\dot z\mathrm{d}t=\int_\alpha^\beta R(z'_x\dot x+z'_y\dot y)\mathrm{d}t=\ointctrclockwise_{L^*}Rz'_x\mathrm{d}x+Rz'_y\mathrm{d}y$.<br>将以上两式相加, 应用 Green 公式, 得到 $\ointctrclockwise_LP\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z=\ointctrclockwise_{L^*}(P+Rz'_x)\mathrm{d}x+(Q+Rz'_y)\mathrm{d}y=\iint\limits_D[\frac{\partial}{\partial x}(Q+Rz'_y)-\frac{\partial}{\partial y}(P+Rz'_x)]\mathrm{d}x\mathrm{d}y$,<br>即 $\ointctrclockwise_LP\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z=\iint\limits_D[(\frac{\partial Q}{\partial z}-\frac{\partial R}{\partial y})z'_x+(\frac{\partial R}{\partial x}-\frac{\partial P}{\partial z})z'_y+(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})]\mathrm{d}x\mathrm{d}y$.<br>另一方面, 将 $\Sigma:z=z(x,y)$ 视为参数为 $x,y$ 的参数方程, 应用参数曲面的第二种曲面积分的计算公式得到 $\iint\limits_{\Sigma+}(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z})\mathrm{d}y\mathrm{d}z+(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x})\mathrm{d}z\mathrm{d}x+(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})\mathrm{d}x\mathrm{d}y=\iint\limits_D\left|\begin{array}\\\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}&\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}&\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\\x'_x&y'_x&z'_x\\x'_y&y'_y&z'_y\end{array}\right|\mathrm{d}x\mathrm{d}y$,<br>即 $\iint\limits_{\Sigma+}(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z})\mathrm{d}y\mathrm{d}z+(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x})\mathrm{d}z\mathrm{d}x+(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})\mathrm{d}x\mathrm{d}y=\iint\limits_D[(\frac{\partial Q}{\partial z}-\frac{\partial R}{\partial y})z'_x+(\frac{\partial R}{\partial x}-\frac{\partial P}{\partial z})z'_y+(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})]\mathrm{d}x\mathrm{d}y$.<br>得证.

[^7.4.2.2]: 由 Gauss 公式 $\oiint\limits_\Sigma\vec v\cdot\vec n\mathrm{d}S=\oiint\limits_{\Sigma_\text{外}}P\mathrm{d}y\mathrm{d}z+Q\mathrm{d}z\mathrm{d}x+R\mathrm{d}x\mathrm{d}y=\iiint(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z})\mathrm{d}V$,<br>易得.

[^7.4.2.1]: 先假定 $V$ 是由上下两个显表示的曲面, 和周围是其母线平行于 $Oz$ 的柱面所围成的.  $V$ 在 $xOy$ 上的投影为 $D$.  设下面的曲面为 $\Sigma_1:z=z_1(x,y),(x,y)\in D$, 上面的曲面为 $\Sigma_2:z=z_2(x,y),(x,y)\in D$, 周围的柱面为 $\Sigma_3$.<br>于是 $\iiint\limits_V\frac{\partial R}{\partial z}\mathrm{d}x\mathrm{d}y\mathrm{d}z=\iint\limits_D\mathrm{d}x\mathrm{d}y\int_{z_1(x,y)}^{z_2(x,y)}\frac{\partial R}{\partial z}\mathrm{d}z=\iint\limits_D[R(x,y,z_2(x,y))-R(x,y,z_1(x,y))]\mathrm{d}x\mathrm{d}y=\iint\limits_{{\Sigma_2}_\text{上}}R\mathrm{d}x\mathrm{d}y+\iint\limits_{{\Sigma_2}_\text{下}}R\mathrm{d}x\mathrm{d}y$,<br>而 $\iint\limits_{{\Sigma_3}_\text{外}}R\mathrm{d}x\mathrm{d}y=0$, 所以 $\iint\limits_V\frac{\partial R}{\partial z}\mathrm{d}x\mathrm{d}y\mathrm{d}z=\iint\limits_{{\Sigma_2}_\text{上}}R\mathrm{d}x\mathrm{d}y+\iint\limits_{{\Sigma_2}_\text{下}}R\mathrm{d}x\mathrm{d}y+\iint\limits_{{\Sigma_3}_\text{外}}R\mathrm{d}x\mathrm{d}y=\oiint\limits_{\Sigma_\text{外}}R\mathrm{d}x\mathrm{d}y$.<br>同样对于 $\iint\limits_V\frac{\partial P}{\partial x}\mathrm{d}x\mathrm{d}y\mathrm{d}z$ 及 $\iint\limits_V\frac{\partial Q}{\partial y}\mathrm{d}x\mathrm{d}y\mathrm{d}z$ 可得类似结果.

[^7.4.1.1]: 先假定 $L$ 的形状满足这样的要求: 平行于 $Oy$ 的直线至多与 $L$ 交于两点.  设下面曲线的方程为 $y=y_1(x),a\leqslant x\leqslant b$, 上面曲线的方程为 $y=y_2(x),a\leqslant x\leqslant b$.<br>于是 $-\iint\limits_D\frac{\partial P}{\partial y}\mathrm{d}x\mathrm{d}y=-\int_a^b\mathrm{d}x\int_{y_1(x)}^{y_2(x)}\frac{\partial P}{\partial y}\mathrm{d}y=-\int_a^b[P(x,y_2(x))-P(x,y_1(x))]\mathrm{d}x=\ointctrclockwise_LP\mathrm{d}x$.<br>同样可以证明 $\iint\limits_D\frac{\partial Q}{\partial x}\mathrm{d}x\mathrm{d}y=\ointctrclockwise_LQ\mathrm{d}y$.

[^7.3.3.1]: $\vec r'_u\times\vec r'_v$ 是曲面 $\Sigma$ 的法矢量, 且 $\vec n=\pm\frac{\vec r'_u\times\vec r'_v}{|\vec r'_u\times\vec r'_v|}=\pm\frac{1}{|\vec r'_u\times\vec r'_v|}\left|\begin{array}\\\vec i&\vec j&\vec k\\x'_u&y'_u&z'_u\\x'_v&y'_v&z'_v\end{array}\right|$, 易知方向余弦 $\cos\gamma=\pm\frac{\frac{\partial(x,y)}{\partial(u,v)}}{|\vec r'_u\times\vec r'_v|}$.<br>另一方面, $\mathrm{d}S=|\vec r'_u\times\vec r'_v|\mathrm{d}u\mathrm{d}v\Rightarrow P\mathrm{d}x\mathrm{d}y=P\cos\gamma\mathrm{d}S=P\left[\pm\frac{\frac{\partial(x,y)}{\partial(u,v)}}{|\vec r'_u\times\vec r'_v|}\right]|\vec r'_u\times\vec r'_v|\mathrm{d}u\mathrm{d}v=P(\pm\frac{\partial(x,y)}{\partial(u,v)})\mathrm{d}u\mathrm{d}v$.<br>同样可证明其余两式.

[^7.3.2.1]: 或简单叫做在 $\Sigma$ 的 $B$ 侧的通量

[^7.2.5.1]: $\int_{L+}f(M)\mathrm{d}y=\int_0^{s_0}f(x(s),y(s),z(s))y'(s)\mathrm{d}s=\int_{L+}f(M)\cos\beta_M\mathrm{d}s$,<br>$\int_{L+}f(M)\mathrm{d}z=\int_0^{s_0}f(x(s),y(s),z(s))z'(s)\mathrm{d}s=\int_{L+}f(M)\cos\gamma_M\mathrm{d}s$.

[^7.2.4.1]: 习惯上把参数增加时曲线运行的方向叫做参数曲线的正向.

[^7.2.3.1]: 在 $xOy$ 中形如 $\int_{L_{AB}}f(M)\mathrm{d}y=\int_{L_{AB}}f(x,y)\mathrm{d}y$;<br>在 $Oxyz$ 中形如 $\int_{L_{AB}}f(M)\mathrm{d}z=\int_{L_{AB}}f(x,y,z)\mathrm{d}z$.

[^7.1.2.1]: 设流线 $\vec r(t)=x(t)\vec i+y(t)\vec j+z(t)\vec k$,<br>则 $\frac{\mathrm{d}\vec r}{\mathrm{d}t}/\mkern-4mu/\vec v\Rightarrow\frac{\mathrm{d}x}{P}=\frac{\mathrm{d}y}{Q}=\frac{\mathrm{d}z}{R}$.<br>这个微分方程组的存在性与唯一性的证明略.

[^7.1.1.1]: 命 $l$ 的方向余弦为 $(\cos\alpha,\cos\beta,\cos\gamma)$, 则 $l$ 上的 $M$ 可表示为$(x_0+t\cos\alpha,y_0+t\cos\beta,z_0+t\cos\gamma)$.<br>于是 $(\frac{\partial u}{\partial l})_{M_0}=\lim\limits_{t\to0}\frac{u(x_0+t\cos\alpha,y_0+t\cos\beta,z_0+t\cos\gamma)-u(x_0,y_0,z_0)}{t}=\frac{\partial u}{\partial x}\cos\alpha+\frac{\partial u}{\partial y}\cos\beta+\frac{\partial u}{\partial z}\cos\gamma$,<br>则 $(\frac{\partial u}{\partial l})_{M_0}=(\frac{\partial u}{\partial x}\vec i+\frac{\partial u}{\partial y}\vec j+\frac{\partial u}{\partial z}\vec k)_{M_0}\cdot(\cos\alpha,\cos\beta,\cos\gamma)$.

[^6.3.2.6]: $\mathrm{d}S=\sqrt{1+z'^2_x+z'^2_y}\mathrm{d}x\mathrm{d}y$ 

[^6.3.2.5]: 易知 $\mathrm{d}S=|\vec r'_u\times\vec r'_v|\mathrm{d}u\mathrm{d}v$,<br>而 $|\vec r'_u\times\vec r'_v|^2=\vec r'^2_u\vec r'^2_v-(\vec r'_u\cdot\vec r'_v)^2$,<br>故令 $\left\{\begin{split}&E=\vec r'^2_u=x'^2_u+y'^2_u+z'^2_u\\&G=\vec r'^2_v=x'^2_v+y'^2_v+z'^2_v\\&F=\vec r'_u\cdot\vec r'_v=x'_ux'_v+y'_uy'_v+z'_uz'_v\end{split}\right.$.

[^6.3.2.4]: $\left\{\begin{split}x,y,z>0\\x+y+z<a\end{split}\right.$ 确定了坐标面与 $x+y+z=a$ 之间的四面体,<br>引入使得 $\left\{\begin{split}x+y+z=q_1\\a(y+z)=q_1q_2\\a^2z=q_1q_2q_3\end{split}\right.$ 成立的新变量 $\left\{\begin{split}&q_1=x+y+z\\&q_2=\frac{a(y+z)}{x+y+z}\\&q_3=\frac{az}{y+z}\end{split}\right.$,<br>容易算出 $\left\{\begin{split}&x=\frac{q_1(a-q_2)}{a}\\&y=\frac{q_1q_2(a-q_3)}{a^2}\\&z=\frac{q_1q_2q_3}{a^2}\end{split}\right.$ 且 $0<q_1,q_2,q_3<a$ 以及 $\frac{\partial(x,y,z)}{\partial(q_1,q_2,q_3)}=\frac{1}{a^3}q_1^2q_2$.<br>则 $\int_0^a\mathrm{d}x\int_0^{a-x}\mathrm{d}y\int_0^{a-x-y}f(x,y,z)\mathrm{d}z=\frac{1}{a^3}\int_0^aq_1^2\mathrm{d}q_1\int_0^aq_2\mathrm{d}q_2\int_0^af(x(q_1,q_2,q_3),y(q_1,q_2,q_3),z(q_1,q_2,q_3))\mathrm{d}q_3$.

[^6.3.2.3]: $\left\{\begin{split}&x=r\cos\theta\\&y=r\sin\theta\\&z=z\end{split}\right.$ 的体素为 $r\mathrm{d}r\mathrm{d}\theta\mathrm{d}z$ 

[^6.3.2.2]: $\left\{\begin{split}&x=\rho\sin\theta\cos\varphi\\&y=\rho\sin\theta\sin\varphi\\&z=\rho\cos\theta\end{split}\right.$, $\varphi$ 为 $\vec\rho$ 在 $xOy$ 上的投影与 $Ox$ 的夹角, $\theta$ 为 $\vec\rho$ 与 $Oz$ 的夹角.<br>体素由 $\frac{\partial(x,y,z)}{\partial(\rho,\theta,\varphi)}=\rho^2\sin\theta$ 求得.

[^6.3.2.1]: $\rho\mathrm{d}\rho\mathrm{d}\theta$ 

[^6.2.2.2]: $\left\{\begin{array}\\F(x,y,\cdots,u(x,y,\cdots),v(x,y,\cdots))=0\\G(x,y,\cdots,u(x,y,\cdots),v(x,y,\cdots))=0\end{array}\right.\Rightarrow\left\{\begin{array}\\\frac{\partial F}{\partial x}+\frac{\partial F}{\partial u}\frac{\partial u}{\partial x}+\frac{\partial F}{\partial v}\frac{\partial v}{\partial x}=0\\\frac{\partial G}{\partial x}+\frac{\partial G}{\partial u}\frac{\partial u}{\partial x}+\frac{\partial G}{\partial v}\frac{\partial v}{\partial x}=0\end{array}\right.$ 

[^6.2.2.1]: $F(x,y,z(x,y))\equiv0\Rightarrow F'_x+F'_z\frac{\partial z}{\partial x}\equiv0$ 

[^6.2.1.3]: 主要是因为 $\Delta_x\Delta_yf=\Delta_y\Delta_xf$.

[^6.2.1.2]: 如果 $x,y$ 是 $u,v$ 的函数, 则<br>$\frac{\partial f}{\partial u}=\frac{\partial f}{\partial x}\frac{\partial x}{\partial u}+\frac{\partial f}{\partial y}\frac{\partial y}{\partial u}$,<br>$\frac{\partial f}{\partial v}=\frac{\partial f}{\partial x}\frac{\partial x}{\partial v}+\frac{\partial f}{\partial y}\frac{\partial y}{\partial v}$.<br>计算出对 $u,v$ 的全微分 $\mathrm{d}x$ 与 $\mathrm{d}y$,<br>立刻推出 $\mathrm{d}f=\frac{\partial f}{\partial u}\mathrm{d}u+\frac{\partial f}{\partial v}\mathrm{d}v=\frac{\partial f}{\partial x}\mathrm{d}x+\frac{\partial f}{\partial y}\mathrm{d}y$.

[^6.2.1.1]: $\mathrm{d}(u\pm v)=\mathrm{d}u\pm\mathrm{d}v$,<br>$\mathrm{d}(uv)=u\mathrm{d}v+v\mathrm{d}u$,<br>$\mathrm{d}(\frac{u}{v})=\frac{v\mathrm{d}u-u\mathrm{d}v}{v^2}$.

[^4.2.3.2]: 由 $\lambda$ 得出复值解 $\tilde{y}(x)=e^{(\alpha\pm\mathrm{i}\beta)x}$, 则应用 Euler 公式即可.<br>$y_1=\frac{1}{2}(e^{(\alpha+\mathrm{i}\beta)x}+e^{(\alpha-\mathrm{i}\beta)x})=e^{ax}\cos\beta x,$<br>$y_2=\frac{1}{2\mathrm{i}}(e^{(\alpha+\mathrm{i}\beta)x}-e^{(\alpha-\mathrm{i}\beta)x})=e^{ax}\sin\beta x.$ 

[^4.2.3.1]: 前面说过, 已知齐次二阶线性常微分方程的一个非平凡解时, 可以算出另一个线性无关的解.<br>故 $y_2(x)=e^{-\frac{a}{2}x}\int{e^{ax}\cdot e^{-\int a\mathrm{d}x}\mathrm{d}x}$.

[^4.2.2.6]: 假设有形如 $y^\ast=C_1(x)y_1(x)+C_2(x)y_2(x)$ 的特解.<br>于是 $\frac{\mathrm{d}y^\ast}{\mathrm{d}x}=C_1y_1'+C_2y_2'+[C_1'y_1+C_2'y_2]$, 不妨命 $C_1'y_1+C_2'y_2=0$.<br>于是 $\frac{\mathrm{d}^2y^\ast}{\mathrm{d}x^2}=C_1y_1''+C_2y_2''+[C_1'y_1'+C_2'y_2']$, 代入 $y''+py'+qy=f$,<br>得到 $C_1[y_1''+py_1'+qy_1]+C_2[y_2''+py_2'+qy_2]+[C_1'y_1'+C_2'y_2']=f$.<br>由于 $y_1,y_2$ 是齐次方程的解, 所以 $C_1'y_1'+C_2'y_2'=f$.<br>将前式与 $C_1'y_1+C_2'y_2=0$ 联立, 由 $W(y_1,y_2)\neq0$ 可知有解,<br>解方程得 $\left\{\begin{array}\\C_1'(x)=\frac{-y_2(x)f(x)}{y_1(x)y_2'(x)-y_1'(x)y_2(x)}\\C_2'(x)=\frac{y_1(x)f(x)}{y_1(x)y_2'(x)-y_1'(x)y_2(x)}\end{array}\right.$.  积分之即可.

[^4.2.2.5]: $W(y_1,y_2)=e^{-\int P\mathrm{d}x}$ 的两边同除以 $y_1^2$,<br>得 $\frac{y_1y_2'-y_1'y_2}{y_1^2}=\frac{1}{y_1^2}e^{-\int P\mathrm{d}x}=\frac{\mathrm{d}}{\mathrm{d}x}(\frac{y_2}{y_1})$,<br>积分之, 得 $\frac{y_2}{y_1}=\int\frac{1}{y_1^2}e^{-\int P\mathrm{d}x}\mathrm{d}x$ 

[^4.2.2.4]: $\frac{\mathrm{d}W}{\mathrm{d}x}=\frac{\mathrm{d}}{\mathrm{d}x}(y_1y_2'-y_1'y_2)=y_1y_2''-y_1''y_2$,<br>但 $y_1''=-p(x)y_1'-q(x)y_1,y_2''=-p(x)y_2'-q(x)y_2$,<br>所以 $\frac{\mathrm{d}W}{\mathrm{d}x}=y_1(-py_2'-qy_2)-y_2(-py_1'-qy_1)=-pW$.

[^4.2.2.3]: $W(\varphi(x_0),\psi(x_0))=0\Rightarrow\left\{\begin{array}\\C_1\varphi(x_0)+C_2\psi(x_0)=0\\C_1\varphi'(x_0)+C_2\psi'(x_0)=0\end{array}\right..$<br>考虑函数 $y(x)=C_1\varphi(x)+C_2\psi(x)$, 它也是齐次方程的解, 且符合初始条件 $y(x_0)=0,y'(x_0)=0$;<br>另一方面, $\tilde{y}(x)\equiv0$ 当然是齐次方程的解, 和 $y(x)$ 满足同样的初始条件.<br>由解的存在唯一性定理推知 $y(x)\equiv\tilde{y}(x)\equiv0$, 这就证明了 $\varphi(x),\psi(x)$ 线性相关.

[^4.2.2.1]: 线性相关意即, 要存在两个不同时为零的常数 $C_1,C_2$,<br>使得 $C_1\varphi(x)+C_2\psi(x)\equiv0$,<br>顺便有 $C_1\varphi'(x)+C_2\psi'(x)\equiv0$,<br>当且仅当 $\left|\begin{array}\\\varphi(x)&\psi(x)\\\varphi'(x)&\psi'(x)\end{array}\right|=0$.

[^4.2.2.2]: 例如<br>$\varphi(x)=\left\{\begin{array}\\-x&x\leqslant0\\0&x\geqslant0\end{array}\right.,$<br>$\psi(x)=\left\{\begin{array}\\0&x\leqslant0\\x&x\geqslant0\end{array}\right..$ 

[^4.2.1.2]: $p=y'\Rightarrow\frac{\mathrm{d}^2y}{\mathrm{d}x^2}=\frac{\mathrm{d}p}{\mathrm{d}x}=\frac{\mathrm{d}p}{\mathrm{d}y}\cdot\frac{\mathrm{d}y}{\mathrm{d}x}=p\frac{\mathrm{d}p}{\mathrm{d}y}$ 可将方程化为 $\frac{\mathrm{d}p}{\mathrm{d}y}=\varphi(y,p)$ 的形式

[^4.2.1.1]: 令 $p=y'$ 即可

[^4.1.3.2]: $\frac{\mathrm{d}y}{\mathrm{d}x}+P(x)y=0\Rightarrow y=Ce^{-\int P(x)\mathrm{d}x}$, 这里 $\int P(x)\mathrm{d}x$ 仅表示 $P(x)$ 的一个原函数.<br>将常数 $C$ 变易为 $x$ 的函数 $C(x)$, 然后将 $C(x)e^{-\int P(x)\mathrm{d}x}$ 代入 $\frac{\mathrm{d}y}{\mathrm{d}x}+P(x)y=Q(x)$,<br>就得到一个 $C(x)$ 的微分方程 $C'(x)=Q(x)e^{\int P(x)\mathrm{d}x}$, $C(x)=\int Q(x)e^{\int P(x)\mathrm{d}x}\mathrm{d}x$ 就是它的解.<br>回代即可.

[^4.1.3.1]: 考虑方程 (1) $\mathrm{d}(\psi(x)y)=f(x)\mathrm{d}x$,<br>将上式两边积分, 得 $\psi(x)y=\int f(x)\mathrm{d}x\Rightarrow y=\frac{1}{\psi(x)}\int f(x)\mathrm{d}x$,<br>原方程 (1) 就是 $\psi(x)\frac{\mathrm{d}y}{\mathrm{d}x}+\psi'(x)y=f(x)$,<br>方程 (1) 还可以写成 $\frac{\mathrm{d}y}{\mathrm{d}x}+P(x)y=Q(x)$ 的形式, 此处 $P(x)=\frac{\psi'(x)}{\psi(x)},Q(x)=\frac{f(x)}{\psi(x)}$.<br>显然 $\psi(x)$ 可以轻松解出, 进而算出 $f(x)$, 代入方程 (1) 的解即可.

[^4.1.2.2]: 令 $y=xu$ 引入新变量,<br>代回 $y'=f(\frac{y}{x})$ 得到 $u+xu'=f(u)$,<br>用分离变量的方法解得 $x=e^{\int\frac{\mathrm{d}u}{f(u)-u}}$.

[^4.1.2.1]: $g(y)\mathrm{d}y=f(x)\mathrm{d}x\Rightarrow\int g(y)\mathrm{d}y=\int f(x)\mathrm{d}x$ 

[^4.1.1.1]: $a_0(x)\frac{\mathrm{d}^ny}{\mathrm{d}x^n}+a_1(x)\frac{\mathrm{d}^{n-1}y}{\mathrm{d}x^{n-1}}+\cdots+a_n(x)y=f(x)$ 

[^3.3.1.2]: 若 $f(x),g(x)$ 在 $x=x_0$ 处有二阶微商, $g'(x_0)\neq0$, 且 $\lim\limits_{x\to x_0}f(x)=0,\lim\limits_{x\to x_0}g(x)=0$,<br>则 $\lim\limits_{x\to x_0}\frac{f(x)}{g(x)}=\lim\limits_{x\to x_0}\frac{f'(x_0)(x-x_0)+O[(x-x_0)^2]}{g'(x_0)(x-x_0)+O[(x-x_0)^2]}=\lim\limits_{x\to x_0}\frac{f'(x_0)+O(x-x_0)}{g'(x_0)+O(x-x_0)}=\lim\limits_{x\to x_0}\frac{f'(x_0)}{g'(x_0)}$.<br>当然还可以有: 若 $f(x),g(x)$ 在 $x=x_0$ 处有 $n$ 阶微商, 且<br>$\lim\limits_{x\to x_0}f(x)=\lim\limits_{x\to x_0}f'(x)=\cdots=\lim\limits_{x\to x_0}f^{(n-1)}(x)=0,$<br>$\lim\limits_{x\to x_0}g(x)=\lim\limits_{x\to x_0}g'(x)=\cdots=\lim\limits_{x\to x_0}g^{(n-1)}(x)=0$,<br>则 $\lim\limits_{x\to x_0}\frac{f(x)}{g(x)}=\frac{f^{(n)}(x_0)}{g^{(n)}(x_0)}$.

[^3.3.1.1]: 令 $P_n(x)=f(0)+f'(0)x+\frac{f''(0)}{2!}x^2+\cdots+\frac{f^{(n)}(0)}{n!}x^n$,<br>记 $f(x)-P_n(x)=\frac{x^{n+1}}{(n+1)!}Q_n$,<br>作 $z$ 的函数 $\phi(z)=f(x)-[f(z)+(x-z)f'(z)+\frac{(x-z)^2}{2!}f''(z)+\cdots+\frac{(x-z)^n}{n!}f^{(n)}(z)+\frac{(x-z)^{n+1}}{(n+1)!}Q_n]$,<br>则显然有 $\phi(0)=\phi(x)=0$.  由微分中值定理, 一定有点 $\xi=\theta x,0<\theta<1$, 使 $\phi'(\xi)=0$,<br>但 $\phi'(z)=\frac{(x-z)^n}{n!}[Q_n-f^{(n+1)}(z)]$, 故 $Q_n=f^{(n+1)}(\xi)$.<br>$Q_n$ 称为泰勒展开式的余项, 所以 $f(x)-P_n=O(x^{n+1})$.

[^2.1.2.3]: $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\mathrm{d}y}{\mathrm{d}t}\frac{\mathrm{d}t}{\mathrm{d}x}=\psi'(t)\frac{1}{\varphi'(t)}=\frac{\psi'(t)}{\varphi'(t)}$,<br>$\frac{\mathrm{d}^2y}{\mathrm{d}x^2}=\frac{\mathrm{d}}{\mathrm{d}x}(\frac{\psi'(t)}{\varphi'(t)})=\frac{\mathrm{d}}{\mathrm{d}t}(\frac{\psi'(t)}{\varphi'(t)})\frac{\mathrm{d}t}{\mathrm{d}x}=\frac{\psi''(t)\varphi'(t)-\psi'(t)\varphi''(t)}{[\varphi'(t)]^2}\frac{1}{\varphi'(t)}=\frac{\psi''\varphi'-\psi'\varphi''}{\varphi'^3}$.

[^2.1.2.2]: $(uv)^{(n)}=\sum_{r=0}^n{\mathrm{C}_n^ru^{(n-r)}v^{(r)}}$ 

[^2.1.2.1]: 以二阶微分为例, 命 $y=f(x)$, 则 $\mathrm{d}y=f'(x)\mathrm{d}x$,<br>则有 $\mathrm{d}^2y=\mathrm{d}(\mathrm{d}y)=\mathrm{d}[f'(x)\mathrm{d}x]=f''(x)\mathrm{d}x^2$.

[^2.1.1.5]: 设 $y=f(x),x=\varphi(t)$ 都是可微函数,<br>而已知复合函数 $y=f[\varphi(t)]$ 的微商为 $y'=f'(x)\varphi'(t)$,<br>因此 $\mathrm{d}y=f'(x)\varphi'(t)\mathrm{d}t$,<br>但 $\mathrm{d}x=\varphi'(t)\mathrm{d}t$,<br>故得 $\mathrm{d}y=f'(x)\mathrm{d}x$.<br>这就是说, 不论 $x$ 是自变量或中间变量, $f(x)$ 的微分形式 $\mathrm{d}y=f'(x)\mathrm{d}x$ 总是不变的.

[^2.1.1.4]: $(u^v)'=u^v[v'\ln u+v\frac{u'}{u}]$<br>$(\ln (1+x))^{(n)}=(-1)^{n-1}\frac{(n-1)!}{(1+x)^n}$<br>$(\sin x)^{(n)}=\sin (x+\frac{n\pi}{2})$<br>$(\cos x)^{(n)}=\cos (x+\frac{n\pi}{2})$ 

[^2.1.1.3]: $(\arcsin x)'=\frac{1}{(\sin y)'}=\frac{1}{\cos y}=\frac{1}{\sqrt{1-\sin^2y}}=\frac{1}{\sqrt{1-x^2}}$.

[^2.1.1.2]: 由于 $y=f(g(y))$, 立刻有 $1=f'(x)g'(y)$.

[^2.1.1.1]: 由于 $\frac{\Delta y}{\Delta x}=\frac{\Delta y}{\Delta u}\cdot\frac{\Delta u}{\Delta x}$,<br>令 $\Delta x\to0$, 注意这时也有 $\Delta u\to0$, 于是得<br>$y'=\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta x}=\lim\limits_{\Delta x\to0}(\frac{\Delta y}{\Delta u}\cdot\frac{\Delta u}{\Delta x})=\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta u}\cdot\lim\limits_{\Delta x\to0}\frac{\Delta u}{\Delta x}=\lim\limits_{\Delta u\to0}\frac{\Delta y}{\Delta u}\cdot\lim\limits_{\Delta x\to0}\frac{\Delta u}{\Delta x}=\frac{\mathrm{d}y}{\mathrm{d}u}\cdot\frac{\mathrm{d}u}{\mathrm{d}x}$.

[^1.3.5.3]: 设函数 $f(x)$ 和 $g(x)$ 都是 $[a,b]$ 上的连续函数, 且在 $(a,b)$ 上可微, 且 $\forall x\in(a,b),g'(x)\neq0$, 则必有 $\xi\in(a,b)$, 使得 $\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f'(\xi)}{g'(\xi)}$.

[^1.3.5.2]: 若 $f(x)$ 在 $[a,b]$ 上连续, 在 $(a,b)$ 上可微, 且 $f(a)=f(b)$, 则至少存在一点 $\xi\in(a,b)$, 使得 $f'(\xi)=0$.

[^1.3.5.1]: 如果 $f(x)$ 在 $x_0$ 点可微, 且在该点取到极值, 那么必有 $f'(x_0)=0$.

[^1.2.3.1]: $\ln x_1+\ln x_2=\int_1^{x_1}\frac{1}{s}{\mathrm{d}s}+\int_1^{x_2}\frac{1}{s}{\mathrm{d}s}=\int_1^{x_1}\frac{1}{s}{\mathrm{d}s}+\int_{x_1}^{x_1 x_2}\frac{1}{\frac{s}{x_1}}{\mathrm{d}{\frac{s}{x_1}}}=\int_1^{x_1}\frac{1}{s}{\mathrm{d}s}+\int_{x_1}^{x_1 x_2}\frac{1}{s}{\mathrm{d}s}=\int_1^{x_1 x_2}\frac{1}{s}{\mathrm{d}s}=\ln {x_1 x_2}$ 

[^1.3.3.1]: $f(x+\Delta x)-f(x)=\frac{f(x+\Delta x)-f(x)}{\Delta x}\cdot \Delta x$,<br>令 $\Delta x\to0$, 两边取极限, 由于 $\lim\limits_{\Delta x\to0}\frac{f(x_0+\Delta x)-f(x)}{\Delta x}$ 存在, 所有等式的右边显然趋于零, 故$\lim\limits_{\Delta x\to0}[f(x+\Delta x)-f(x)]=0$,<br>即 $f(x)$ 在 $x_0$ 处连续.

[^1.1.1.1]: 如果 $\lim\limits_{n\to\infty}b_n = B$, 那么<br>	$\lim\limits_{n\to\infty}(a_n\pm b_n)=A\pm B$,<br>	$\lim\limits_{n\to\infty}(a_n\cdot b_n)=AB$,<br>	$\lim\limits_{n\to\infty}\frac{a_n}{b_n}=\frac{A}{B}$  $(B\neq0)$.<br>如果 $k$ 为常数, 那么<br>	$\lim\limits_{n\to\infty}{k\cdot a_n}=kA$.<br>再如果有 $\lim\limits_{n\to\infty}c_n=C$, 且 $a_n\leqslant b_n\leqslant c_n$, 则<br>	$A\leqslant B\leqslant C$.

[^1.1.1.2]: 如果 $\lim\limits_{x\to a}g(x)$ 也存在且有限, 则有<br>	$\lim\limits_{x\to a}(f(x)\pm g(x))=\lim\limits_{x\to a}{f(x)}\pm\lim\limits_{x\to a}g(x)$,<br>	$\lim\limits_{x\to a}(f(x)\cdot g(x))=\lim\limits_{x\to a}{f(x)}\cdot\lim\limits_{x\to a}g(x)$,<br>	$\lim\limits_{x\to a}\frac{f(x)}{g(x)}=\lim\limits_{x\to a}{f(x)}/\lim\limits_{x\to a}g(x)$  $(\lim\limits_{x\to a}g(x)\neq0)$.<br>此外, 如在点 $a$ 的附近成立不等式 $f(x)\leqslant g(x)\leqslant h(x)$ 且 $\lim\limits_{x\to a}f(x)=\lim\limits_{x\to a}h(x)=A$, 则<br/>	$\lim\limits_{x\to a}g(x)=A$.

[^1.3.3.2]: 由微商的定义, $\frac{1}{x}=\frac{\mathrm{d}{\ln x}}{\mathrm{d}x}=\frac{\mathrm{d}{\log_e x}}{\mathrm{d}x}=\lim\limits_{\Delta x\to0}\frac{\log_e(x_0+\Delta x)-\log_e x}{\Delta x}=\lim\limits_{\Delta x\to0}{\log_e{(1+\frac{\Delta x}{x})^\frac{1}{\Delta x}}}$,<br>特别取 $x=1,\Delta x=\frac{1}{n}$, 因此, $\lim\limits_{n\to\infty}{\log_e{(1+\frac{1}{n})^n}}=1$, 易得

[^1.3.4.1]: 一般来说, 当 $y=f(x)$ 比较复杂时, $\Delta y$ 不易计算,<br>然而由微商的定义知道 $\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{f(x_0+\Delta x)-f(x)}{\Delta x}=f'(x_0)$.<br>若令 $\frac{\Delta y}{\Delta x}-f'(x)=\alpha$, 则显然有 $\lim\limits_{\Delta x\to0}\alpha=0$,<br>也就是说 $\Delta y=f'(x)\Delta x+\alpha \Delta x=\mathrm{d}y+\alpha \Delta x$ 中的 $\alpha\Delta x$ 可以忽略不计.

[^1.3.4.2]: 特别取函数 $y=x$, 则 $f'(x)=x'=1$.<br>因此, 函数 $y=x$ 的微分 $\mathrm{d}x=1\cdot\Delta x=\Delta x$.  易得
