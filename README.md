# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
# Program to implement Linear Regression using Gradient Descent
# Developed by:
# RegisterNumber:

import numpy as np
import matplotlib.pyplot as plt

# Dataset
X = np.array([2.5, 3.0, 3.5, 4.0, 4.5,
              5.0, 5.5, 6.0, 6.5, 7.0])

y = np.array([5.0, 5.5, 6.0, 6.5, 7.0,
              7.5, 8.0, 8.5, 9.0, 9.5])

# Normalize input
X_mean = np.mean(X)
X_std = np.std(X)
X_norm = (X - X_mean) / X_std

# Initialize parameters
m = 0
c = 0
learning_rate = 0.01
iterations = 1000
n = len(X)

# Gradient Descent
for i in range(iterations):

    y_pred = m * X_norm + c

    dm = (-2/n) * np.sum(X_norm * (y - y_pred))
    dc = (-2/n) * np.sum(y - y_pred)

    m = m - learning_rate * dm
    c = c - learning_rate * dc

# Prediction
y_pred = m * X_norm + c

# Calculate cost
cost = np.mean((y - y_pred) ** 2)

print("Slope:", m)
print("Intercept:", c)
print("Mean Squared Error:", cost)

# Plot graph
plt.scatter(X, y, color='blue', label='Actual Data')
plt.plot(X, y_pred, color='red', label='Regression Line')

plt.xlabel("Population")
plt.ylabel("Profit")
plt.title("Linear Regression using Gradient Descent")
plt.legend()
plt.show()

# Predict profit for a new city
population = float(input("Enter population value: "))

population_norm = (population - X_mean) / X_std

predicted_profit = m * population_norm + c

print("Predicted Profit:", predicted_profit)
```
```
/*
Program to implement the linear regression using gradient descent.
Developed by: SACHIN S.B
RegisterNumber:  212225040353
*/
```

## Output:
![linear regression using gradient descent](sam.png)
<img width="1533" height="733" alt="image" src="https://github.com/user-attachments/assets/f9a54aa3-b541-4f5d-842e-5498483b8318" />



## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
