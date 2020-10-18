---
title: "Covariance Matrix"
excerpt: "Also known as the second central moment is a measurement of the spread."
date: 2020-03-10
category:
- 'Math'
tag:
- 'Statistics'
- 'Basics'
references:
- name: Covariance Matrix @ Wikipedia
  link: https://en.wikipedia.org/wiki/Covariance_matrix
---

> We use Einstein's summation convention.

Covariance of two discrete series $A$ and $B$ is defined as

$$
\text{Cov} ({A,B}) = \sigma_{A,B}^2 = \frac{  (a_i - \bar A) (b_i - \bar B) }{ n- 1 },
$$

where $n$ is the length of the series. The normalization factor is set to $1/(n-1)$ to mitigate the bias for small $n$.

One could show that

$$
\mathrm{Cov}({A,B}) = E( A,B ) - \bar A \bar B.
$$

<div class="notes--info" markdown="1">

At first glance, the square in the definition seems to be only for notation purpose at this point.

Meanwhile, using this idea of the mean of geometric mean, we could easily generalize it to the covariance of three series,

$$
\sigma_{A,B,C}^3 = \frac{ (a_i - \bar A) (b_i - \bar B)(c_i - \bar C) }{ n-1 },
$$

or even arbitrary N series,

$$
\sigma_{A_1, A_2, ..., A_N }^N = \frac{ \sum_{i=1}^{n} \text{ geometric mean of the ith elements to the Nth power }  }{ n-1 }  = \frac{  (a_{1,i} - \bar A_1) \cdots (a_{N,i} - \bar A_{N})}{ n-1 },
$$

which should be called the covariance of all the N series, $\mathrm{Cov} ({A_1, A_2,\cdots, A_N })$.

We do not use these since we could easily build a covariance matrix to indicate all the possible covariances between any two variables.

</div>

For a complete picture of the data, we build a matrix for all the possible combinations of the covariances,

$$
\mathbf{C} = \begin{pmatrix}
\mathrm{Cov} (A_1, A_1) & \mathrm{Cov} (A_1, A_2) \\
\mathrm{Cov} (A_2, A_1) & \mathrm{Cov} (A_2, A_2)
\end{pmatrix}.
$$

For real series, $\mathrm{Cov} (A_2, A_1) = \mathrm{Cov} (A_1, A_2)$.

<div class="notes--info" markdown="1">

The covariance matrix of complex numbers and quaternions is not necessariy symmetric. A more general concept of symmetries is Hermitian.

</div>

Given a dataset $X$,

$$
X = \begin{pmatrix}
\mathbf X_{1} & \mathbf X_{2} & \cdots & \mathbf X_{N}
\end{pmatrix}
$$

where $N$ is the number of features (variables). The covariance matrix is

$$
C_{ij} = \operatorname{Cov}(\mathbf X_i, \mathbf X_j).
$$

The covariance becomes variance when $i=j$.