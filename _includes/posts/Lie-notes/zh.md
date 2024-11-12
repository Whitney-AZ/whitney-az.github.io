## 矩阵李群的定义
&emsp;&emsp;**定义**&emsp;&emsp;*一般线性群*是在某个数域$F$上的所有$n \times n$的可逆矩阵组成的群，记作$\mathrm{GL}(n, F)$。矩阵中的每个元素都在数域$F$中。特别的，实数和复数上的一般线性群分别被记作$\mathrm{GL}(n, \mathbb{R})$和$\mathrm{GL}(n, \mathbb{C})$。

&emsp;&emsp;**定义**&emsp;&emsp;令$M_n(\mathbb{C})$代表所有$n\times n$的复矩阵组成的空间。

&emsp;&emsp;**定义**&emsp;&emsp;令$A_m$代表$M_n(\mathbb{C})$中一个复矩阵的序列。如果随着$m \rightarrow \infty$，$A_m$中的每一个元素都收敛于一个确定的$A$中对应的元素，那么我们称$A_m$收敛至$A$。

&emsp;&emsp;**定义**&emsp;&emsp;一个*矩阵李群* $G$ 是一般线性群的子群，并且需要满足对于 $G$中任意一个收敛的数列 $A_m$，其极限 $A\in G$。

&emsp;&emsp;通过以上定义我们可以发现，$G$实际上是一般线性群的一个闭子集，因此一个矩阵李群实际上也可以被定义为是一般线性群的一个闭子群。比如说实数上的一般线性群 $\mathrm{GL}(n, \mathbb{R})$就是一个矩阵李群，同理复数上的一般线性群 $\mathrm{GL}(n, \mathbb{C})$也是一个矩阵李群。特别的，如果一个一般线性群的行列式为1，那么我们称这个一般线性群为*特殊线性群*，记为 $\mathrm{SL}(n,F)$。当然，所有的特殊线性群也是矩阵李群。


&emsp;&emsp;**定义**&emsp;&emsp;*正交群*是所有实正交矩阵组成的集合，记作 $\mathrm{O}(n)$。所谓正交的矩阵指的是所有组成矩阵的列向量均正交，即
$$
\sum^{n}_{l = 1} A_{lj}A_{lk} = \delta_{jk} 
$$
满足这一性质的矩阵作为坐标变换还能维持 $\mathbb{R}^n$中的内积不变，即
$
\left\langle x, y\right\rangle = \left\langle Ax, Ay\right\rangle
$
。同时正交矩阵还有性质 $A^TA = I$。这一性质还能告诉我们正交矩阵的行列式只可能取 $\pm 1$。如果我们取 $\mathrm{det}A = 1$的部分，那么我们就能得到 *特殊正交群* $\mathrm{SO}(n)$。



