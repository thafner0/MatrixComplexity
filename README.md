# MatrixComplexity

## Motivation

_à quoi sert-il ?_

The idea of this project originated from the discussion in a linear algebra
course about how diagonalisation can make evaluating powers of matrices (i.e.
$[A]^k$) much easier using eigenvectors and eigenvalues. The principle
motivation was the curiosity of _how much_ more efficient is diagonalisation
compared to the 'traditional' method of multiplying the matricies repeatedly
using standard matrix multiplication.

The name of this project was chosen as I am also intrigued about the time
complexities of other matrix operations such as standard matrix multiplications.
At this time (Fall 2025), however, I am focusing specifically on diagonalisation
versus standard matrix multplication.

## Overview on How Diagonalisation Works

Given some matrix $A$ that has eigenvectors and eigenvalues such that a matrix
$P$ is a matrix whose columns consist of the eigenvectors and that a matrix
$D$ is a matrix that is similar to $A$ containing the eigenvectors along a
diagonal. Since each eigenvector has an associated eigenvalue, the eigenvector
in the $i$th column of matrix $P$ corresponds to the eigenvalue in the entry
of matrix $D$ in its $i$th row and $i$th column. The following relation
emerges as a result:
$$
A = PDP^{-1}
$$

This can be expanded to work for $A^k$ as shown below:
$$
A^k = (PDP^{-1})^k = (PDP^{-1})(PDP^{-1})(PDP^{-1})...
$$

Since $P^{-1}P = I$, the above can be simplified to:
$$
A^k = PD^kP^{-1}
$$

The (theoretically) increased efficiency of doing this type of matrix
multiplication using diagonalisation comes from the fact that raising a diagonal
matrix to the $k$th power requires only raising each entry along the diagonal to
the $k$th power and thus doens't require any other products and any addition
that would normally be found with matrix multplication.

## Project Status

This project is currently a work in progress. It will be updated and expanded
upon as time progresses, along with this README.
