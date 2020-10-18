#### 1) Matrix

 is a rectangular array of numbers within square brackets. or this is another way of 2D-array

##### example: 

1) A[3 5 5 6]

here, A i,j = "i,j entry" in the ith row, jth column

Above matrix dimension is R[1x4]



#### 2) Vector

 A vector is a special case of matrix, a vector is a matrix which has only one column.

##### example:

y = [460

​       232

​       315

​       178]

in above example, number of element is 4 

so, this is matrix with 4 elements

so, NX1 Matrix is a vector. Here, N is number of rows and 1 is number of columns

Note: generally, capital letters are used to represent matrix and lower case letters are used to represent vectors.

**Notation and terms**:

- A_{ij}Aij refers to the element in the ith row and jth column of matrix A.
- A vector with 'n' rows is referred to as an 'n'-dimensional vector.
- v_ivi refers to the element in the ith row of the vector.
- In general, all our vectors and matrices will be 1-indexed. Note that for some programming languages, the arrays are 0-indexed.
- Matrices are usually denoted by uppercase names while vectors are lowercase.
- "Scalar" means that an object is a single value, not a vector or matrix.
- \mathbb{R}R refers to the set of scalar real numbers.
- \mathbb{R^n}Rn refers to the set of n-dimensional vectors of real numbers.



#### Matrix Addition

A = [ 1 0

​         2 5

​         3 1]

B = [ 4 0.5

​        2   4 

​         0   1]



A+B = [ 5  0.5

​             4     9

​             3      2]



##### Note:

* Addition and Substraction are element-wise.

*  for addition both the matrix should have same dimension.

C = [ 1 0

​         2  4]

D = [ 4 0.5

​        2   4 

​         0   1]

C +D = compiler error (here, the dimension of matrix C is 2X2 and dimension of matrix D is 3X2)



#### Scalar Multiplication: 

3 x [1  0                 [3   0

​       2   5                 6    15

​       3    1]    =         9     3]

#### Matrix-Vector Multiplication

We map the column of the vector onto each row of the matrix, multiplying each element and summing the result.

The result is a **vector**. The number of **columns** of the matrix must equal the number of **rows** of the vector.

An **m x n matrix** multiplied by an **n x 1 vector** results in an **m x 1 vector**.



#### Matrix Multiplication Properties

- Matrices are not commutative: A∗B≠B∗A
- Matrices are associative: (A∗B)∗C=A∗(B∗C)
- The **identity matrix**, when multiplied by any matrix of the same dimensions, results in the original matrix. It's just like multiplying numbers by 1. The identity matrix simply has 1's on the diagonal (upper left to lower right diagonal) and 0's elsewhere

#### Inverse and Transpose

* The **inverse** of a matrix A is denoted A^{-1}A^{−1}. Multiplying by the inverse results in the identity matrix.

* Matrices that don't have an inverse are *singular* or *degenerate*


# Addition and Scalar Multiplication

Addition and subtraction are **element-wise**, so you simply add or subtract each corresponding element:

[acbd]+[wyxz]=[a+wc+yb+xd+z]

Subtracting Matrices:

[acbd]−[wyxz]=[a−wc−yb−xd−z]

To add or subtract two matrices, their dimensions must be **the same**.

In scalar multiplication, we simply multiply every element by the scalar value:

[acbd]∗x=[a∗xc∗xb∗xd∗x]

In scalar division, we simply divide every element by the scalar value:

[acbd]/x=[a/xc/xb/xd/x]

