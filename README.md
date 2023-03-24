# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
### import pandas as pd df=pd.read_csv("/content/Data_set.csv") print(df) df.head(5) df.info() df.isnull().sum() df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0]) df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0]) df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0]) df.head() df['rating']=df['rating'].fillna(df['rating'].mean()) df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean()) df.head() df['watchers']=df['watchers'].fillna(df['watchers'].median()) df.head() df.info() df.isnull().sum()
# OUPUT
### ![image](https://user-images.githubusercontent.com/128350225/227574704-c04940a8-c955-4415-92b3-2648119ff954.png)
## df.head()
### ![image](https://user-images.githubusercontent.com/128350225/227574862-f25b54d9-4693-444e-81a5-fa752529df42.png)
## df.info()
### ## df.isnull().sum()
### ![image](https://user-images.githubusercontent.com/128350225/227575217-680a7e0f-503c-492f-8c4c-3254e4f58ea1.png)
## Result:
### Hence the given data is read and perform data cleaning and save the cleaned data to a file.

