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
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_ra
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()

```
# OUPUT

![image](https://user-images.githubusercontent.com/118626456/227699596-82a2134c-d29a-4fbf-bd83-929a017aa80c.png)
![image](https://user-images.githubusercontent.com/118626456/227699607-b3bafabf-64ae-4253-ae09-73073110fb77.png)
![image](https://user-images.githubusercontent.com/118626456/227699616-730d8893-b31d-4b76-9653-98055ae1fcf2.png)
![image](https://user-images.githubusercontent.com/118626456/227699624-bb26ec9f-9430-450d-8423-c793ddc3ae60.png)
![image](https://user-images.githubusercontent.com/118626456/227699630-1c21e380-218b-4052-9286-88fd680b5fa4.png)
![image](https://user-images.githubusercontent.com/118626456/227699648-83b5d6dd-8159-4551-993b-deb8a20db7c3.png)
![image](https://user-images.githubusercontent.com/118626456/227699655-9028b92f-531a-4430-8c4a-284f0313ee59.png)



#RESULT 

Data cleaning for given data was cleaned and saved to file
