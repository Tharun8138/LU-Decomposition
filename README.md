# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
## step 1:Use LU Decomposition to find L and U matrix.
## step 2:LU Decomposition to solve a matrix.

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
