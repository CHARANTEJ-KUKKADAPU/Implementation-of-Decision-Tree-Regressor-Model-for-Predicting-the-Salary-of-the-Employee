# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

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
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: KUKKADAPU CHARAN TEJ
RegisterNumber: 212224040167
*/
```
```py
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
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
## DATA HEAD:
![9 1 ml](https://github.com/user-attachments/assets/c694f6c4-288d-4156-905b-35a67c475039)

## Data Info:
![9 2 ml](https://github.com/user-attachments/assets/ee54f977-cfb2-4ad2-bdbf-767c423cd010)


## isnull() sum():
![9 3 ml](https://github.com/user-attachments/assets/64b9fa1b-5d02-4882-b970-71e2a11df171)


## Data Head for salary:
![9 4 ml](https://github.com/user-attachments/assets/46537c21-6efb-40ea-9d97-68f78418ad6f)


## Mean Squared Error :
![9 5 ml](https://github.com/user-attachments/assets/b59ce9bd-4cae-4638-9ed8-48343611dea5)


## r2 Value:
![9 6 ml](https://github.com/user-attachments/assets/e95785de-d134-47b1-883a-bb0bc2653e7b)


## Data prediction :
![9 7 ml](https://github.com/user-attachments/assets/6f769aae-cf22-41e7-8e54-62fcc2ea6518)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
