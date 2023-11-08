# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

1..Get the matrix from user.

2.Using "from numpy as np" to import numpy.

3.Using numpy library we solve the matrix using gaussian elimination with partial pivoting.

4.Print the result matrices (Gaussian Elimination).

5.End the program. imination).

## Program:
'''Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by:Mahalakshmi.k 
RegisterNumber:212222240057 
'''
import numpy as np
import sys
n = int(input())
a = np.zeros((n,n+1))
X = np.zeros(n)
for i in range(n): 
    for j in range(n+1):
        a[i][j] = float(input())
for i in range(n):
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k]-ratio*a[i][k]
X[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i] = a[i][n]
    for j in range(i+1,n):
        X[i] = X[i]-a[i][j]*X[j]
    X[i] = X[i]/a[i][i]
for i in range(n):
    print('X%d = %.2f'%(i,X[i]),end = ' ')
    

## Output:

![Screenshot (17)](https://github.com/maha712/Gaussian/assets/121156360/cf68d5ba-a8f0-4e36-99e0-e37aa865983c)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

