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
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: I S ISHITA
RegisterNumber:  212224220038
*/
```

```
import numpy as np
import matplotlib.pyplot as plt

# Input data
X = np.array(eval(input("Enter X values (list): ")))
Y = np.array(eval(input("Enter Y values (list): ")))

# Mean of X and Y
X_mean, Y_mean = np.mean(X), np.mean(Y)

# Calculate slope (m) and intercept (b)
num = sum((X - X_mean) * (Y - Y_mean))
denom = sum((X - X_mean)**2)
m = num / denom
b = Y_mean - m * X_mean

# Print results
print("Slope (m) =", m)
print("Intercept (b) =", b)

# Predicted values
Y_pred = m * X + b
print("Predicted Y values:", Y_pred)

# Plot
plt.scatter(X, Y, color='blue', label="Data Points")
X_sorted = np.sort(X)  # sorting ensures line is smooth
plt.plot(X_sorted, m*X_sorted + b, color='red', label="Regression Line")
plt.xlabel("X - Independent Variable")
plt.ylabel("Y - Dependent Variable")
plt.title("Univariate Linear Regression using Least Squares")
plt.legend()
plt.show()

```

## Output:
<img width="1917" height="1148" alt="image" src="https://github.com/user-attachments/assets/00a9aa66-ca6f-4902-b8a2-6586d91b45d4" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
