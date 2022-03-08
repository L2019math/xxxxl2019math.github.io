---
title: Ch2-导数与微分
date: 2022-01-30 21:09:48
categories: 研究生入学考试
tags: 高等数学
cover: /img/math.jpg
---

# 基本概念

## 基本公式

1. $ y=x^{a}( \alpha 为实数) \quad y^{\prime}=\alpha x^{\alpha-1} \quad \mathrm{~d} y=\alpha x^{\alpha-1} \mathrm{~d} x$
2. $ y=a^{x} \quad y^{\prime}=a^{x} \ln a \quad \mathrm{~d} y=a^{x} \ln a \mathrm{~d} x$
3. $ y=\log _{a} x, a>0, a \neq 1 \quad y^{\prime}=\frac{1}{x \ln a} \quad \mathrm{~d} y=\frac{1}{x \ln a} \mathrm{~d} x \quad(x>0)$
4. $ y=\tan x \quad y^{\prime}=\frac{1}{\cos ^{2} x}=\sec ^{2} x \quad \mathrm{~d}(\tan x)=\sec ^{2} x \mathrm{~d} x$
5. $ y=\sec x \quad y^{\prime}=\sec x \tan x \quad \mathrm{~d}(\sec x)=\sec x \tan x d x$
6. $ y=\arcsin x \quad y^{\prime}=\frac{1}{\sqrt{1-x^{2}}} \quad \mathrm{~d}(\arcsin x)=\frac{1}{\sqrt{1-x^{2}}} \mathrm{~d} x$
7. $ y=\arccos x \quad y^{\prime}=-\frac{1}{\sqrt{1-x^{2}}} \quad \mathrm{~d}(\arccos x)=-\frac{1}{\sqrt{1-x^{2}}} \mathrm{~d} x$
8. $ y=\arctan x \quad y^{\prime}=\frac{1}{1+x^{2}} \quad d(\arctan x)=\frac{1}{1+x^{2}} d x$
9. $ y=\operatorname{arccot} x \quad y^{\prime}=-\frac{1}{1+x^{2}} \quad \mathrm{~d}(\operatorname{arccot} x)=-\frac{1}{1+x^{2}} \mathrm{~d} x$

> 反三角函数特殊记忆：反正弦 是 根号负(x^2 前的符号)，反正切 是 $1+x^2$ 可联系 $1+\tan^2x=\sec^2x$ 记忆。

## 弧微分和曲率

### 弧微分

弧微分是用一条线段的长度来近似代表一段弧的长度。设函数$f(x)$在区间$(a,b)$内具有连续导数，在曲线Y=f(x)上取定点$M_o(x_o,f(x_o))$作为计算曲线弧长的基点，$M(x,y)$是曲线上任意一点。

1. 直角坐标系 ：$ \mathrm{d} s=\sqrt{1+y^{\prime 2}} \mathrm{~d} x$
2. 参数方程：$ \quad \mathrm{d} s=\sqrt{x^{\prime 2}(t)+y^{\prime 2}(t)} \mathrm{d} t $
3. 极坐标方程：$ d s=\sqrt{r^{\prime 2}(\theta)+r^{2}(\theta)} d \theta$

### 曲率

曲率公式：  $ k=\frac{\left|y^{\prime \prime}\right|}{\left(1+y^{\prime 2}\right)^{\frac{3}{2}}}$

曲率半径：$ \rho=\frac{1}{k}$

## 高阶导数

1. $ \left(a^{x}\right)^{(n)}=a^{x} \ln ^{n} a \quad(a>0)$, 特别的 $ \left(\mathrm{e}^{x}\right)^{(n)}=\mathrm{e}^{x}$
1. $ (\sin k x)^{(n)}=k^{n} \sin \left(k x+n \cdot \frac{\pi}{2}\right)$
1. $ (\cos k x)^{(n)}=k^{n} \cos \left(k x+n \cdot \frac{\pi}{2}\right)$
1. $ \left(x^{m}\right)^{(n)}=m(m-1) \cdots(m-n+1) x^{m-n}$
1. 菜布尼茨公式: 若 $ u(x), v(x)$ 均 $ n$ 阶可导,则 $ (u v)^{(n)}=\sum^{n} C_{n}^{\prime} u^{(i)} v^{(n-i)}$, 其中 $ u^{(0)}=u, v^{(0)}=v$.



