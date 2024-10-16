## Preliminaries
### Dimension

**Dimensions** (or say physical dimension, differs from dimension in the mathematical sense) expresses how the numerical value of a physical quantity depends on the units you choose to measure it. Or put in simpler words, it's a set of regulations which people use to describe/ compare physical quantities. One can choose a set of fundamental quantities and build other quantities on top of them. 

Quote:
>A formula in physics *must* give a correct result independently of the system of units used.

That means dimensions can only be multiplied/ divided but never added.

We say that an argument in a formula must be *dimensionless*. 

We use the unit of mass, length, and time to define the following:
1. Momentum $\mathbf{p} = m\mathbf{v}$  has dimension $[lt^{-1}m]$
2. Angular momentum $\mathbf{L} = \mathbf{r}\times\mathbf{F}$, has dimension $[l^2t^{-1}m]$
3. Energy $E = 1/2mv^2$, has dimension $[l^2t^{-2}m]$
4. Action $S = \int \mathcal{L}\mathrm{d}t$ with $\mathcal{L}$ having the dimension of energy, has dimension $[l^2t^{-1}m]$
5. Reduced Planck Constant $\hbar = h/2\pi$ has dimension $[l^2t^{-1}m]$

**Exercise 1.1.1**
&emsp;&emsp;The energy has dimension $[l^2t^{-2}m]$, while $RHS = h\nu$ has dimension $[l^2t^{-1}m][t^{-1}] = [l^2t^{-2}m] = LHS$, which means this formula makes sense with respect to dimension.

**Exercise 1.1.2**
&emsp;&emsp;The wavelength simply has the dimension $[l]$, while $RHS = h/p$ has dimension $[l^2t^{-1}m]/[lt^{-1}m] = [l] = LHS$, which means this formula makes sense with respect to dimension.

### Notation
We declare:
1. The conjugate of a complex number $a$ is denoted by $a^*$;
2. the complex number is denoted by $\mathrm{i}$;
3. the inner product $(\cdot, \cdot)$ is anti-linear in the *first* variable, which means

$$
(ax, y) = a^*(x, y)
$$

and 

$$
(x, y) = (y, x)^*
$$

Here we give the **Cauchy-Schwarz inequality**

$$
|(x, y)|^2 \le \left \| x \right \|^2 \left \| y \right \|^2 
$$

Consider some complex-valued functions $f, g$ in space $L^2(\mathbb{R})$, then the inner product is then given by 

$$
(f, g) = \int^{+\infty}_{-\infty}\mathrm{d}^1 x f^*(x)g(x)
$$

We define an **operator** A on a finite-dimensional Hilbert space to be a linear map $\mathcal{H} \rightarrow \mathcal{H}$ and it satisfies:

$$
(A^\dagger(x), y) = (x, A(y))
$$

in which $A^\dagger$ is the adjoint of $A$. 

**Exercise 1.2.1**
<br>
(a)&emsp;&emsp;Operate $LHS$ to an arbitrary inner product:

$$
    \begin{aligned}
        ((\alpha A)^\dagger(x), y) 
            &= (x, (\alpha A)(y))\\
            &= \alpha(x, A(y))\\
            &= \alpha(A^\dagger(x), y)\\
            &= ((\alpha^*A^\dagger)(x), y)
    \end{aligned}
$$

Therefore we have $(\alpha A)^\dagger = \alpha^* A^\dagger$.

(b)&emsp;&emsp;Use a similar method to (a):

$$
    \begin{aligned}
        ((AB)^\dagger(x), y) 
            &= (x, (AB)(y))\\
            &= (x, A(B(y)))\\
            &= (A^\dagger(x), B(y))\\
            &= (B^\dagger(A^\dagger(x)), y)\\
            &= ((B^\dagger A^\dagger)(x), y)
    \end{aligned}
$$

Therefore we'll immediately see that $(AB)^\dagger = B^\dagger A^\dagger$.