# Gaussian Elimination


## AIM:

To write a program to find the solution of a matrix using Gaussian Elimination.


## Equipments Required:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner



## Algorithm

1. Import numpy library using import statement.
2. Import the sys module to use the built-in functions.
3. Get input from the user for number of rows and add it by 1 for number of columns.
4. Using np.zeros() set the matrix as null matrix
5. Using for loop get input from the user for each element in the matrix.
6. Using for loop we can perform the elementary row operations and find the final matrix.
7. Print the values by solving the matrix using for loop with 2 point precision.
8. End the program.


## Program:

```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: VASANTH KUMAR V 
Register Number:  2305002027


import numpy as py
import sys

n=int(input())

a=np.zeros((n,n+1))

x=np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())

for i in range(n):
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k] - ratio *a[i][k]

x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]

for i in range(n):
    print('x%d = %0.2f' %(i,x[i]),end= ' ')

```

## Output:

![WhatsApp Image 2024-05-10 at 11 54 24_ed9ee5f4](https://github.com/vasanth0228/Gaussian/assets/155505264/c76da213-3af6-46e8-b634-deaf994a606e)



## Result:

Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

