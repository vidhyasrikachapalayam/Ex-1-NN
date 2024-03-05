## ENTER YOUR NAME: VIDHYASRI.K
## ENTER YOUR REGISTER NO: 212222230170
### EX 1 Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
```
```
df=pd.read_csv("/content/Churn_Modelling.csv", index_col="RowNumber")
df
```
```
df.drop(['CustomerId'],axis=1,inplace=True)
df.drop(['Surname'],axis=1,inplace=True)
df.drop('Age',axis=1,inplace=True)
df.drop('Geography',axis=1,inplace=True)
df.drop('Gender',axis=1,inplace=True)
df
```
```
df.isnull().sum()
```
```
df.duplicated()
```
```
df.describe()
```
```
scaler=StandardScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
df1
```
```
x=df1.iloc[:,:-1].values
x
y=df1.iloc[:,-1].values
y
```
```
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_train))
print(x_test)
print(len(x_test))
```


## OUTPUT:
## DATASET
![image](https://github.com/vidhyasrikachapalayam/Ex-1-NN/assets/119477817/186484d9-113c-4555-9523-c125e0c73c7b)
## DROPPING THE UNWANTED DATASET
![image](https://github.com/vidhyasrikachapalayam/Ex-1-NN/assets/119477817/747f5c5b-05f0-4937-8156-68526bd739ff)
## CHECKING NULL VALUES
![image](https://github.com/vidhyasrikachapalayam/Ex-1-NN/assets/119477817/b793d03b-9b80-47b1-b26a-4bf549ea23f3)
## CHECKING FOR DUPLICATION
![image](https://github.com/vidhyasrikachapalayam/Ex-1-NN/assets/119477817/41856813-51f7-4b33-b1e3-4228678524da)
## DESCRIBING THE DATASET
![image](https://github.com/vidhyasrikachapalayam/Ex-1-NN/assets/119477817/748c6ca9-34aa-4485-a23b-e46f38cdb295)
## SCALING THE DATASET
![image](https://github.com/vidhyasrikachapalayam/Ex-1-NN/assets/119477817/a445cef1-d80e-44eb-affb-643feb3a1048)
## X FEATURES
![image](https://github.com/vidhyasrikachapalayam/Ex-1-NN/assets/119477817/aaddde8c-ddbe-4467-be38-447d661a4ab2)
## Y FEATURES
![image](https://github.com/vidhyasrikachapalayam/Ex-1-NN/assets/119477817/95166433-15fd-4bc4-830e-51f70dc352b3)
## SPLITTING THE TRAINING AND TESTING DATASET:
![image](https://github.com/vidhyasrikachapalayam/Ex-1-NN/assets/119477817/c2789f9a-7dfe-4ce9-8a79-2ec7abce89be)

## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


