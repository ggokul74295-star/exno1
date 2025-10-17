# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import numpy as np
import pandas as pd
dt=pd.read_csv("SAMPLEIDS.csv")
dt
```
![01sS](https://github.com/user-attachments/assets/b9e00162-0893-4e0a-869a-72ff7068e5df)
```
dt.head()
```
![02](https://github.com/user-attachments/assets/7adb359e-7246-431a-9fbf-e5978b8416ab)
```
dt.tail()
```

![03](https://github.com/user-attachments/assets/8bd2f870-2ac0-4f32-ba9a-ac341abd13eb)
```
dt.isnull()
```
![4](https://github.com/user-attachments/assets/b95b5a4a-b46b-4281-9fd6-59f3b3eaade5)
```
dt.isnull()
```
![06](https://github.com/user-attachments/assets/b08e3114-d3b2-44a0-9723-6d388c4e28f3)
```
dt.notnull()
```
![07](https://github.com/user-attachments/assets/7c797369-b3a8-4ee3-883d-d5d55d11a71e)
```
dt.dropna(axis=1)
```
![8](https://github.com/user-attachments/assets/266fa95e-8262-450f-8c0b-a16eca0ae8a7)
```
dt.dropna(axis=0)
```
![9](https://github.com/user-attachments/assets/c3968179-9aac-410a-af15-18d687c80750)
```
dt.fillna(0)
```
![10](https://github.com/user-attachments/assets/cd973d59-5bdd-4a2e-b14a-648be3840e28)
```
dt.fillna(method='ffill')

q1=ir.sepal_width.quantile(0.25)
q3=ir.sepal_width.quantile(0.75)
iqr=q3-q1
rid=ir[((ir.sepal_width<(q1-1.5*iqr))|(ir.sepal_width>(q3+1.5*iqr)))]
rid['sepal_width']
```
![11](https://github.com/user-attachments/assets/ed5e36b7-5a4b-4cc6-a4a1-ee6cafe87ce2)
```
ir=pd.read_csv("iris.csv")
ir
rid=ir[~((ir.sepal_width<(q1-1.5*iqr))|(ir.sepal_width>(q3+1.5*iqr)))]
rid
import scipy.stats as stats
z=np.abs(stats.zscore(ir.sepal_width))
z
```
![12](https://github.com/user-attachments/assets/d912576a-535f-4c84-94ee-69a75617d2b3)





# Result
          <<include your Result here>>
