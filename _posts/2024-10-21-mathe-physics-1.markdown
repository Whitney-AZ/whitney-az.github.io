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
2. 所有$m\times n$的矩阵组成的集合$\mathcal{M}^{m\times n}$配以普通的矩阵加法构成一个复数上的向量空间。
3. 所有收敛的复数序列$\mathbb{C}^\infty$构成一个复数上的向量空间。
4. 所有在$(a, b)$上连续且任意阶可导的函数的集合构成一个实数上的向量空间。

<br>
&emsp;&emsp;**定义**&emsp;&emsp;如果对于等式$\sum^n_{i = 1}\alpha_i \left \vert a_i \right \rangle = 0$能够对于所有的$i$推得$\alpha_i = 0$，那么我们称这些向量$\left \vert a_1 \right \rangle, \left \vert a_2 \right \rangle, \cdots, \left \vert a_n \right \rangle$**线性独立**，并称$\sum^n_{i = 1}\alpha_i \left \vert a_i \right \rangle$是$\{\left \vert a_i \right \rangle\}^n_{i = 1}$的一个**线性组合**。

### 子空间
&emsp;&emsp;**定义**&emsp;&emsp;一个向量空间$\mathcal{V}$的**子空间**$\mathcal{W}$是一个满足以下性质的$\mathcal{V}$的一个非空子集：

$$
\left \vert a \right \rangle, \left \vert b \right \rangle \in \mathcal{W} \Rightarrow \forall \alpha, \beta \in \mathbb{C}, \alpha\left \vert a \right \rangle+\beta \left \vert b \right \rangle \in \mathcal{W}.
$$

&emsp;&emsp;**定理**&emsp;&emsp;记向量空间$\mathcal{V}$中任意非空子集为$S$，那么$S$中所有元素的线性组合的集合$\mathcal{W}_S$构成$\mathcal{V}$的一个子空间。我们称$S$张成$\mathcal{W}_S$，$\mathcal{W}_S$常被记作$\mathrm{Span}\{S\}$。

&emsp;&emsp;**定义**&emsp;&emsp;向量空间$\mathcal{V}$的一组**基**是一个线性独立向量组成的集合$B$，并且$B$张成$\mathcal{V}$。如果一个向量空间有有限个基，那么这个向量空间被称作**有限维的向量空间**；如果有无限多个基，那么被称为**无穷维向量空间**。

&emsp;&emsp;**定理**&emsp;&emsp;所有给定的有限维向量空间的基的线性独立的向量个数相同。
>这一条定理实际上保证了基之间变换的可能性和给定有限维向量空间维数的唯一性。换句话讲，如果我们按照基的个数来定义一个向量空间的维数（正如下面一个定义将要做的），那么根据这个定理一个向量空间就不可能有两个不同的维度。

&emsp;&emsp;**定义**&emsp;&emsp;向量空间$\mathcal{V}$的基的势被称作$\mathcal{V}$的**维度**，记作$\dim \mathcal{V}$。

&emsp;&emsp;对于任意一个$\vert a \rangle \in \mathcal{V}$ 以及一个向量空间中的基 $B = \{\vert a_i \rangle\}^N_{i = 1}$， 存在且唯一存在一组标量$\{\alpha_1, \alpha_2, \ldots, \alpha_n\}$ 使得$\vert a \rangle=\sum_{i=1}^N \alpha_i\vert a_i\rangle$. 这个集合$\{ \alpha_i \}_{i=1}^N$被称作$\vert a\rangle$在基$B$下的**分量**。

<br>
&emsp;&emsp;上面提过的向量空间的基可以取作：
1. $\mathcal{P}^c[t]$的基显然可以取为$1, t, t^2, \ldots$。显然这个向量空间是无穷维的。
2. $\mathcal{M}^{m \times n}$的基可以取作$e_{11}, e_{12}, \ldots , e_{mn}$，其中$e_{ij}$是只有$a_{ij}$是$1$，其余元素都为$0$的矩阵。

>特别注意的是，一个基的子集张成的空间是原来的向量空间的子空间。

### 商空间
&emsp;&emsp;对于向量空间$\mathcal{V}$及其子空间$\mathcal{W}$，在$\mathcal{V}$上定义一种等价关系：对于$\vert a\rangle \in \mathcal{V}$ and $\vert b\rangle \in \mathcal{V}$, 如果$\vert a\rangle-\vert b\rangle$ is in $\mathcal{W}$，那么我们说$\vert a\rangle$和$\vert b\rangle$等价,并记作$\vert a\rangle \bowtie\vert b\rangle$。将这种等价类记作$\[ a\]$，并将集合$\{\[a\] \ \big\vert \ \vert a\rangle \in \mathcal{V} \}$ 记作 $\mathcal{V} / \mathcal{W}$。
>商集合（或者后面会使用的商空间）实际上是一个等价类的集合。采用维基百科上的例子，令$X$是所有汽车的集合，定义等价关系为所有颜色一样的车，那么商集合就是所有轿车颜色的集合。

