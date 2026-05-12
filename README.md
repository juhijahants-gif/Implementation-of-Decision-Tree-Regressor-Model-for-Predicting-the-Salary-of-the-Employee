# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries (pandas, sklearn).

2.Load the dataset using read_csv().

3.Select input features (X) and target (y).

4.Split data into training and testing sets.

5.Train Decision Tree model and predict sala 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: JUHI JAHAN T S
RegisterNumber: 212225100020 
*/
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.tree import DecisionTreeRegressor
dataset = pd.read_csv(r"C:\Users\acer\Downloads\Salary.csv")
X = dataset.iloc[:, 1:2].values
y = dataset.iloc[:, 2].values
regressor = DecisionTreeRegressor(random_state=0)
regressor.fit(X, y)
salary_pred = regressor.predict([[6.5]])
print("Predicted Salary:", salary_pred)
X_grid = np.arange(min(X), max(X), 0.01)
X_grid = X_grid.reshape((len(X_grid), 1))

plt.scatter(X, y, color='red')
plt.plot(X_grid, regressor.predict(X_grid), color='blue')
plt.title('Decision Tree Regression')
plt.xlabel('Position Level')
plt.ylabel('Salary')
plt.show()
```

## Output:
<img width="762" height="615" alt="WhatsApp Image 2026-05-12 at 7 04 56 PM" src="https://github.com/user-attachments/assets/6012350e-6a0b-4275-929e-f0c49178c5d3" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
