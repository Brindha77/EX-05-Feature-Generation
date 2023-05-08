# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file
## PROGRAM:
Devloped by: R BRINDHA
Register No.: 212222230023

# CODE
# Encoding Data.csv
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
# Data.csv
```
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
# Titanic_dataset.csv
```
df2 = pd.read_csv("titanic_dataset.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Sex'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])
df2
```
# OUPUT
# Encoding Data.csv
![G1](https://user-images.githubusercontent.com/118889143/236739976-9ba66582-464f-417d-a3c1-a9c33c074895.png)

![G2](https://user-images.githubusercontent.com/118889143/236740007-148f49a1-ad85-4975-82bf-0e398a99bf43.png)

![G3](https://user-images.githubusercontent.com/118889143/236740052-6ab3591b-93d1-4df3-b4bc-ce4929bb7108.png)
 
![G4](https://user-images.githubusercontent.com/118889143/236740117-2d4cd807-1493-4061-af14-71d8f42264ee.png)

![G5](https://user-images.githubusercontent.com/118889143/236740149-60b2fefb-b3ae-4fde-b9c2-42a765622958.png)

# data.csv
![G6](https://user-images.githubusercontent.com/118889143/236740183-81ae711e-c9cb-40e9-af65-7d66c4777a07.png)

![G7](https://user-images.githubusercontent.com/118889143/236740223-11a5a239-9cb1-47c5-b300-68ff1a76a586.png)

![G8](https://user-images.githubusercontent.com/118889143/236740240-fc8487f6-15f9-4d28-b793-9cfde4b4079a.png)

![G9](https://user-images.githubusercontent.com/118889143/236740279-c3c2810c-6d1b-45b1-b9e1-c5186ba44fcd.png)

![G10](https://user-images.githubusercontent.com/118889143/236740368-9c3b4177-ef2a-45cf-b2e9-9f6640b65772.png)

![G11](https://user-images.githubusercontent.com/118889143/236740401-6d68e45f-19c1-4ffc-9063-5c38807baef9.png)

![G12](https://user-images.githubusercontent.com/118889143/236740439-9882c104-aee7-4681-9fee-0cbd60a0cd0d.png)

# titanic_dataset.csv
![G13](https://user-images.githubusercontent.com/118889143/236740469-68785f1d-b26c-40a1-988c-ad0e4f5963df.png)

![G14](https://user-images.githubusercontent.com/118889143/236740509-c4352cf0-19a7-4639-8422-cd90a651ff92.png)

![G15](https://user-images.githubusercontent.com/118889143/236740571-dc5f7dc7-c488-49c5-8bd9-df6b71d3cf04.png)

# RESULT:
The Feature Generation process was performed and saved the data to a file.
