# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the necessary libraries and get input from the user
2. Use nested loops to iterate over each element of the matrix
3. Perfrom Gaussian elimination to solve the system of linear equations.
4. Use back substitution and print the output

## Program:
```python
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: JEECIKASRINA M
RegisterNumber: 23013947

import sys
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][i]==0.0:
        sys.exit("Divide by zero erro")
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```
## Output:
![image](https://github.com/Jeecikasrina23013947/Gaussian/assets/148515300/fa426a4f-d15e-4512-938b-79c421d6c349)
## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

