# Matrix Analysis Using NumPy 
---

## 1️. Library Import Section

import numpy as np
* Imports NumPy, which is used for all numerical and matrix operations such as determinant, rank, eigenvalues and inverse.

from sympy import Matrix
* Imports Matrix from SymPy.

import matplotlib.pyplot as plt
import seaborn as sns
* Libraries for plotting and visualization.

---

## 2️. Personal Matrix Creation

d1 = 3    # last digit of my student ID = 3
d2 = 0    # second last digit of my student ID = 0
```python
A = np.array([[d1+2, d2+1], [2*d1, d2+2]])


python
A = np.array([[5, 1], [6, 2]])

* The same matrix is manually reassigned.

---

## 3️. Analyzing Matrix A

### Shape of Matrix A

python
size_A = A.shape

* Returns the number of rows and columns.

**Output:**

size_A:
 (2, 2)

---

### Determinant of A

python
det_A = np.linalg.det(A)

**Output:**

det_A:
 4.0

---

### Rank of A

python
rank_A = np.linalg.matrix_rank(A)

* Number of linearly independent rows/columns.

**Output:**

rank_A:
 2

---

### Eigenvalues and Eigenvectors of A

python
eigenvalues = np.linalg.eig(A)

* Computes eigenvalues and eigenvectors.

**Output:**

eigenvalues:
 (array([6.37228132, 0.62771868]),
  array([[ 0.58471028, -0.22975292],
         [ 0.81124219,  0.97324899]]))

* First array → eigenvalues
* Second array → eigenvectors

---

### Inverse of A

python
if np.linalg.det(A) != 0:
    inv_A = np.linalg.inv(A)

* Since determinant ≠ 0, inverse exists.



**Output:**

inv_A:
 [[ 0.5  -0.25]
  [-1.5   1.25]]

---

## 4️. Value Changing Experiment (Matrix B)

python
B = np.array([[5, 2], [6, 2]])

* Exactly **one value is changed**:

  * `A[0][1] = 1 → 2` (added +1 to the second element)


---

## 5️. Re-analyzing Matrix B

### Shape of B

pOutput:B = B.shape

**Output:**

size_B:
 (2, 2)

---

### Determinant of B

python
det_B = np.linalg.det(B)

[
|B| = (5×2) − (6×2) = 10 − 12 = −2
]

**Output:**

det_B:
 -2.0

---

### Rank of B

python
rank_B Output:.matrix_rank(B)

**Output:**

rank_B:
 2

---

### Eigenvalues and Eigenvectors of B

python
eigenOutput:.linalg.eig(B)


**Output:**

eigenvalues:
 (array([ 7.27491722, -0.27491722]),
  array([[ 0.75036352, -0.27472113],
         [ 0.66102634,  0.96152395]]))

---

### Inverse of B

python
Output:linalg.inv(B)



**Output:**

inv_B:
 [[-1.   1. ]
  [ 3.  -2.5]]

---

## 5 Comparison & Explanation
Answer the following in your own words:

1. How did the determinant change and why?
Answer: The determinant changed from 4 to -2 because increasing the element at index (0,1) from 1 to 2 increased the product of the off-diagonal elements (bc), which is subtracted from the product of the main diagonal (ad) in the formula (det = ad - bc).

2. Did the rank change? Explain.
Answer: The rank did not change. It remained 2 for both matrix because both A and B have non-zero determinants, so their rows remain linearly independent.

3. did the eigenvalues respond to the value change?
Answer: The eigenvalues shifted from approximately [6.37, 0.63] in Matrix A to [7.27, -0.27] in Matrix B, showing that the characteristic equation changed and one eigenvalue became negative.

4. Is B easier or harder to invert than A? Why?
Answer: Neither is inherently "easier" or "harder" to invert computationally, as both are non-singular 2 \times 2 matrix with non-zero determinants.
`


---
