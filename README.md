# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.


## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook


## Algorithm
Step 1: Start

Step 2: Get the independent variable X and dependent variable Y.

Step 3: Calculate the mean of the X -values and the mean of the Y -values.

Step 4: Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

Step 5: Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

Step 6: Use the slope m and the y -intercept to form the equation of the line.

Step 7: Obtain the straight line equation Y=mX+b and plot the scatterplot.

Step 8: Stop


## Program:

/*
Program to implement univariate Linear Regression to fit a straight line using least squares.

Developed by: Gobathi P

RegisterNumber: 212222080017
*/


```py
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
denom=0
for i in range(len(x)):
    num+=(x[i] -x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2
m=num/denom
b=y_mean-m*x_mean
print(m,b)
y_prediction=m*x+b
print(y_prediction)
plt.scatter(x,y)
plt.plot(x,y_prediction, color='red')
plt.show()

```


## Output:

### Slope and Y-Intercept
![image](https://github.com/user-attachments/assets/6cfa0a77-9357-4261-8bda-cb71a1e6bf6a)

### Y Predicted
![image](https://github.com/user-attachments/assets/4064a83d-8fa7-4a30-88b7-889e4eb5ad94)

### Graph
![image](https://github.com/user-attachments/assets/c4b4883d-aa96-404f-9b28-6237f511893a)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
