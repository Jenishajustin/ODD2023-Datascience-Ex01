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
# OUTPUT
## For Data_set
### DATA
![1d](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/18cfcc53-5aee-4958-b597-6e18a804f2cd)

![2](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/c29adda2-de39-4852-9ab7-79b220c54862)

![3](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/9a46a768-f132-4b50-af24-19ee1d29e63b)

![4](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/13c36bb8-303d-444b-a1d0-adc021ab1f7f)

### MODE
![5](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/8ca67e4f-2246-4797-b891-c8ae17430e7b)

### MEAN
![6](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/dd50e1c1-de67-41bc-b730-abf86331fa9a)

### MEDIAN
![7](https://github.com/Jenishajustin/ODD2023-Datascience-Ex01/assets/119405070/f8fdb598-4950-4aa4-88b3-682167cdf6f7)

# RESULT
Thus, the given data is read, cleansed and the cleaned data is saved into the file.

