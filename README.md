# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Program for Univariate linear regression using the least squares method.
#Developed by: Yuvaraj V
#RegisterNumber: 23013769
import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
num+=(x[i]-xmean)*(y[i]-ymean)
den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)
plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```
## Output
![Screenshot 2023-12-29 171132](https://github.com/YuvarajVB/Univariate-Linear-Regression/assets/151488375/1f262ca0-9b77-4526-9bd7-893ee33c27f6)
Graph-1
![Screenshot 2023-12-29 171215](https://github.com/YuvarajVB/Univariate-Linear-Regression/assets/151488375/8c358e55-fc8a-43de-925d-f0697c560c61)
Graph-2
![Screenshot 2023-12-29 171250](https://github.com/YuvarajVB/Univariate-Linear-Regression/assets/151488375/074dbdff-b978-43e0-a79b-80340f370248)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