# 常见题型

## 链式求导法则

题目

设 $\left\{\begin{array}{l}x=f^{\prime}(t), \\ y=t f^{\prime}(t)-f(t),\end{array}\right.$ 其中 $f(t)$ 的三阶导数存在, 且 $f^{\prime \prime}(t) \neq 0$. 求 $\frac{\mathrm{d} y}{\mathrm{~d} x}, \frac{\mathrm{d}^{2} y}{\mathrm{~d} x^{2}}, \frac{\mathrm{d}^{3} y}{\mathrm{~d} x^{3}}$.

解答

$ \frac{\mathrm{d} y}{\mathrm{~d} x}=\frac{y^{\prime}(t)}{x^{\prime}(t)}=\frac{f^{\prime}(t)+t f^{\prime \prime}(t)-f^{\prime}(t)}{f^{\prime \prime}(t)}=t$

$ \frac{\mathrm{d}^{2} y}{\mathrm{~d} x^{2}}=\frac{\mathrm{d}}{\mathrm{d} x}\left(\frac{\mathrm{d} y}{\mathrm{~d} x}\right)=\frac{\mathrm{d}}{\mathrm{d} x}(t)=\frac{1}{f^{\prime \prime}(t)}$

$ \frac{\mathrm{d}^{3} y}{\mathrm{~d} x^{3}}=\frac{\mathrm{d}}{\mathrm{d} x}\left(\frac{\mathrm{d}^{2} y}{\mathrm{~d} x^{2}}\right)=\frac{\mathrm{d}}{\mathrm{d} x}\left(\frac{1}{f^{\prime \prime}(t)}\right)=\frac{\mathrm{d}}{\mathrm{d} t}\left(\frac{1}{f^{\prime \prime}(t)}\right) \cdot \frac{\mathrm{d} t}{\mathrm{~d} x}$

$ \quad\quad =-\frac{f^{\prime \prime \prime}(t)}{\left[f^{\prime \prime}(t)\right]^{2}} \cdot \frac{1}{f^{\prime \prime}(t)}=-\frac{f^{\prime \prime \prime}(t)}{\left[f^{\prime \prime}(t)\right]^{3}} .$

## 隐函数求导

![隐函数求导的三种方法](https://cdn.jsdelivr.net/gh/L2019math/imagebed@main/image-20220130235151375.png)

> 解析
>
> 1. 方程两边对 $x$ 求导,要记住 $y$ 是 $x$ 的函数,则 $y$ 的函数是 $x$ 的复合函数,例如 $\frac{1}{y}, y^{2}$, $\ln y, \mathrm{e}^{y}$ 等均是 $x$ 的复合函数. 对 $x$ 求导应按复合函数连锁法则做;
>
> 2. 公式法. 由 $F(x, y)=0$, 知
>    $$
>    \frac{\mathrm{d} y}{\mathrm{~d} x}=-\frac{F_{x}^{\prime}(x, y)}{F_{y}^{\prime}(x, y)},
>    $$
>    其中, $ F_{x}^{\prime}(x, y), F_{y}^{\prime}(x, y)$ 分别表示 $ F(x, y)$ 对 $ x$ 和 $ y$ 的偏导数.
>
> 3. 利用微分形式不变性, 在方程两边求微分, 然后解出 $ \frac{\mathrm{d} y}{\mathrm{~d} x}$.

## 反函数求导

![反函数求导](https://cdn.jsdelivr.net/gh/L2019math/imagebed@main/image-20220131000638337.png)

> 注意本题是 $ x=f(y)$  , 切勿想当然认为$y=f(x)$，同时反函数的题目不要慌，按照最基本的定义来做。

## 定义题

![定义题1](https://cdn.jsdelivr.net/gh/L2019math/imagebed@main/image-20220131002810541.png)
![定义题2](https://cdn.jsdelivr.net/gh/L2019math/imagebed@main/image-20220131002851200.png)

> 本题考察了多方面的细节，属于佳题！
>
> 1. $e^{\infty}$ 的两种不同取值，$+\infty$ 趋近于无穷大，$-\infty$ 时趋近于 0
> 2. 函数的确定，分类讨论
> 3. 某点导数存在的充要条件：左导数 = 右导数
> 4. 某点处导数的定义
> 5. 可导必连续，连续不一定可导

