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
```
df=pd.read_csv("/content/Loan_data (1).csv")
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
# OUPUT
### ![image](https://user-images.githubusercontent.com/128350225/227574704-c04940a8-c955-4415-92b3-2648119ff954.png)
## df.head()
### ![image](https://user-images.githubusercontent.com/128350225/227574862-f25b54d9-4693-444e-81a5-fa752529df42.png)
## df.info()
### ![image](https://user-images.githubusercontent.com/128350225/227579055-321c991d-bb59-46d5-863e-898cb6997776.png)
## df.isnull().sum()
### ![image](https://user-images.githubusercontent.com/128350225/227575217-680a7e0f-503c-492f-8c4c-3254e4f58ea1.png)
## Result:
### Hence the given data is read and perform data cleaning and save the cleaned data to a file.
