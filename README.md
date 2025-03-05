# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: NAVEEN G
RegisterNumber:  212223220066

import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
X_mean = np.mean(X)
Y_mean = np.mean(Y)
print(X_mean)
print(Y_mean)
num, denum = 0,0
for i in range (len(X)):
    num += (X[i]-X_mean)*(Y[i]-Y_mean)
    denum += (X[i]-X_mean)**2
m = num/denum
c = Y_mean - m*X_mean
print(m)
print(c)
Y_predicted = m*X+c
plt.scatter(X,Y)
plt.plot(X,Y_predicted,color='black')
plt.show()
```

## Output:
![418078262-7054a525-19f3-4625-ac26-11a9fcd1bf88](https://github.com/user-attachments/assets/4f285766-0ced-48fe-9d1e-71de066d0722)




![418077455-fd2c94e7-919b-48fc-a98f-bb5ea144d882](https://github.com/user-attachments/assets/8253c5d9-502c-4894-95c8-1aedc740c06a)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
