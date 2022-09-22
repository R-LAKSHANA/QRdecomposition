# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)

## Program:
### Gram-Schmidt Method
```python
''' 
Program to QR decomposition using the Gram-Schmidt method
Developed by: R LAKSHANA
RegisterNumber: 22004909
'''
import numpy as np
 
def qr(A):   
    u[:,0] = a[:,0]
    e[:,0] = u[:,0]/np.linalg.norm(u[:,0])
    for i in range(1,n):                                                            
        u[:,i] = a[:,i]
        for j in range(i):
            u[:,i] -= (a[:,i]@e[:,j])*e[:,j]
            e[:,i] = u[:,i]/np.linalg.norm(u[:,i])
    return e

def make_householder(a):
    R = np.zeros((n,m))
    for i in range(n):
        for j in range(i,m):
            R[i,j]=a[:,j]@e[:,i]   
    return R
    
a = np.array(eval(input()))
n,m = a.shape
u = np.empty((n,m)) 
e = np.empty((n,m))

q, r =  qr(a), make_householder(a)

print(q.round(8))
print(r.round(8))
```

## Output

![output](/Output.png)

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.