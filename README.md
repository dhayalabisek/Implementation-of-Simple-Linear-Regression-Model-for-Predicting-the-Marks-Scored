# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and create the dataset of hours studied and marks scored.

2.Create and train a Simple Linear Regression model using the dataset.

3.Give the student's study hours as input and predict the marks.

4.Display the predicted marks and plot the regression line.
 
 
 
## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: DHAYAL ABISEK R
RegisterNumber:  212225060061
*/
```
```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Data
X = np.array([1, 2, 3, 4, 5, 6, 7, 8]).reshape(-1, 1)
Y = np.array([35, 40, 50, 55, 60, 65, 70, 80])

# Create Linear Regression model
model = LinearRegression()

# Train the model
model.fit(X, Y)

# Predict marks for a student who studies 6.5 hours
hours = np.array([[6.5]])
predicted_marks = model.predict(hours)

print("Predicted Marks =", predicted_marks[0])

# Plot
plt.scatter(X, Y, color="blue", label="Actual Marks")
plt.plot(X, model.predict(X), color="red", label="Regression Line")

plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Student Marks Prediction")
plt.legend()
plt.show()
```

## Output:
```
Predicted Marks = 69.13690476190476
```
<img width="562" height="455" alt="ex2 out" src="https://github.com/user-attachments/assets/549b404a-9d1c-42c8-b37a-f83cec1ba256" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
