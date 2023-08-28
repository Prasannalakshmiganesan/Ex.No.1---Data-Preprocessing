# Ex.No.1---Data-Preprocessing
## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

##REQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

Kaggle :
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

Data Preprocessing:

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

Need of Data Preprocessing :

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
Importing the libraries
Importing the dataset
Taking care of missing data
Encoding categorical data
Normalizing the data
Splitting the data into test and train

## PROGRAM:
```
Developed by : G.Prasannalakshmi
Reg no - 212222240075
```
# Importing libraries :
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
```
# Reading the dataset :
```
df=pd.read_csv("/content/Churn_Modelling.csv", index_col="RowNumber")
df
```
# Dropping the unwanted Columns :
```
df.drop(['CustomerId'],axis=1,inplace=True)
df.drop(['Surname'],axis=1,inplace=True)
df.drop('Age',axis=1,inplace=True)
df.drop('Geography',axis=1,inplace=True)
df.drop('Gender',axis=1,inplace=True)
df
```
# Checking for null values :
```
df.isnull().sum()
```
# Checking for duplicate values :
```
df.duplicated()
```
# Describing the dataset :
```
df.describe()
```
# Scaling the dataset :
```
scaler=StandardScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
df1
```
# Allocating X and Y attributes :
```
x=df1.iloc[:,:-1].values
x
y=df1.iloc[:,-1].values
y
```
# Splitting the data into training and testing dataset :
```
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_train))
print(x_test)
print(len(x_test))
```

## OUTPUT:
## The dataset :
![image](https://github.com/Prasannalakshmiganesan/Ex.No.1---Data-Preprocessing/assets/118610231/391cce8d-f388-414d-899a-4752e2648ec5)

## Dropping unwanted features :
![image](https://github.com/Prasannalakshmiganesan/Ex.No.1---Data-Preprocessing/assets/118610231/2bcaef48-5a20-4bb6-b0fd-7e48d106e963)

## Checking for null values :
![image](https://github.com/Prasannalakshmiganesan/Ex.No.1---Data-Preprocessing/assets/118610231/9c21e1be-8ccd-4fd7-a83e-3975c673c1c1)

## Checking for duplication :
![image](https://github.com/Prasannalakshmiganesan/Ex.No.1---Data-Preprocessing/assets/118610231/c9ce2aa0-0a52-4018-9600-364a7ab8ee48)

## Describing the dataset :
![image](https://github.com/Prasannalakshmiganesan/Ex.No.1---Data-Preprocessing/assets/118610231/6cd21fe4-36e0-4ca2-95d5-13062a8e50fe)

## Scaling the values :
![image](https://github.com/Prasannalakshmiganesan/Ex.No.1---Data-Preprocessing/assets/118610231/d9ae5839-2ee0-4dc6-a840-2c95bd101ee2)

## X Features :
![image](https://github.com/Prasannalakshmiganesan/Ex.No.1---Data-Preprocessing/assets/118610231/423295d1-741a-46ee-9bfe-580b74c0632d)

## Y Features :
![image](https://github.com/Prasannalakshmiganesan/Ex.No.1---Data-Preprocessing/assets/118610231/c56f5bf0-f479-43fb-98fb-9632f624f449)

## Splitting the training and testing dataset :
![image](https://github.com/Prasannalakshmiganesan/Ex.No.1---Data-Preprocessing/assets/118610231/ccd3e259-59d5-415a-b880-2ee0c4473368)





## RESULT
Thus we have successfully performed Data preprocessing in a data set downloaded from Kaggle
