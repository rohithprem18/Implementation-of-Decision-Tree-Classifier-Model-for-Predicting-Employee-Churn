# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
step 1.Start.

step 2.Import pandas.

step 3. Import Decision tree classifier.

step 4. Fit the data in the model.

step 5. Find the accuracy score.

step 6.Stop.
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: ROHITH PREM S
RegisterNumber:  212223040172

import pandas as pd
data=pd.read_csv("/content/Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
```
```


from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()    #no departments and no left
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

#### data.head()
![Screenshot 2024-04-29 142409](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145917810/e97dc5fc-9b64-431e-8462-5769f5961087)

#### data.info()
![Screenshot 2024-04-29 142427](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145917810/c6f58517-e59f-48b9-aa60-ab33f4206788)

#### isnull() and sum()
![Screenshot 2024-04-29 142435](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145917810/06704ae3-d4b8-46a6-b425-6ee06cf275eb)

#### data value counts()
![Screenshot 2024-04-29 142442](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145917810/08f1ca1b-f240-4e03-9513-72e30a9190b6)

#### data.head() for salary
![Screenshot 2024-04-29 142451](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145917810/1a1b7dfe-3fb9-4c09-8dcc-9ddbdd61b684)

#### x.head()
![Screenshot 2024-04-29 142459](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145917810/6145dd94-434d-48c3-b57c-4c344ffdfe46)

#### accuracy value
![Screenshot 2024-04-29 142507](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145917810/e799065a-0220-4665-b2e3-43cb945b7011)

#### data prediction
![Screenshot 2024-04-29 142519](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145917810/7af9bc3d-e2a9-4acc-96ad-0e7188c6db9e)
```

```

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
