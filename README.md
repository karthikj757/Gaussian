# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```python
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: 
RegisterNumber: 
*/
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range (n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')

```

## Output:

<img width="1444" height="543" alt="Screenshot 2026-02-12 083114" src="https://github.com/user-attachments/assets/0dccc3e1-d461-4481-8ebf-bf03370d4c80" />
<img width="1258" height="669" alt="Screenshot 2026-02-12 083137" src="https://github.com/user-attachments/assets/b8d308c2-1a8a-4959-a42f-7ed03977f7f5" />
<img width="1257" height="599" alt="Screenshot 2026-02-12 083153" src="https://github.com/user-attachments/assets/90a46d35-ccc3-4118-a0ad-952aaf176fbd" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

