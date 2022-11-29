# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import dataset and print dataset info

2.check for null value

3.Map numerical values for salary feature

4.Assign x and y values

5.Split the dataset into train and test sets

6.Import decisiontree classifier and fit it in the dataset

7.Find accuracy and predict values

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Akalya A
RegisterNumber:  212220220002
##program##
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
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=10)
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

![6 1](https://user-images.githubusercontent.com/114275126/204464674-c6d01727-f4f2-4799-86cb-31a888ad7598.PNG)

![6 2](https://user-images.githubusercontent.com/114275126/204464692-25eaaca7-5cc3-40f4-991e-5fb7296dbd62.PNG)

![6 3](https://user-images.githubusercontent.com/114275126/204464725-bfa65e19-be36-4277-8fe4-00f355b568d6.PNG)

![6 4](https://user-images.githubusercontent.com/114275126/204464862-0d7e1b7d-a595-4a89-908f-add4955b01b2.PNG)

![6 5](https://user-images.githubusercontent.com/114275126/204464900-d1ae2379-572e-4557-bd0f-be9310d9329d.PNG)

![6 6](https://user-images.githubusercontent.com/114275126/204464937-1431f318-eeb7-4368-8e69-b769eb9c5125.PNG)

![6 7](https://user-images.githubusercontent.com/114275126/204464980-ab27f37a-cae1-4ddc-8fa5-9847ac1d5e50.PNG)

![6 8](https://user-images.githubusercontent.com/114275126/204465037-22ee74da-8b70-422d-aa37-65800834c875.PNG)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
