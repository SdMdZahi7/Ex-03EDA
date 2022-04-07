# Ex-03EDA

## AIM
To perform EDA on the given data set. 

# Explanation
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 

# ALGORITHM
### STEP 1
Import libraries and load dataset.
### STEP 2
Check for missing values.
### STEP 3
Visualizing the missing values.
### STEP 4
Replacing the missing values.
### STEP 5
Asking Analytical Questions and Visualizations.
### STEP 6
Positive Correlation.
### STEP 7
Negative Correlation.

# CODE
~~~
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("")
df.info()
df.head()
df.isnull().sum()
df.drop("Cabin",axis=1,inplace=True)
df.info()
df.isnull().sum()
df["Age"]=df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull().sum()
df["Embarked"]=df["Embarked"].fillna(df["Embarked"].mode()[0])
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
sns.countplot(x="Survived",data=df)
sns.countplot(x="Pclass",data=df)
sns.countplot(x="Sex",data=df)
df.info()

sns.displot(df["Fare"])
sns.countplot(x="Pclass",hue="Survived",data=df)
sns.displot(df[df["Survived"]==0]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Sex"],df["Survived"])
df.corr()
sns.heatmap(df.corr(),annot=True)
~~~
# OUPUT
# Reading the data
![output](ot1.png)
# Checking the Null values:
![output](ot2.png)
![output](ot3.png)
![output](ot4.png)
# Null values with outliers:
![output](ot5.png)
![output](ot6.png)
# Replacing Null values:
![output](ot7.png)
![output](ot8.png)
![output](ot9.png)
# Plotting graphs:
![output](ot10.png)
![output](ot11.png)
![output](ot12.png)
# After Replacing the Null values:
![output](ot13.png)
![output](ot14.png)
![output](ot15.png)
![output](ot16.png)
![output](ot17.png)
![output](ot18.png)
# Correlation data set:
![output](19.png)
# Heat map:
![output](ot20.png)
# RESULT
Thus the performing of EDA on the given data set(titanic_dataset.csv) is sucessfully done
