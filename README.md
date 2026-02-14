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
# DEVELOPED BY : SARAVANAN SHAM PRAKASH
# REGISTRATION NO : 212224230254
import numpy as np
import matplotlib.pyplot as plt

# Preprocessing input data
X = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
Y = np.array([0, 3, 2, 5, 7, 8, 8, 9, 10, 12])

plt.scatter(X, Y)
plt.show()

# Building the model
X_mean = np.mean(X)
Y_mean = np.mean(Y)

num = 0
den = 0

for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean) ** 2

m = num / den
c = Y_mean - m * X_mean

print(m, c)

# Making predictions
Y_pred = m * X + c

# Plotting actual vs predicted
plt.scatter(X, Y)               # Actual data
plt.plot([min(X), max(X)], [min(Y_pred), max(Y_pred)], color='red')  # Predicted line
plt.show()





```
## Output
<img width="832" height="585" alt="image" src="https://github.com/user-attachments/assets/973314f7-ac3d-4603-ac27-7194cb2141e9" />
<img width="777" height="599" alt="image" src="https://github.com/user-attachments/assets/1300a979-6832-4427-8b56-e2b291d32bbe" />



## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
