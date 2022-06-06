# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.import pandas module and import the required data set.<br/>
2.Find the null values and count them.<br/>
3.Count number of left values.<br/>
4.From sklearn import LabelEncoder to convert string values to numerical values.<br/>
5.From sklearn.model_selection import train_test_split.<br/>
6.Assign the train dataset and test dataset.<br/>
7.From sklearn.tree import DecisionTreeClassifier.<br/>
8.Use criteria as entropy.<br/>
9.From sklearn import metrics.<br/>
10.Find the accuracy of our model and predict the require values.<br/>

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: D.Amarnath Reddy
RegisterNumber:212221240012

import pandas as pd
data = pd.read_csv("Employee.csv")
data.head()
data.info()

data.isnull().sum()

data["left"].value_counts

from sklearn.preprocessing import LabelEncoder
le= LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()

x= data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]

x.head()
y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state = 100)

from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)

y_pred = dt.predict(x_test)
from sklearn import metrics

accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])

*/
```

## Output:


<img width="752" alt="1" src="https://user-images.githubusercontent.com/94165103/172185341-2dc80f5b-74c5-4656-8d9e-845f726e9d21.png">



<img width="757" alt="2" src="https://user-images.githubusercontent.com/94165103/172185387-0cb717ea-d51d-4d54-9894-9f8e0d0e707c.png">


<img width="757" alt="3" src="https://user-images.githubusercontent.com/94165103/172185424-491f9aaa-da99-48bd-9135-13ef3fa4ad1c.png">

<img width="856" alt="4" src="https://user-images.githubusercontent.com/94165103/172185714-fcc1f244-4a58-47cc-9d1f-66cc7a8ca718.png">


<img width="857" alt="5" src="https://user-images.githubusercontent.com/94165103/172185816-bc180b70-9ec0-47f2-b4f8-f641c87795b0.png">


<img width="860" alt="6" src="https://user-images.githubusercontent.com/94165103/172185923-336b7c38-21e6-4dbf-a828-da95b215e374.png">

<img width="858" alt="7" src="https://user-images.githubusercontent.com/94165103/172185981-71243817-fe85-4e05-868c-78c97d0e7d42.png">


<img width="862" alt="8" src="https://user-images.githubusercontent.com/94165103/172186168-6ec4dd20-5e61-44ad-bd7d-fe8821156dd7.png">


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
