# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and read the dataset containing student study hours and scores.

2. Extract the input (Hours) and output (Scores) values, then calculate their mean values.

3. Use a loop to calculate the slope of the regression line using the least squares method.

4. Compute the y-intercept using the slope and the mean values of x and y.

5. Predict the scores using the linear equation and plot both the original data and the regression line.

## Program:
Program to implement the simple linear regression model for predicting the marks scored.

Developed by: D Keerthan

RegisterNumber:  212224240075
```
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd

df=pd.read_csv('/content/student_scores.csv')
x=df['Hours'].values
y=df['Scores'].values

x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
denom=0

for i in range(len(x)):
  num+=(x[i]-x_mean)*(y[i]-y_mean)
  denom+=(x[i]-x_mean)**2

m=num/denom

b = y_mean - m * x_mean

print('Slope: ',m)
print('Y-intercept: ',b)

y_predicted=m*x+b #y = mx + c
print('Predicted values: ',y_predicted)

plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.title('LINEAR REGRESSION GRAPH')
plt.xlabel('Hours Studied')    
plt.ylabel('Scores Obtained')  
plt.show()
```





## Output:
![image](https://github.com/user-attachments/assets/c9823735-2ede-4a97-8572-cd09035650b2)



## Result:
Thus, the program to implement the simple linear regression model for predicting the marks scored is written and verified using Python programming.
