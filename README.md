# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy library as np
2. create a matrix.
3. 
4. Get the output and the end the program

## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: BHARATHGANESH.S
RegisterNumber: 22001588

```
```
import numpy as np
import sys
n = int(input())
a = np.zeros((n,n+1))
x = np.zeros(n)
for i in  range (n):
    for j in range(n+1):
        a[i][j] = float(input())
for i in range(n):
    for j in range (i+1, n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
          a[j][k] = a[j][k] - ratio * a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    for j in range(i+1,n):
        x[i] = x[i] - a[i][j]*x[j]
    x[i] = x[i]/a[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]), end = ' ')
  
 ```
## Output:
![output6](https://user-images.githubusercontent.com/119478098/215316271-e1e1fec9-2d08-42f1-a170-28f1744aa3d1.png)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

