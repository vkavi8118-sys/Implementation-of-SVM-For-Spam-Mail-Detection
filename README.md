# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Detect File Encoding: Use chardet to determine the dataset's encoding.
2.Load Data: Read the dataset with pandas.read_csv using the detected encoding.
3.Inspect Data: Check dataset structure with .info() and missing values with .isnull().sum().
4.Split Data: Extract text (x) and labels (y) and split into training and test sets using train_test_split.
5.Convert Text to Numerical Data: Use CountVectorizer to transform text into a sparse matrix.
6.Train SVM Model: Fit an SVC model on the training data.
7.Predict Labels: Predict test labels using the trained SVM model.
8.Evaluate Model: Calculate and display accuracy with metrics.accuracy_score.

## Program:
```
/*

import chardet
file='spam.csv'
with open(file, 'rb') as rawdata:
    result = chardet.detect (rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv('spam.csv', encoding='Windows-1252')
data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train, x_test, y_train,y_test=train_test_split(x,y,test_size=0.2, random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train, y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

Developed by: Kavinaya V
RegisterNumber: 212225230133 
*/
```

## Output:
<img width="765" height="48" alt="image" src="https://github.com/user-attachments/assets/b0ddccc6-88ff-49c9-9b50-214d9394dc42" />

<img width="447" height="278" alt="image" src="https://github.com/user-attachments/assets/87e0929d-cbbd-41ad-b1e2-cfca2d123b41" />

<img width="220" height="303" alt="image" src="https://github.com/user-attachments/assets/3292314e-81aa-41d6-bbe3-9bc6445c5b00" />
<img width="736" height="93" alt="image" src="https://github.com/user-attachments/assets/235f3db2-4175-4930-b8c7-db6f83a86932" />
<img width="211" height="27" alt="image" src="https://github.com/user-attachments/assets/223a2463-1e4c-4599-b964-fb536079a517" />

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
