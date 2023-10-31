# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas
2.Import Decision tree classifier
3.Fit the data in the model
4.Find the accuracy score

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: LOGESHWARI.P
RegisterNumber:212221230055 
*/
```
```

import pandas as pd
data=pd.read_csv("salary.csv")
data.head()
data.info()
data.isnull().sum()
 from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
data.info()
x=data[["Position","Level" ]]
x.head()
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test= train_test_split(x,y,test_size=0.2,random_state=100)
x_train.shape
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```
## Output:
## df.head()
![277580594-91b9c4a1-fb7c-41a5-aa1e-5f35a14e4cf5](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94211349/07b0f990-fdd9-41ef-89c4-77709da71244)
## df.info()
![277580739-8485e4e9-12d3-4ab8-8506-7e81301bbbb9](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94211349/6669d0f3-0518-44f8-b4fd-378e914e3690)
## df.isnull.sum()
![277581018-c9d7decf-4b46-4ba8-b66f-43c1a45dce8d](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94211349/e3319702-282a-40e8-a253-975f8dc852d6)
## after lable encoding
![277581393-4f3b818a-f717-4a9f-8a78-1f1978a7dc70](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94211349/d5124655-ad21-4104-8e67-8ba13669a4c1)
## x_train.shape
![277582091-e2a522c9-ce29-44e4-93f9-3e78cf025649](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94211349/43dc2337-678f-44d5-89e9-1ebf22bf52b0)
## y_pred
![277582409-4c6fa12e-6f09-4c96-81d6-507774f5d6f0](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94211349/e6a777dc-7524-47d9-82e0-e7b548d3cfe4)
## MSE
![277582522-37997899-18a5-42f0-95ac-5f09ac36420a](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94211349/747cad96-bded-4abe-8a24-4186cb9831dc)
## R2
![277582695-5131da2c-8d49-4599-8d40-0e645acf86c4](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94211349/de780cc7-23fa-472a-b73a-4561e3a3ce5a)
## predicted value
![277582967-8a2fae35-dee2-41e9-89fa-7262f9b31f6d](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94211349/e883f9d6-7b68-4270-af59-906b0b07b89c)
## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
