# Ex03-Univariate-Analysis

# Aim
To read the given data and perform the univariate analysis with different types of plots.
 
# Explanation
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
    
# Algorithm

## Step1
Read the given data.
    
## Step2
Get the information about the data.
    
## Step3
Remove the null values from the data.

## Step4
Mention the datatypes from the data.
    
## Step5
Count the values from the data.
    
## Step6
Do plots like boxplots,countplot,distribution plot,histogram plot.
    
# Program
```
Developed by : M Vignesh
Registration Number : 212220233002
```
```
import numpy as np
import pandas as pd
import io
from scipy import stats
import seaborn as sns

from google.colab import files
uploaded = files.upload()

df = pd.read_csv(io.BytesIO(uploaded['SuperStore.csv']))
print(df)

df.info()
df.describe()
df.isnull()
df.isnull().sum()
df['Postal Code'] = df['Postal Code'].fillna(df['Postal Code'].mode()[0])
df.isnull().sum()
df.dtypes
df['Postal Code'].value_counts()
df.skew()
df.kurtosis()
sns.boxplot(x='Postal Code', data=df)
sns.countplot(x='Postal Code',data=df)
sns.distplot(df["Postal Code"])
sns.histplot(x='Postal Code',data=df)
```

# Output

DATA INFORMATION

![1](https://user-images.githubusercontent.com/53014593/192564539-43f7a2b4-0851-4c45-a0a7-1ffb32c35bac.png)

DATA'S DATATYPES

![2](https://user-images.githubusercontent.com/53014593/192564689-616669dc-a53c-4883-b776-988d758d9d57.png)

BOXPLOT

![3](https://user-images.githubusercontent.com/53014593/192564853-6ca96a1c-38c6-4d0e-8578-5d218c7b6186.png)


COUNTPLOT

![4](https://user-images.githubusercontent.com/53014593/192564909-24601dff-e7c9-4161-96f7-576f17944584.png)

DISTRIBUTION PLOT

![5](https://user-images.githubusercontent.com/53014593/192564985-48d9f1c0-73d8-4a40-85c1-ed46d3259d59.png)

HISTOGRAM PLOT

![6](https://user-images.githubusercontent.com/53014593/192565054-5fd83588-e99b-4c8d-8160-2282f82eab51.png)

# Result
Thus we have read the given data and performed the univariate analysis with different types of plots.





    
