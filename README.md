# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Step 1: Start and read the number of variables n and the augmented matrix.

Step 2: Perform forward elimination to convert the matrix into upper triangular form.

Step 3: Check the pivot elements; if any diagonal element is zero, stop.

Step 4: Apply back substitution to find the values of variables.

Step 5: Print the solutions and stop.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: LEENA SHREE M
RegisterNumber:212225220056

import sys
n = int(input())
a = []
for i in range(n):
    row = []
    for j in range(n+1):
        row.append(float(input()))
    a.append(row)
x = [0]*n
for i in range(n):
    if a[i][i] == 0:
        sys.exit()
    for j in range(1+i,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k]-ratio*a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    for j in range(i+1,n):
        x[i] = x[i]-a[i][j]*x[j]
    x[i] = x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')
*/
```

## Output:

![WhatsApp Image 2026-03-20 at 2 02 42 PM](https://github.com/user-attachments/assets/9406fad7-2d8e-49f9-80ce-faa3012e2b4d)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

