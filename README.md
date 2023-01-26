# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Step1
Import Pandas library and linear_model from sklearn using import statement.

## Step2
Read the given csv file using read_csv() method.

## Step3
Create two arrays, independent array x with two classes and dependent array y with one class. Find the regression of x and y using linear_model.LinearRegression() method and fit x and y usind .fit() method.

## Step4
Find the coefficients using .coef_ and intercept using .intercept_

## Step5
Predict the liner regression using regr.predict() method and display the result.

## Program:
## Developed by:PRAVEENKUMAR S
## Reg.No: 22004035
```
import pandas as pd
from sklearn import linear_model
df=pd.read_csv("/content/cars (1).csv")
x=df[['Weight','Volume']]
y=df['CO2']
regr=linear_model.LinearRegression()
regr.fit(x,y)
print("Coefficient:",regr.coef_)
print("Intercept:",regr.intercept_)
predictedCO2=regr.predict([[1995,522]])
print("Predicted CO2 emission based on weight and volume",predictedCO2)

```

## Output:
![multivariate](https://user-images.githubusercontent.com/119559827/214857811-cf208a2f-9248-42fe-a439-4f8182c392f9.png)

## Insert your output
```
<br>Coefficient: [0.00755095 0.00780526]
Intercept: 79.69471929115939
Predicted CO2 emission based on weight and volume [98.83320352]
```
## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
