# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required packages.
2. Import the dataset to operate on.
3. Split the dataset.
4. Predict the required output.
5. End the program.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: M.Harini
RegisterNumber:212222240035  
*/

import chardet
file='/content/s
from sklearn.feature_extraction.text import CountVectorizer #Countervectorizer
pam.csv'
with open(file, 'rb') as rawdata:
     result = chardet.detect(rawdata.read(100000))
     
import pandas as pd
data=pd.read_csv("/content/spam.csv",encoding='Windows-1252')

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer #Countervectorizer
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

```
# Output:

## chardet

![image](https://github.com/Harinimuthu17/Implementation-of-SVM-For-Spam-Mail-Detection/assets/130278614/8a81a671-9bab-473a-a37a-88eaf22edfa5)

## head

![image](https://github.com/Harinimuthu17/Implementation-of-SVM-For-Spam-Mail-Detection/assets/130278614/b059b69c-7e7c-4e2e-9108-fa92ee3abca2)

## info

![image](https://github.com/Harinimuthu17/Implementation-of-SVM-For-Spam-Mail-Detection/assets/130278614/642150d2-20fd-422c-b36c-5f8ef7b1a23d)

## is.null.sum()

![image](https://github.com/Harinimuthu17/Implementation-of-SVM-For-Spam-Mail-Detection/assets/130278614/c5db9bef-4798-4be6-a2ad-d7dfa9a31530)

## y_pred

![image](https://github.com/Harinimuthu17/Implementation-of-SVM-For-Spam-Mail-Detection/assets/130278614/4367605a-6e7e-4be7-8e7e-e80ec7e03239)

## accuracy

![image](https://github.com/Harinimuthu17/Implementation-of-SVM-For-Spam-Mail-Detection/assets/130278614/b8af5622-c0a5-4aac-ac9a-d820135660b6)




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
