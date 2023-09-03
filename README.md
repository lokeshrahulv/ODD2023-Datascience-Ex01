# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE
### LOAN_DATA.CSV
```
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```
### DATA_SET.CSV
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
```
# OUTPUT
### FOR LOAN_DATA:
### DATA
```
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
```
![261767057-e56346b9-5358-4755-9fa9-0731384d7875](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/7d0a4249-7d39-4119-9c20-7bb8d7260328)

### NON NULL BEFORE
```
df.info()
```
![261767356-bcdd59da-892b-4b61-aea5-90c31b7fdff5](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/31d1cb74-3f08-43f6-b824-2d004fc1884f)

### MODE
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![261767382-219a6d74-2cf9-4385-9a10-e2612b3bc28f](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/011b67e0-8452-43a6-a8d2-de43aa149259)

### MEAN
```
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![261767399-326bd78c-ea1c-4502-a090-0c858b90392c](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/8e46652e-d586-4c93-aaff-413416ac3672)

### MEDIAN
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![261767415-ff17ebcb-2b94-4fc1-a3cd-e6de2825a5e4](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/4e89e662-b39a-494c-ba4b-25ad7b31123b)

### NON NULL AFTER
```
df.info()
```
![261767520-8b3d8ad9-670e-4765-b931-fd8f17896b07](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/e38d3aff-e219-4c4f-8d2b-f3926d23eb92)
```
df.isnull().sum()
```
![261767531-bd92664f-5dda-4fb8-a785-24bfe8f23830](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/da0e1945-0801-4fec-948a-77e14254836c)

### FOR DATA_SET:
### DATA
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
```
![261767548-f088086c-bab3-4a3b-a14a-407209394c15](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/0329839d-2c02-4e4b-91f4-f9c0825e497f)

### NON NULL BEFORE
```
df.info()
```
![261767667-19b2df64-70aa-4b25-a0c4-e01864623991](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/e94d3113-1074-47de-9184-2bdd72f62341)
```
df.isnull()
```
![261767769-0ce02807-0898-4881-96e9-c0a05b4c3275](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/7c0569ce-109b-419f-aa1b-ad2a46287cca)
```
df.isnull().sum()
```
![261767803-f82ae558-0de5-4473-9f26-f57036bef55c](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/ce50ab5d-c663-4725-90aa-43e79293a725)

### MODE
```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![261767891-6a6b6c93-f4a9-4839-89a2-8c4e04f03772](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/c5ff4c2a-772a-41e3-86c3-5a1fa37d5cd5)

### MEAN
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![261776919-d45490eb-f685-4b1d-8fbc-f2d9d32188ae](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/0032293e-a24e-43eb-a603-6dd044989e4b)

### MEDIAN
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![261776992-ec53fe34-539b-4abf-8a49-3a0770f1b8b6](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/820ba595-0516-427e-b91e-93b93c630f11)

### NON NULL AFTER
```
df.info()
```
![261777008-f38ef5d5-af1b-4c19-bd5d-14ee0427ac08](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/4abee53c-f0cc-4709-a6a7-e8eb3214eb66)
```
df.isnull()
```
![261777013-4634d6c5-51ab-4972-a742-4b158c40d670](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/620e38f1-0624-46e9-8cd6-103e8afc9140)
```
df.isnull().sum()
```
![261777076-4611191e-159e-4a17-9170-8bdc523d8c93](https://github.com/lokeshrahulv/ODD2023-Datascience-Ex01/assets/118423842/0c962428-71a3-4363-94ab-76d232d83035)

## RESULT
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
