# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### Step 1: Start with the Matrix ( A )
Take the square matrix ( A ) (of order ( n )).
Create empty matrices ( L ) (lower triangular) and ( U ) (upper triangular).

### Step 2: Compute Elements of ( L ) and ( U )
For each row ( i ) (from ( 1 ) to ( n )):
Calculate ( Ui][j] ) for ( j \geq i ): [ Ui][j] = Ai][j] - \sum_{k=1}^{i-1} Li][k] \cdot Uk][j] ]
Calculate ( Li][j] ) for ( j < i ): [ Li][j] = \frac{Ai][j] - \sum_{k=1}^{j-1} Li][k] \cdot Uk][j]}{Uj][j]} ]
Diagonal of ( L ): Set ( Li][i] = 1 ).

### Step 3: Loop Through All Rows
Repeat Step 2 for all rows of ( A ) until ( L ) and ( U ) are fully filled.

### Step 4 :
The matrix ( A ) is expressed as ( A = LU ), where:- ( L ) is a lower triangular matrix with ( 1 )s on the diagonal.
( U ) is an upper triangular matrix.

## Program:
```
#Program to find L and U matrix using LU decomposition.
#Developed by: Tharun.V
#RegisterNumber:212224230290

import numpy as np
from scipy.linalg import lu
a = np.array(eval(input()))
p,l,u=lu(a)
print(l)
print(u)
```

# To print X matrix (solution to the equations)
```
#Program to solve a matrix using LU decomposition.
#Developed by: Tharun.V
#RegisterNumber:212224230290

import numpy as np
from scipy.linalg import lu_factor,lu_solve
a=np.array(eval(input()))
b=np.array(eval(input()))
lu,piv=lu_factor(a)
x=lu_solve((lu,piv),b)
print(x)
```


## Output:
![Screenshot 2025-04-22 232318](https://github.com/user-attachments/assets/6a726d10-ea25-4a97-90aa-e92cba46bd70)

![Screenshot 2025-04-22 232422](https://github.com/user-attachments/assets/81e6d9d6-9eb3-45a5-ad59-2a3635519cce)




## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.
