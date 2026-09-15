# 考研数学二 · 公式手册

> **适用**：2027 考研数学二（高等数学 ≈80% ＋ 线性代数 ≈20%，**不考概率论与数理统计**）
> **用法**：按目录查公式 → 回对应章节笔记看推导 → 考前两周只刷本页
> **原则**：只收公式、条件与常用结论，不写推导和例题（推导见 `../高等数学/` 等章节笔记）
> **免责**：本手册按数二大纲范围整理，边缘考点已单独标注；最终以当年度教育部教育考试院《数学考试大纲》原文为准

---

## 目录

- [〇、数二范围边界（先看这个）](#〇数二范围边界先看这个)
- [一、函数、极限与连续](#一函数极限与连续)
- [二、一元函数微分学](#二一元函数微分学)
- [三、不定积分](#三不定积分)
- [四、定积分及其应用](#四定积分及其应用)
- [五、多元函数微分学](#五多元函数微分学)
- [六、二重积分](#六二重积分)
- [七、常微分方程](#七常微分方程)
- [八、线性代数](#八线性代数)
- [九、高频易错速查](#九高频易错速查)

---

## 〇、数二范围边界（先看这个）

| 模块 | 数二 | 备注 |
| --- | --- | --- |
| 函数、极限、连续 | ✅ | 等价无穷小、泰勒展开是高频入口 |
| 一元函数微分学 | ✅ | 中值定理证明题必考 |
| 一元函数积分学 | ✅ | 含反常积分 |
| 多元函数微分学 | ✅ | 偏导、全微分、复合与隐函数求导、极值 |
| 二重积分 | ✅ | 直角坐标、极坐标、对称性 |
| 常微分方程 | ✅ | 一阶 ＋ 可降阶 ＋ 二阶常系数 |
| 线性代数（六章） | ✅ | 与数一、数三基本一致，深度不降低 |
| 概率论与数理统计 | ❌ | 数二完全不考 |
| 无穷级数（含幂级数、傅里叶级数） | ❌ | 不用复习 |
| 向量代数与空间解析几何 | ❌ | 不用复习 |
| 三重积分、曲线积分、曲面积分 | ❌ | 但**二重积分要考** |
| 方向导数、梯度、场论 | ❌ | 数一内容 |
| 曲率、伯努利方程、欧拉方程 | ⚠️ | 大纲表述各年略有差异，作拓展了解即可 |

> **试卷结构**：单选 10×5＝50 分，填空 6×5＝30 分，解答 6 题共 70 分，满分 150 分，180 分钟。

---

## 一、函数、极限与连续

### 1.1 常用等价无穷小（$x \to 0$）

$$x \sim \sin x \sim \tan x \sim \arcsin x \sim \arctan x \sim \ln(1+x) \sim e^{x}-1$$

$$1-\cos x \sim \frac{x^{2}}{2}, \qquad (1+x)^{\alpha}-1 \sim \alpha x, \qquad a^{x}-1 \sim x\ln a$$

$$\sqrt[n]{1+x}-1 \sim \frac{x}{n}, \qquad x - \ln(1+x) \sim \frac{x^{2}}{2}, \qquad x - \sin x \sim \frac{x^{3}}{6}$$

$$\tan x - x \sim \frac{x^{3}}{3}, \qquad \arcsin x - x \sim \frac{x^{3}}{6}, \qquad \tan x - \sin x \sim \frac{x^{3}}{2}$$

> **使用条件**：只在乘除结构中可直接替换；加减结构中替换需保证不丢失主部（等价无穷小相减可能丢阶，此时改用泰勒展开）。

### 1.2 两个重要极限与 $1^{\infty}$ 型

$$\lim_{x\to 0}\frac{\sin x}{x}=1, \qquad \lim_{x\to\infty}\left(1+\frac{1}{x}\right)^{x}=e, \qquad \lim_{x\to 0}(1+x)^{\frac{1}{x}}=e$$

$1^{\infty}$ 型统一处理：若 $\lim u = 1,\ \lim v = \infty$，则

$$\lim u^{v} = e^{\lim v(u-1)}$$

### 1.3 极限存在准则与常用结论

- **夹逼准则**：$g \le f \le h$ 且 $\lim g = \lim h = A \Rightarrow \lim f = A$
- **单调有界准则**：单调有界数列必收敛（数列极限证明题的固定套路）
- **海涅定理**：$\lim\limits_{x\to x_0}f(x)=A \iff$ 对任意 $x_n \to x_0$ 都有 $f(x_n)\to A$
- $\lim\limits_{n\to\infty}\sqrt[n]{a_1^n+a_2^n+\cdots+a_k^n}=\max\{a_1,\dots,a_k\}$（$a_i>0$）
- $\lim\limits_{n\to\infty}\sqrt[n]{n}=1$，$\lim\limits_{n\to\infty}\sqrt[n]{a}=1\ (a>0)$
- $\lim\limits_{x\to+\infty}\dfrac{x^{a}}{e^{x}}=0$，$\lim\limits_{x\to+\infty}\dfrac{\ln x}{x^{a}}=0\ (a>0)$

**用定积分定义求和式极限**：

$$\lim_{n\to\infty}\frac{1}{n}\sum_{i=1}^{n}f\left(\frac{i}{n}\right)=\int_{0}^{1}f(x)\,dx$$

### 1.4 常用麦克劳林展开（佩亚诺余项）

$$e^{x}=1+x+\frac{x^{2}}{2!}+\cdots+\frac{x^{n}}{n!}+o(x^{n})$$

$$\sin x = x-\frac{x^{3}}{3!}+\frac{x^{5}}{5!}-\cdots+(-1)^{n}\frac{x^{2n+1}}{(2n+1)!}+o(x^{2n+1})$$

$$\cos x = 1-\frac{x^{2}}{2!}+\frac{x^{4}}{4!}-\cdots+(-1)^{n}\frac{x^{2n}}{(2n)!}+o(x^{2n})$$

$$\ln(1+x)=x-\frac{x^{2}}{2}+\frac{x^{3}}{3}-\cdots+(-1)^{n-1}\frac{x^{n}}{n}+o(x^{n})$$

$$(1+x)^{\alpha}=1+\alpha x+\frac{\alpha(\alpha-1)}{2!}x^{2}+\cdots+\frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!}x^{n}+o(x^{n})$$

$$\frac{1}{1-x}=1+x+x^{2}+\cdots+x^{n}+o(x^{n}), \qquad \frac{1}{1+x}=1-x+x^{2}-\cdots+(-1)^{n}x^{n}+o(x^{n})$$

$$\tan x = x+\frac{x^{3}}{3}+\frac{2x^{5}}{15}+o(x^{5}), \qquad \arctan x = x-\frac{x^{3}}{3}+\frac{x^{5}}{5}+o(x^{5})$$

### 1.5 连续与间断点

- **连续**：$\lim\limits_{x\to x_0}f(x)=f(x_0)$，等价于左连续且右连续
- **间断点分类**：
  - 第一类：左右极限都存在 —— 可去间断点（左＝右≠函数值）、跳跃间断点（左≠右）
  - 第二类：左右极限至少一个不存在 —— 无穷间断点、振荡间断点
- **闭区间连续函数的四条性质**：有界性、最值性、介值性、零点存在性

---

## 二、一元函数微分学

### 2.1 定义与可导性

$$f'(x_0)=\lim_{\Delta x\to 0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}=\lim_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}$$

- 可导 $\Rightarrow$ 连续，反之不成立
- 可导 $\iff$ 左导数 ＝ 右导数
- 分段函数在分界点必须用定义求导

### 2.2 基本导数公式

| 函数 | 导数 | 函数 | 导数 |
| --- | --- | --- | --- |
| $C$ | $0$ | $\sin x$ | $\cos x$ |
| $x^{\alpha}$ | $\alpha x^{\alpha-1}$ | $\cos x$ | $-\sin x$ |
| $a^{x}$ | $a^{x}\ln a$ | $\tan x$ | $\sec^{2}x$ |
| $e^{x}$ | $e^{x}$ | $\cot x$ | $-\csc^{2}x$ |
| $\log_a x$ | $\dfrac{1}{x\ln a}$ | $\sec x$ | $\sec x\tan x$ |
| $\ln x$ | $\dfrac{1}{x}$ | $\csc x$ | $-\csc x\cot x$ |
| $\arcsin x$ | $\dfrac{1}{\sqrt{1-x^{2}}}$ | $\arccos x$ | $-\dfrac{1}{\sqrt{1-x^{2}}}$ |
| $\arctan x$ | $\dfrac{1}{1+x^{2}}$ | $\operatorname{arccot} x$ | $-\dfrac{1}{1+x^{2}}$ |

### 2.3 求导法则

$$(uv)'=u'v+uv', \qquad \left(\frac{u}{v}\right)'=\frac{u'v-uv'}{v^{2}}$$

- **复合**：$\{f[g(x)]\}'=f'[g(x)]\cdot g'(x)$
- **反函数**：$[f^{-1}(y)]'=\dfrac{1}{f'(x)}$
- **参数方程**：$\dfrac{dy}{dx}=\dfrac{y'(t)}{x'(t)}$，$\dfrac{d^{2}y}{dx^{2}}=\dfrac{y''(t)x'(t)-y'(t)x''(t)}{[x'(t)]^{3}}$
- **隐函数**：$F(x,y)=0 \Rightarrow \dfrac{dy}{dx}=-\dfrac{F_x}{F_y}$
- **幂指函数** $u^{v}$：取对数 $v\ln u$ 再求导，或写成 $e^{v\ln u}$
- **对数求导法**：连乘、连除、带根式的函数

### 2.4 高阶导数

**莱布尼茨公式**：

$$(uv)^{(n)}=\sum_{k=0}^{n}C_n^{k}u^{(k)}v^{(n-k)}$$

常见 $n$ 阶导数：

$$(e^{ax})^{(n)}=a^{n}e^{ax}, \qquad (\sin ax)^{(n)}=a^{n}\sin\left(ax+\frac{n\pi}{2}\right), \qquad (\cos ax)^{(n)}=a^{n}\cos\left(ax+\frac{n\pi}{2}\right)$$

$$\left[\ln(1+x)\right]^{(n)}=\frac{(-1)^{n-1}(n-1)!}{(1+x)^{n}}, \qquad \left(\frac{1}{x+a}\right)^{(n)}=\frac{(-1)^{n}n!}{(x+a)^{n+1}}$$

### 2.5 微分

$$dy=f'(x)\,dx, \qquad f(x_0+\Delta x)\approx f(x_0)+f'(x_0)\Delta x$$

- 一阶微分形式不变性：无论 $x$ 是自变量还是中间变量，$dy=f'(x)dx$ 都成立
- 常用近似（$|x|$ 很小时）：$\sqrt[n]{1+x}\approx 1+\dfrac{x}{n}$，$e^{x}\approx 1+x$，$\ln(1+x)\approx x$，$\sin x\approx x$

### 2.6 微分中值定理

| 定理 | 条件 | 结论 |
| --- | --- | --- |
| 费马引理 | $x_0$ 为极值点且可导 | $f'(x_0)=0$ |
| 罗尔定理 | $[a,b]$ 连续，$(a,b)$ 可导，$f(a)=f(b)$ | $\exists \xi,\ f'(\xi)=0$ |
| 拉格朗日 | $[a,b]$ 连续，$(a,b)$ 可导 | $f(b)-f(a)=f'(\xi)(b-a)$ |
| 柯西 | 均连续可导且 $g'(x)\ne 0$ | $\dfrac{f(b)-f(a)}{g(b)-g(a)}=\dfrac{f'(\xi)}{g'(\xi)}$ |
| 泰勒 | $n+1$ 阶可导 | 见下 |

**泰勒公式（拉格朗日余项）**：

$$f(x)=\sum_{k=0}^{n}\frac{f^{(k)}(x_0)}{k!}(x-x_0)^{k}+\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}$$

**证明题套路**：结论含 $f'(\xi)$ → 构造辅助函数用罗尔；含两个中值点 → 拉格朗日/柯西分区间；含高阶导 → 泰勒在端点或中点展开。

### 2.7 洛必达法则与未定式

$$\lim\frac{f(x)}{g(x)}=\lim\frac{f'(x)}{g'(x)} \quad \left(\frac{0}{0}\ \text{或}\ \frac{\infty}{\infty}\right)$$

| 未定式 | 处理方式 |
| --- | --- |
| $0\cdot\infty$ | 化为 $\dfrac{0}{1/\infty}$ 或 $\dfrac{\infty}{1/0}$ |
| $\infty-\infty$ | 通分、有理化、提取公因子 |
| $1^{\infty}$ | 用 $e^{\lim v(u-1)}$ |
| $0^{0},\ \infty^{0}$ | 取对数化为 $0\cdot\infty$ |

### 2.8 单调性、极值、凹凸与渐近线

- **单调**：$f'(x)>0$ 递增，$f'(x)<0$ 递减（区间内）
- **极值第一充分条件**：$f'$ 在 $x_0$ 两侧变号
- **极值第二充分条件**：$f'(x_0)=0$ 且 $f''(x_0)\ne 0$；$f''(x_0)<0$ 极大，$f''(x_0)>0$ 极小
- **凹凸**：$f''(x)>0$ 凹（下凸），$f''(x)<0$ 凸（上凸）；$f''$ 变号处为拐点
- **渐近线**：
  - 铅直：$\lim\limits_{x\to x_0}f(x)=\infty$
  - 水平：$\lim\limits_{x\to\infty}f(x)=A$
  - 斜：$k=\lim\limits_{x\to\infty}\dfrac{f(x)}{x}$，$b=\lim\limits_{x\to\infty}[f(x)-kx]$，则 $y=kx+b$

> 曲率为数一内容，数二可跳过：$K=\dfrac{|y''|}{(1+y'^{2})^{3/2}}$。

---

## 三、不定积分

### 3.1 基本积分表

$$\int x^{\alpha}dx=\frac{x^{\alpha+1}}{\alpha+1}+C\ (\alpha\ne -1), \qquad \int \frac{dx}{x}=\ln|x|+C$$

$$\int a^{x}dx=\frac{a^{x}}{\ln a}+C, \qquad \int e^{x}dx=e^{x}+C$$

$$\int \sin x\,dx=-\cos x+C, \qquad \int \cos x\,dx=\sin x+C$$

$$\int \sec^{2}x\,dx=\tan x+C, \qquad \int \csc^{2}x\,dx=-\cot x+C$$

$$\int \sec x\tan x\,dx=\sec x+C, \qquad \int \csc x\cot x\,dx=-\csc x+C$$

$$\int \sec x\,dx=\ln|\sec x+\tan x|+C, \qquad \int \csc x\,dx=\ln|\csc x-\cot x|+C$$

$$\int \tan x\,dx=-\ln|\cos x|+C, \qquad \int \cot x\,dx=\ln|\sin x|+C$$

$$\int \frac{dx}{a^{2}+x^{2}}=\frac{1}{a}\arctan\frac{x}{a}+C$$

$$\int \frac{dx}{\sqrt{a^{2}-x^{2}}}=\arcsin\frac{x}{a}+C$$

$$\int \frac{dx}{x^{2}-a^{2}}=\frac{1}{2a}\ln\left|\frac{x-a}{x+a}\right|+C$$

$$\int \frac{dx}{\sqrt{x^{2}+a^{2}}}=\ln\left(x+\sqrt{x^{2}+a^{2}}\right)+C, \qquad \int \frac{dx}{\sqrt{x^{2}-a^{2}}}=\ln\left|x+\sqrt{x^{2}-a^{2}}\right|+C$$

$$\int \sqrt{a^{2}-x^{2}}\,dx=\frac{x}{2}\sqrt{a^{2}-x^{2}}+\frac{a^{2}}{2}\arcsin\frac{x}{a}+C$$

### 3.2 换元积分法

- **第一类（凑微分）**：$\int f[\varphi(x)]\varphi'(x)dx=\int f(u)du$
- **第二类（变量代换）**：

| 被积函数含 | 令 |
| --- | --- |
| $\sqrt{a^{2}-x^{2}}$ | $x=a\sin t$ |
| $\sqrt{a^{2}+x^{2}}$ | $x=a\tan t$ |
| $\sqrt{x^{2}-a^{2}}$ | $x=a\sec t$ |
| $\sqrt[n]{ax+b}$ | $t=\sqrt[n]{ax+b}$ |
| $e^{x}$ 的有理式 | $t=e^{x}$ |

### 3.3 分部积分

$$\int u\,dv=uv-\int v\,du$$

选 $u$ 的口诀：**反 · 对 · 幂 · 指 · 三**（反三角、对数、幂函数、指数、三角，排在前的取作 $u$）。

### 3.4 有理函数与三角有理式

- **有理函数**：先做多项式除法化为真分式，再部分分式分解
  - 单实根：$\dfrac{A}{x-a}$；$k$ 重实根：$\dfrac{A_1}{x-a}+\cdots+\dfrac{A_k}{(x-a)^{k}}$
  - 不可约二次因式：$\dfrac{Bx+C}{x^{2}+px+q}$
- **三角有理式万能代换**：$t=\tan\dfrac{x}{2}$，则

$$\sin x=\frac{2t}{1+t^{2}}, \qquad \cos x=\frac{1-t^{2}}{1+t^{2}}, \qquad dx=\frac{2}{1+t^{2}}dt$$

---

## 四、定积分及其应用

### 4.1 定义与性质

$$\int_{a}^{b}f(x)dx=\lim_{\lambda\to 0}\sum_{i=1}^{n}f(\xi_i)\Delta x_i$$

- 线性、区间可加性、保号性、$\left|\int f\right|\le\int|f|$
- **估值定理**：$m(b-a)\le\int_a^b f\le M(b-a)$
- **积分中值定理**：$\int_a^b f=f(\xi)(b-a)$

### 4.2 变限积分与牛顿-莱布尼茨

$$\left(\int_{a}^{x}f(t)dt\right)'=f(x), \qquad \left(\int_{a}^{\varphi(x)}f(t)dt\right)'=f[\varphi(x)]\varphi'(x)$$

$$\left(\int_{\psi(x)}^{\varphi(x)}f(t)dt\right)'=f[\varphi(x)]\varphi'(x)-f[\psi(x)]\psi'(x)$$

$$\int_{a}^{b}f(x)dx=F(b)-F(a)$$

### 4.3 对称性、周期性与常用结论

- **奇偶性**：$\int_{-a}^{a}f(x)dx=2\int_{0}^{a}f(x)dx$（偶），$=0$（奇）
- **周期性**：$\int_{a}^{a+T}f(x)dx=\int_{0}^{T}f(x)dx$
- $\int_{0}^{\pi}xf(\sin x)dx=\dfrac{\pi}{2}\int_{0}^{\pi}f(\sin x)dx$
- $\int_{0}^{\pi/2}f(\sin x)dx=\int_{0}^{\pi/2}f(\cos x)dx$
- **华里士（点火）公式**：

$$\int_{0}^{\pi/2}\sin^{n}x\,dx=\int_{0}^{\pi/2}\cos^{n}x\,dx=\begin{cases}\dfrac{n-1}{n}\cdot\dfrac{n-3}{n-2}\cdots\dfrac{1}{2}\cdot\dfrac{\pi}{2}, & n\ \text{为正偶数}\\[4pt] \dfrac{n-1}{n}\cdot\dfrac{n-3}{n-2}\cdots\dfrac{2}{3}\cdot 1, & n\ \text{为正奇数}\end{cases}$$

### 4.4 反常积分

$$\int_{a}^{+\infty}f(x)dx=\lim_{t\to+\infty}\int_{a}^{t}f(x)dx, \qquad \int_{a}^{b}f(x)dx=\lim_{t\to b^{-}}\int_{a}^{t}f(x)dx$$

**$p$ 积分判敛**（核心结论）：

$$\int_{1}^{+\infty}\frac{dx}{x^{p}}\ \text{收敛}\iff p>1, \qquad \int_{0}^{1}\frac{dx}{x^{p}}\ \text{收敛}\iff p<1$$

> 记忆：**无穷区间看 $p>1$，瑕点看 $p<1$**，两者互为镜像。

### 4.5 定积分的几何与物理应用

设平面曲线 $y=f(x)\ge 0$，$a\le x\le b$：

| 量 | 公式 |
| --- | --- |
| 平面图形面积（直角坐标） | $A=\displaystyle\int_{a}^{b}\left[f(x)-g(x)\right]dx$ |
| 面积（极坐标） | $A=\dfrac{1}{2}\displaystyle\int_{\alpha}^{\beta}r^{2}(\theta)\,d\theta$ |
| 绕 $x$ 轴旋转体体积 | $V_x=\pi\displaystyle\int_{a}^{b}f^{2}(x)\,dx$ |
| 绕 $y$ 轴旋转体体积（柱壳法） | $V_y=2\pi\displaystyle\int_{a}^{b}x|f(x)|\,dx$ |
| 绕 $x$ 轴旋转曲面侧面积 | $S=2\pi\displaystyle\int_{a}^{b}|f(x)|\sqrt{1+f'^{2}(x)}\,dx$ |
| 弧长（直角坐标） | $s=\displaystyle\int_{a}^{b}\sqrt{1+f'^{2}(x)}\,dx$ |
| 弧长（参数方程） | $s=\displaystyle\int_{\alpha}^{\beta}\sqrt{x'^{2}(t)+y'^{2}(t)}\,dt$ |
| 弧长（极坐标） | $s=\displaystyle\int_{\alpha}^{\beta}\sqrt{r^{2}(\theta)+r'^{2}(\theta)}\,d\theta$ |
| 函数平均值 | $\bar{f}=\dfrac{1}{b-a}\displaystyle\int_{a}^{b}f(x)dx$ |
| 变力做功 | $W=\displaystyle\int_{a}^{b}F(x)\,dx$ |
| 水压力 | $P=\rho g\displaystyle\int_{a}^{b}h(x)\cdot l(x)\,dx$ |
| 形心 | $\bar{x}=\dfrac{\int_a^b x f(x)dx}{\int_a^b f(x)dx}$ |

> **技巧**：旋转体体积优先比较"圆盘法"与"柱壳法"哪个积分更容易；侧面积别漏掉 $\sqrt{1+f'^2}$。

---

## 五、多元函数微分学

### 5.1 偏导数与全微分

$$f_x(x_0,y_0)=\lim_{\Delta x\to 0}\frac{f(x_0+\Delta x,y_0)-f(x_0,y_0)}{\Delta x}$$

$$dz=f_x(x,y)dx+f_y(x,y)dy$$

- 可微 $\Rightarrow$ 偏导存在，且 $\Rightarrow$ 连续；反之均不成立
- **可微的充分条件**：偏导数连续 $\Rightarrow$ 可微
- **可微的判定式**：$\lim\limits_{(\Delta x,\Delta y)\to(0,0)}\dfrac{\Delta z-f_x\Delta x-f_y\Delta y}{\sqrt{\Delta x^{2}+\Delta y^{2}}}=0$

### 5.2 复合函数与隐函数求导

- **链式法则**：$z=f(u,v),\ u=u(x,y),\ v=v(x,y)$

$$\frac{\partial z}{\partial x}=\frac{\partial z}{\partial u}\frac{\partial u}{\partial x}+\frac{\partial z}{\partial v}\frac{\partial v}{\partial x}$$

- **隐函数**：$F(x,y)=0 \Rightarrow \dfrac{dy}{dx}=-\dfrac{F_x}{F_y}$；$F(x,y,z)=0 \Rightarrow \dfrac{\partial z}{\partial x}=-\dfrac{F_x}{F_z},\ \dfrac{\partial z}{\partial y}=-\dfrac{F_y}{F_z}$

### 5.3 极值与最值

**无条件极值**：驻点满足 $f_x=f_y=0$，记 $A=f_{xx},\ B=f_{xy},\ C=f_{yy}$：

- $AC-B^{2}>0$：$A>0$ 取极小值，$A<0$ 取极大值
- $AC-B^{2}<0$：不是极值点
- $AC-B^{2}=0$：失效，需另作判断

**条件极值（拉格朗日乘数法）**：求 $f(x,y)$ 在 $\varphi(x,y)=0$ 下的极值，构造

$$L(x,y,\lambda)=f(x,y)+\lambda\varphi(x,y)$$

令 $L_x=L_y=L_\lambda=0$ 解出候选点。

**有界闭区域上求最值**：区域内部驻点 ＋ 边界上的最值，逐一比较。

---

## 六、二重积分

### 6.1 性质与对称性

$$\iint_{D}\left[af+bg\right]d\sigma=a\iint_{D}f\,d\sigma+b\iint_{D}g\,d\sigma$$

- **关于 $x$ 轴对称**：$f$ 关于 $y$ 为奇函数 $\Rightarrow \iint_D f\,d\sigma=0$；为偶函数 $\Rightarrow$ 等于上半部分的两倍
- **关于 $y$ 轴对称**：同理，看 $f$ 关于 $x$ 的奇偶性
- **轮换对称性**：$D$ 关于直线 $y=x$ 对称 $\Rightarrow \iint_D f(x,y)d\sigma=\iint_D f(y,x)d\sigma$
- $\iint_D 1\,d\sigma=S_D$（区域面积）

> 拿到二重积分先问三句：**区域对称吗？被积函数有奇偶性吗？换极坐标会简单吗？**

### 6.2 直角坐标

$$\iint_{D}f\,d\sigma=\int_{a}^{b}dx\int_{y_1(x)}^{y_2(x)}f(x,y)\,dy \quad (\text{X 型})$$

$$\iint_{D}f\,d\sigma=\int_{c}^{d}dy\int_{x_1(y)}^{x_2(y)}f(x,y)\,dx \quad (\text{Y 型})$$

**交换积分次序**：画出积分区域 → 重新按另一方向定限（这是高频考点，别硬算）。

### 6.3 极坐标

$$x=r\cos\theta,\quad y=r\sin\theta,\quad d\sigma=r\,dr\,d\theta$$

$$\iint_{D}f\,d\sigma=\int_{\alpha}^{\beta}d\theta\int_{r_1(\theta)}^{r_2(\theta)}f(r\cos\theta,r\sin\theta)\,r\,dr$$

> 适用信号：区域是圆/扇形/环，或被积函数含 $x^{2}+y^{2}$。极坐标下 $d\sigma$ 中的 $r$ **千万别漏**。

---

## 七、常微分方程

### 7.1 基本概念

- 阶 = 最高阶导数的阶数；通解含独立常数个数 = 阶数
- 初始条件定特解；$y'=f(x)g(y)$ 分离变量时注意 $g(y)=0$ 的常数解

### 7.2 一阶微分方程

| 类型 | 形式 | 解法 |
| --- | --- | --- |
| 可分离变量 | $\dfrac{dy}{dx}=f(x)g(y)$ | 分离后两边积分 |
| 齐次方程 | $\dfrac{dy}{dx}=\varphi\left(\dfrac{y}{x}\right)$ | 令 $u=\dfrac{y}{x}$，化为可分离 |
| 一阶线性 | $y'+P(x)y=Q(x)$ | 见下方通解公式 |
| 伯努利（拓展） | $y'+P(x)y=Q(x)y^{n}$ | 令 $z=y^{1-n}$ 化为一阶线性 |

**一阶线性通解公式**：

$$y=e^{-\int P(x)dx}\left[\int Q(x)e^{\int P(x)dx}dx+C\right]$$

### 7.3 可降阶的二阶方程

| 形式 | 换元 |
| --- | --- |
| $y''=f(x)$ | 连续两次积分 |
| $y''=f(x,y')$ | 令 $p=y'$，则 $y''=p'$ |
| $y''=f(y,y')$ | 令 $p=y'$，则 $y''=p\dfrac{dp}{dy}$ |

### 7.4 二阶常系数线性方程

**齐次** $y''+py'+qy=0$，特征方程 $r^{2}+pr+q=0$：

| 根的情况 | 通解 |
| --- | --- |
| 两个不等实根 $r_1\ne r_2$ | $y=C_1e^{r_1x}+C_2e^{r_2x}$ |
| 二重实根 $r$ | $y=(C_1+C_2x)e^{rx}$ |
| 共轭复根 $\alpha\pm\beta i$ | $y=e^{\alpha x}(C_1\cos\beta x+C_2\sin\beta x)$ |

**非齐次** $y''+py'+qy=f(x)$：通解 ＝ 齐次通解 ＋ 一个特解 $y^{*}$。

| $f(x)$ 形式 | 特解设法 | $k$ 的取法 |
| --- | --- | --- |
| $P_m(x)e^{\lambda x}$ | $y^{*}=x^{k}Q_m(x)e^{\lambda x}$ | $\lambda$ 是特征根的重数（0/1/2） |
| $e^{\alpha x}\left[P_l(x)\cos\beta x+P_n(x)\sin\beta x\right]$ | $y^{*}=x^{k}e^{\alpha x}\left[R_m(x)\cos\beta x+S_m(x)\sin\beta x\right]$ | $\alpha\pm\beta i$ 是特征根取 1，否则取 0 |

其中 $m=\max\{l,n\}$，$Q_m,R_m,S_m$ 为待定的 $m$ 次多项式。

> **叠加原理**：若 $f=f_1+f_2$，可分别求特解再相加。

---

## 八、线性代数

### 8.1 行列式

**基本性质**：

$$|A^{T}|=|A|, \qquad |kA|=k^{n}|A|, \qquad |AB|=|A||B|, \qquad |A^{-1}|=\frac{1}{|A|}, \qquad |A^{*}|=|A|^{n-1}$$

- 两行（列）互换变号；某行乘 $k$ 等于行列式乘 $k$；某行加上另一行的 $k$ 倍不变
- 两行（列）成比例或相同 $\Rightarrow |A|=0$
- 上（下）三角行列式 ＝ 对角线元素之积
- **按行（列）展开**：$|A|=\sum\limits_{j=1}^{n}a_{ij}A_{ij}$（$A_{ij}$ 为代数余子式）

**常用特殊行列式**：

- **范德蒙德**：$\begin{vmatrix}1&1&\cdots&1\\ x_1&x_2&\cdots&x_n\\ \vdots&\vdots&&\vdots\\ x_1^{n-1}&x_2^{n-1}&\cdots&x_n^{n-1}\end{vmatrix}=\prod_{1\le i<j\le n}(x_j-x_i)$
- **分块（拉普拉斯）**：$\begin{vmatrix}A&O\\ C&B\end{vmatrix}=|A||B|$

### 8.2 矩阵

**运算律**：

$$(AB)^{T}=B^{T}A^{T}, \qquad (AB)^{-1}=B^{-1}A^{-1}, \qquad (A^{T})^{-1}=(A^{-1})^{T}, \qquad (A^{*})^{-1}=(A^{-1})^{*}=\frac{A}{|A|}$$

> 注意：$(AB)^{*}=B^{*}A^{*}$；$(A+B)^{*}\ne A^{*}+B^{*}$；$AB=0$ 推不出 $A=0$ 或 $B=0$。

**伴随矩阵**：

$$AA^{*}=A^{*}A=|A|E, \qquad A^{-1}=\frac{A^{*}}{|A|}\ (|A|\ne 0)$$

$$r(A^{*})=\begin{cases}n, & r(A)=n\\ 1, & r(A)=n-1\\ 0, & r(A)<n-1\end{cases}$$

**秩的不等式**：

$$r(A+B)\le r(A)+r(B), \qquad r(AB)\le \min\{r(A),r(B)\}, \qquad r(AB)\ge r(A)+r(B)-n$$

- $A$ 可逆 $\Rightarrow r(AB)=r(B)$（左乘右乘可逆矩阵秩不变）
- 初等变换不改变秩；初等矩阵左乘 ＝ 行变换，右乘 ＝ 列变换
- $n$ 阶矩阵 $A$ 可逆 $\iff r(A)=n \iff |A|\ne 0 \iff$ 特征值全不为 0

### 8.3 向量与线性方程组

**线性相关性**：$\alpha_1,\dots,\alpha_s$ 线性相关 $\iff$ 存在不全为零的 $k_i$ 使 $\sum k_i\alpha_i=0$ $\iff r(\alpha_1,\dots,\alpha_s)<s$。

- 向量个数 > 维数 $\Rightarrow$ 必线性相关
- 部分相关 $\Rightarrow$ 整体相关；整体无关 $\Rightarrow$ 部分无关
- **施密特正交化**：$\beta_1=\alpha_1$，$\beta_k=\alpha_k-\sum\limits_{i=1}^{k-1}\dfrac{(\alpha_k,\beta_i)}{(\beta_i,\beta_i)}\beta_i$，再单位化
- **正交矩阵**：$A^{T}A=E$，$|A|=\pm 1$，特征值只能是 $\pm 1$

**解的判定**（$A$ 为 $m\times n$）：

| 方程组 | 条件 | 结论 |
| --- | --- | --- |
| $Ax=0$ | $r(A)=n$ | 只有零解 |
| $Ax=0$ | $r(A)<n$ | 有非零解，基础解系含 $n-r(A)$ 个向量 |
| $Ax=b$ | $r(A)<r(A\mid b)$ | 无解 |
| $Ax=b$ | $r(A)=r(A\mid b)=n$ | 唯一解 |
| $Ax=b$ | $r(A)=r(A\mid b)<n$ | 无穷多解 |

**解的结构**：$Ax=b$ 通解 ＝ 一个特解 ＋ $Ax=0$ 的通解；$Ax=0$ 的任一解是基础解系的线性组合。

### 8.4 特征值与特征向量

$$A\alpha=\lambda\alpha\ (\alpha\ne 0), \qquad |\lambda E-A|=0$$

**常用性质**：

$$\sum_{i=1}^{n}\lambda_i=\operatorname{tr}(A), \qquad \prod_{i=1}^{n}\lambda_i=|A|$$

| $A$ 的特征值 | 对应矩阵的特征值 |
| --- | --- |
| $\lambda$ | $kA \to k\lambda$；$A^{m}\to\lambda^{m}$；$f(A)\to f(\lambda)$ |
| $\lambda$ | $A^{-1}\to\dfrac{1}{\lambda}$；$A^{*}\to\dfrac{|A|}{\lambda}$ |
| $\lambda$ | $A^{T}$ 与 $A$ 特征值相同 |

- 不同特征值对应的特征向量线性无关
- **可对角化** $\iff$ 有 $n$ 个线性无关的特征向量 $\iff$ 每个特征值的几何重数 ＝ 代数重数
- $A\sim B$（相似）$\Rightarrow$ 特征值相同、秩相同、迹相同、行列式相同
- **实对称矩阵**：必可正交对角化；不同特征值的特征向量必正交；$k$ 重特征值恰有 $k$ 个线性无关特征向量

**实对称矩阵正交对角化步骤**：求特征值 → 求特征向量 → 同一特征值的向量组施密特正交化 → 全部单位化得正交矩阵 $Q$ → $Q^{-1}AQ=Q^{T}AQ=\Lambda$。

### 8.5 二次型

$$f(x_1,\dots,x_n)=x^{T}Ax,\quad A^{T}=A$$

- **标准形**：只含平方项；**规范形**：系数只有 $1,-1,0$
- **惯性定理**：二次型的正、负惯性指数在可逆线性变换下不变
- **合同**：存在可逆 $C$ 使 $B=C^{T}AC$，记 $A\simeq B$
- **化标准形两法**：配方法（可逆线性变换）、正交变换法（保持几何形状，$x=Qy$）
- **正定判定**（下列等价）：
  1. 对任意 $x\ne 0$ 有 $x^{T}Ax>0$
  2. 正惯性指数 $=n$
  3. 特征值全为正
  4. 顺序主子式全大于 0
  5. 存在可逆 $C$ 使 $A=C^{T}C$

---

## 九、高频易错速查

| 易错点 | 正确做法 |
| --- | --- |
| 加减结构里用等价无穷小替换 | 改用泰勒展开到足够阶 |
| 洛必达前不验证 $0/0$ 或 $\infty/\infty$ | 先判断类型，非未定式不能洛必达 |
| 用 $f'(x_0)$ 代替分段点处的定义求导 | 分界点一律用定义求左右导数 |
| 积分漏绝对值 | $\int \frac{1}{x}dx=\ln|x|+C$，含对数都要加绝对值 |
| 极坐标下丢 $r$ | $d\sigma=r\,dr\,d\theta$ |
| 二重积分直接硬算 | 先看对称性与奇偶性，再看能否交换次序 |
| 二阶非齐次特解漏乘 $x^{k}$ | 先看 $\lambda$ 是否为特征根及其重数 |
| 分离变量丢常数解 | 检查 $g(y)=0$ 的情形 |
| 混淆 $|A+B|$ 与 $|A|+|B|$ | 行列式对加法不线性 |
| 忘记 $r(A^{*})$ 的分段结论 | 按 $r(A)=n,\ n-1,\ <n-1$ 三种情况 |
| 判断可对角化只看特征值个数 | 要看几何重数是否等于代数重数 |

---

> **维护提醒**：本页随复习推进持续补充。新增专题（如"中值定理证明套路""二重积分技巧"）可另建 `主题名.md`，并用相对路径链接回本手册。
