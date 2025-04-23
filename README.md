# EX 08-Implementation of Decision Tree Classifier Model for Predicting Employee Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.


2.Upload and read the dataset.


3.Check for any null values using the isnull() function.


4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.


5.Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: PRAVEEN.K
RegisterNumber: 212223040152
import pandas as pd

from sklearn.tree import DecisionTreeClassifier, plot_tree

data=pd.read_csv("Employee_EX6.csv")

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

plt.figure(figsize=(18,6))

plot_tree(dt,feature_names=x.columns,class_names=['salary','left'],filled=True)

plt.show()




*/
```

## Output:
![Screenshot 2025-04-23 033008](https://github.com/user-attachments/assets/4e448514-e861-455a-b45a-8cba05ce0a6e)
![Screenshot 2025-04-23 033020](https://github.com/user-attachments/assets/5b7adf7d-1a38-4e5b-9431-7ecbf7740730)
![Screenshot 2025-04-23 033029](https://github.com/user-attachments/assets/7eb61771-cb52-44c4-9667-326b8f0cb2b4)
![Screenshot 2025-04-23 033041](https://github.com/user-attachments/assets/0825f2e2-f096-4f99-8d88-7f12da52ffcc)
![Screenshot 2025-04-23 033055](https://github.com/user-attachments/assets/b5837ea8-26e8-4ac9-887a-fd574fc7c58f)
![Screenshot 2025-04-23 033109](https://github.com/user-attachments/assets/acca8d8f-86ad-499a-92ad-5f1f61c5aa96)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
