---
layout:     post
title:      "Mathematical Physics by Sadri Hassani 抄书（1）"
subtitle:   "第二章 向量和线性映射"
date:       2024-10-21 13:00:00
author:     "Whitney"
header-img: "img/in-post/mathe-physics-bg.jpg"
catalog: true
usemathjax: true
header-mask:  0.3
tags:
    - 数学
    - 笔记
    - 物理
    - 数学物理
---

## 向量空间
&emsp;&emsp;**定义**&emsp;&emsp;一个在$\mathbb{C}$上的**向量空间**$\mathcal{V}$包含一个二元的阿贝尔的运算和一些满足以下性质的**向量**组成的集合：

$$
\forall \left \vert a \right \rangle, \left \vert b \right \rangle, \left \vert c \right \rangle, \left \vert 0 \right \rangle \in \mathcal{V}
\begin{cases}
    \left \vert a \right \rangle + (\left \vert b \right \rangle + \left \vert c \right \rangle ) = (\left \vert a \right \rangle + \left \vert b \right \rangle) + \left \vert c \right \rangle \\
    \forall \left \vert a \right \rangle, \exists \left \vert 0 \right \rangle \ \ s.t. \left \vert a \right \rangle + \left \vert 0 \right \rangle = \left \vert a \right \rangle\\
    \forall \left \vert a \right \rangle, \exists -\left \vert a \right \rangle \in \mathcal{V}\ \ s.t. \left \vert a \right \rangle + (-\left \vert a \right \rangle) = \left \vert 0 \right \rangle\\
    \forall \alpha \in \mathbb{C}, \left \vert a \right \rangle \in \mathcal{V}, \exists \alpha\left \vert a \right \rangle \in \mathcal{V}\ \ s.t. \alpha(\beta\left \vert a \right \rangle) = (\alpha\beta)\left \vert a \right \rangle, 1\left \vert a \right \rangle = \left \vert a \right \rangle\\
    \alpha(\left \vert a \right \rangle+ \left \vert b \right \rangle) = \alpha\left \vert a \right \rangle + \alpha\left \vert b \right \rangle\\
    (\alpha + \beta)\left \vert a \right \rangle = \alpha\left \vert a \right \rangle+ \beta \left \vert a \right \rangle.
\end{cases}
$$

以上七条加上运算的阿贝尔性构成了向量空间的八条性质。这里我们用狄拉克的符号**bra** $\left \langle  \right \vert$ 和 **ket** $\left \vert  \right \rangle$ 来代表向量。
<br>
&emsp;&emsp;以上使用复数定义的向量空间被称作复向量空间；如果在以上的定义中将复数集$\mathbb{C}$换作$\mathbb{R}$，那么我们就可以得到一个实向量空间。$\mathbb{C}$和$\mathbb{R}$都是数学结构**域**的具体例子；域是一个配有两个名叫加法和乘法的二元运算的集合，并且每个运算都有自己的单位元。加法的单位元被记作$0$，乘法的单位元被记作$1$。对于域中的每一个元素$\alpha$，都有其在加法下的逆元$-\alpha$和在乘法下的逆元$\alpha^{-1}$。

>注：向量空间中，我们往往还需关注其所作用的域。例如，$\mathbb{C}$是$\mathbb{R}$上的向量空间而$\mathbb{R}$就不是$\mathbb{C}$上的向量空间。

<br>
&emsp;&emsp;一些重要的向量空间如下：
1. 复系数的多项式组成的集合配以普通的加法构成一个复数上的向量空间，被记作$\mathcal{P^c[t]}$.
2. 所有$m\times n$的矩阵组成的集合配以普通的矩阵加法构成一个复数上的向量空间。
3. 所有收敛的复数序列$\mathbb{C}^\infty$构成一个复数上的向量空间。
4. 所有在$(a, b)$上连续且任意阶可导的函数的集合构成一个实数上的向量空间。

<br>
&emsp;&emsp;**定义**&emsp;&emsp;如果对于等式$\sum^n_{i = 1}\alpha_i \left \vert a_i \right \rangle = 0$能够对于所有的$i$推得$\alpha_i = 0$，那么我们称这些向量$\left \vert a_1 \right \rangle, \left \vert a_2 \right \rangle, \cdots, \left \vert a_n \right \rangle$**线性独立**，并称$\sum^n_{i = 1}\alpha_i \left \vert a_i \right \rangle$是$\{\left \vert a_i \right \rangle\}^n_{i = 1}$的一个**线性组合**。

### 子空间
&emsp;&emsp;**定义**&emsp;&emsp;一个向量空间$\mathcal{V}$的**子空间**$\mathcal{W}$是一个满足以下性质的$\mathcal{V}$的一个非空子集：

$$
\left \vert a \right \rangle, \left \vert b \right \rangle \in \mathcal{W} \Rightarrow \forall \alpha, \beta \in \mathbb{C}, \alpha\left \vert a \right \rangle+\beta \left \vert b \right \rangle \in \mathcal{W}.
$$