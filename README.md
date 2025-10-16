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
import numpy as np
import matplotlib.pyplot as plt
X=np.array([20, 22, 18, 25, 21, 19, 23])
Y=np.array([100, 110, 90, 130, 105, 95, 120])
num=0
deno=0
X_mean=np.mean(X)
Y_mean=np.mean(Y)
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  deno+=(X[i]-X_mean)**2
m=num/deno
b=Y_mean-m*X_mean
print(m,b)
Y_pred=m*X+b
print(Y_pred)

plt.scatter(X,Y,color="red")
plt.plot(X,Y_pred)
plt.show()


```

## Output

<img width="745" height="913" alt="image" src="https://github.com/user-attachments/assets/63178883-a5b3-44bf-bfd9-7fcd7b972814" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
