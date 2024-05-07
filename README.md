# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree classification in dataset.
4. calculate Accuracy,data prediction.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: T DANUSH REDDY
RegisterNumber: 212223040029

import pandas as pd
data=pd.read_csv("/content/Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company",
          "Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])

 
*/
```

## Output:
![decision tree classifier model](sam.png)
![image](https://github.com/danushreddy7/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149035740/971a6088-5c68-49f2-88af-a9b61d2c316a)
![image](https://github.com/danushreddy7/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149035740/943b83bf-b846-44bb-8f85-5e3002544acd)
![image](https://github.com/danushreddy7/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149035740/0a7bdea7-af01-4a03-8061-7249dd4f53e3)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
