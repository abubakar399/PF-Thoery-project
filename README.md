## Data Loading
import pandas as pd
df = pd.read_csv("data.csv")
df.columns
## Data Cleaning
df.dropna()
df.dropna(inplace=True)
## Data Fetching
df.head(3)
## Data Duplications
df.duplicated()
pd.set_option("display.max_rows",None)
pd.set_option("display.max_columns",None)
df.duplicated()
## Adding new coloum 
df['coloum']=9
df
## Removing coloum 
df.drop(columns=['coloum'],inplace=True)
df
## Shape of the data
df.shape
## View the bottom rows
df.tail(3)
## Random sample
df.sample(3)
## Renaming Columns
df.columns
df.rename(columns={"Age at Marriage":"Marriage Age","Education level":"Educational qualifications"})
df.head(2)
## Data Information
df.info()
## Statistical Analysis
df.describe()
a = df.describe(include="all")
## Data Slicing
a.loc[["max","mean"]]
a.iloc[[0,8]]
df[2:5]
df[2:6:1]
pd.set_option('display.max_rows',None)
pd.set_option('display.max_columns',None)
df[["Caste/Religion","Children"]]
## Mean, Mode, Median
df["Income Level (INR per month)"].mean()
df["Income Level (INR per month)"].mode()
df["Income Level (INR per month)"].median()
df["Caste/Religion"].value_counts()
## Plots (Visualization)
import matplotlib.pyplot as plt
## Bar Plot
df['Caste/Religion'].value_counts().plot(kind="bar",title="Caste/Religion",color="green")
## Histogram
df['Caste/Religion'].value_counts().plot(kind="hist",title="Caste/Religion",color="green")
## Line bar
df['Caste/Religion'].value_counts().plot(kind="line",title="Caste/Religion",color="green")
## Horizontal Bar Plot
df['Caste/Religion'].value_counts().plot(kind="barh",title="Caste/Religion",color="green")
## Pie Chart
df['Caste/Religion'].value_counts().plot(kind="pie",title="Caste/Religion",color="green")
df['Income Level (INR per month)'].plot(kind="hist", title="Histogram of Values",  color="green",)
## Scatter Plot
df.plot.scatter(x="Income Level (INR per month)", y="Caste/Religion", title="Scatter Plot Example", color="green",)
## Density Plot (KDE)
df['Income Level (INR per month)'].plot(kind="kde", title="Density Plot Example", color="green")
## Box Plot
df[['Caste/Religion', 'Income Level (INR per month)']].plot(kind="box", title="Box Plot Example", figsize=(8, 5))
## Finding Null Values
df.isnull().sum()
## Finding Rows by Null Values
df[df["Income Level (INR per month)"].isnull()]
## Filling Null Values
df["final_Income Level (INR per month)"] = df["Income Level (INR per month)"].fillna(df["Income Level (INR per month)"].mean())
df[df["Income Level (INR per month)"].isnull()]
## Group By Relationships
df.groupby("Caste/Religion").describe()
df.to_csv("data2.csv")
df = pd.read_csv("data.csv")
df
df.to_excel("newdata.xlsx", sheet_name="newsheet")
pip install openpyxl# PF-Thoery-project