我们可以按照如下定义

$$
\alpha[a] + \beta[b] = [\alpha a + \beta b]
$$

从而将一个商集合变为一个商空间。
> 商空间可以自然的看成积空间的逆运算；这也是其商空间名字的来源。

我们还能通过如下的论证找到商空间中的一组基矢：

$$
[a] \equiv \left\vert a \right\rangle + \mathcal{W} = \sum_i\alpha_i\left\vert a_i\right\rangle + \sum_j\beta_j\left\vert b_j\right\rangle + \mathcal{W}\\
\ \ \  =\sum_j\beta_j\left\vert b_j\right\rangle + \mathcal{W}\\
\Longrightarrow [a] = \left[\sum_j\beta_j\left\vert b_j\right\rangle\right] = \sum_j\beta_j[b_j]
$$

因此$\{[b_j]\}$张成$\mathcal{V}/\mathcal{W}$。我们还能得到如下的结论：

$$
\mathrm{dim}\left(\mathcal{V}/\mathcal{W}\right) = \mathrm{dim}\mathcal{V} - \mathrm{dim}\mathcal{W}.
$$

### 直和
&emsp;&emsp;将一个向量空间拆成两个向量空间通常是非常实用的。因此我们令 $\mathcal{U}, \mathcal{W}$ 是 $\mathcal{V}$ 的子空间，将所有能够写作两个子空间中元素的和的向量的集合记作 $\mathcal{U} + \mathcal{W}$ 。那么很显然这个集合是原来向量空间的子空间。如果满足 $\mathcal{V} = \mathcal{U} + \mathcal{W}$ 且 $\mathcal{U}\cap \mathcal{W} = \left\vert 0\right\rangle$，那么我们称 $\mathcal{V}$ 是 $\mathcal{U}$ 和 $\mathcal{W}$ 的直积，记作 $\mathcal{V} = \mathcal{U} \oplus \mathcal{W}$。直积有诸多好性质。比如，对于一个向量空间的一个子空间，总存在另一个子空间使得两者直积成原来的子空间，而且 $\mathrm{dim}\left(\mathcal{V}\right) = \mathrm{dim}\mathcal{U} + \mathrm{dim}\mathcal{W}.$

### 笛卡尔积
&emsp;&emsp;笛卡尔积是直和的一个特殊情况。在笛卡尔积中，两个子空间的元素仅有某些分量不为0，即若 $\mathcal{V} = \mathcal{U} \oplus \mathcal{W}$，那么 $\mathcal{U}$ 中的元素可以被写作 $(\left\vert u \right\rangle, \left\vert 0\right\rangle_\mathcal{W})$ 和 $(\left\vert 0 \right\rangle_\mathcal{U}, \left\vert w\right\rangle)$。通过这种方式我们将两个向量空间粘在了一起，形成了一个更高维的空间。

### 张量积
&emsp;&emsp;笛卡尔积构造的新向量空间维数是两个子空间的维数之和。现在我们介绍一种能构造出维数之积的方法：在笛卡尔积的基础上，额外指定这样一些关系：

$$
\begin{aligned}
\alpha(|u\rangle,|v\rangle) & =(\alpha|u\rangle,|v\rangle)=(|u\rangle, \alpha|v\rangle) \\
\left(\alpha_1\left|u_1\right\rangle+\alpha_2\left|u_2\right\rangle,|v\rangle\right) & =\alpha_1\left(\left|u_1\right\rangle,|v\rangle\right)+\alpha_2\left(\left|u_2\right\rangle,|v\rangle\right) \\
\left(|u\rangle, \beta_1\left|v_1\right\rangle+\beta_2\left|v_2\right\rangle\right) & =\beta_1\left(|u\rangle,\left|v_1\right\rangle\right)+\beta_2\left(|u\rangle,\left|v_2\right\rangle\right)
\end{aligned}
$$

这样一种方式将 $\mathcal{U}$ 和 $\mathcal{V}$ 变成了一个新的向量空间 $\mathcal{W} = \mathcal{U}\otimes \mathcal{V}$ ，被称作 $\mathcal{U}$ 和 $\mathcal{V}$ 的*张量积*，并且 $\mathrm{dim}(\mathcal{W}) = \mathrm{dim}(\mathcal{U})\mathrm{dim}(\mathcal{V})$ 。

## 内积空间
&emsp;&emsp;
