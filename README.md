# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy library using import statement.
2. import sys library.
3. create a variable n to receive to receive dimention of the matrix.
4.using import n, create a zero matrix 'a' of x(n+1) and a zero row matrix 'x' of n using np.zeros().
5. initiate 1st nested for loop to get values from user and store it in the 'a'  matrix using float(input()).
6. initiate 2nd nested for loop to apply gausian elimination.
7. initiate 3rd nested for loop to calculate the solution of the 'a' matrix using back substitution.
8. display the solution for each variable upto 2 decimals using using loop and print() with '%' operator. 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Hoshini S
RegisterNumber:2305003006
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
        
for i in range(n):
    if a[i][i]==0.0:
        sys.exit("Divide by zero detected!")
        
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]   
    
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')
*/
```

## Output:
![Screenshot 2024-05-23 094038](https://github.com/hoshini2809/Gaussian/assets/170595101/4bbc280b-440f-4eda-bf96-b8a7825efe1d)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

