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
## For Data_set
```
import pandas as pd
df=pd.read_csv("/content/Data_set .csv")
df

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

df.isnull().sum()
```
## For Loan_data
```
import pandas as pd
df=pd.read_csv("/content/Loan_Data.csv")
print(df)

df.head(5)

df.info()

df.isnull()

df.isnull().sum()

df['Loan_ID']=df['Loan_ID'].fillna(df['Education'].mode()[0])
df['Education']=df['Education'].fillna(df['Education'].mode()[0])
df['Married']=df['Married'].fillna(df['Education'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df.head()

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.head()

df.info()

df.isnull().sum()
```
# OUTPUT
## For Data_set
### DATA
![1d](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/18cfcc53-5aee-4958-b597-6e18a804f2cd)

![2](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/c29adda2-de39-4852-9ab7-79b220c54862)

![3](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/9a46a768-f132-4b50-af24-19ee1d29e63b)

![4](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/13c36bb8-303d-444b-a1d0-adc021ab1f7f)

### NON NULL BEFORE
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/8f5fdb9b-229a-43b0-8908-9931dd695a6d)

![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/b0ec2878-bfb1-468d-a038-707d29e82d81)

![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/add988e3-0e02-4d0f-ba53-bbdfc9f1dd0d)

### MODE
![5](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/8ca67e4f-2246-4797-b891-c8ae17430e7b)

### MEAN
![6](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/dd50e1c1-de67-41bc-b730-abf86331fa9a)

### MEDIAN
![7](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/f8fdb598-4950-4aa4-88b3-682167cdf6f7)

### NON NULL AFTER
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/5816a0ee-aa3f-4814-96c5-e7d223c702ef)

## For Loan_data
### DATA
![8](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/70672e50-03a4-4efc-94c9-89a2899aa268)

![9](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/05d5703a-f01b-452f-9cdf-0530d2fc525a)

### NON NULL BEFORE
![10](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/b911a713-9014-4092-9cf1-cd25aa7d5c93)

![11](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/8992e3e3-6e1a-49b0-a39b-28c2df1b2d1f)

![12](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/040d26bb-0131-4e47-bdbf-6b162d354201)

### MODE
![13](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/0bb3e484-7514-4b3c-a042-52d7c74bee9c)

### MEAN
![14](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/13d366f0-3124-474b-b339-9cad1f8497c4)

### MEDIAN
![15](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/46a3201a-7e13-4a48-aea0-49cab17bf24e)

### NON NULL AFTER
![16](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/c616344e-814c-4c41-99ae-6cf0d45bae73)

# RESULT
Thus, the given data is read, cleansed and the cleaned data is saved into the file.

