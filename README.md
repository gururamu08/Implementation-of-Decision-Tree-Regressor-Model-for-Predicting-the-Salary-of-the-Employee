# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
### 1.Prepare your data

Collect and clean data on employee salaries and features
Split data into training and testing sets
### 2.Define your model

Use a Decision Tree Regressor to recursively partition data based on input features
Determine maximum depth of tree and other hyperparameters
### 3.Train your model

Fit model to training data
Calculate mean salary value for each subset
### 4.Evaluate your model

Use model to make predictions on testing data
Calculate metrics such as MAE and MSE to evaluate performance
### 5.Tune hyperparameters

Experiment with different hyperparameters to improve performance
### 6.Deploy your model

Use model to make predictions on new data in real-world application. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: GURUMOORTHI R
RegisterNumber:  212222230042
*/
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
x.head()

y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

## Output:
### Initial dataset:



### Data Info:

![image](https://github.com/gururamu08/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707009/0f1161ad-28b4-497f-8464-c7ac3c911fa7)


### Optimization of null values:

![image](https://github.com/gururamu08/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707009/7a6ec797-a97e-4f10-9927-1b07f2813ae6)


### Converting string literals to numericl values using label encoder:


![image](https://github.com/gururamu08/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707009/7297ea17-1d25-42ab-b68c-9dd342029d35)

### Assigning x and y values:

![image](https://github.com/gururamu08/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707009/b7bcd6e7-fdbc-40d6-8f5b-0af217d5026c)

### Mean Squared Error:

![image](https://github.com/gururamu08/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707009/c832eaf5-a820-45d3-81e7-4a37dc61e1a2)

### R2 (variance):

![image](https://github.com/gururamu08/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707009/dc89e8a9-643d-4332-92be-771ee771e19c)

### Prediction:

![image](https://github.com/gururamu08/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707009/e90b35af-0253-4ca4-a8b0-cd355d639d75)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
