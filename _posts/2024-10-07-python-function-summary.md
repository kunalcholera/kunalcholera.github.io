---
layout: post
title: Pandas reference sheet - UGBA-88
date: 2024-10-07 20:53 -0700
---

We are using these alias in the reference sheet below

```Python3
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```


# Index
- [pd.read_csv(‘data-file.csv’)](#1)
- [df.isnull().sum()](#2)
- [df = df.dropna()](#3)
- [plt.hist(df['column_name'])](#4)
- [df.shape](#5)
- [df.columns](#6)
- [len(df)](#7)
- [df.dtypes](#8)
- [sns.barplot(data=df['Make'].value_counts(), orient='h')](#9)
- [plt.figure(figsize=(15,10))](#10)
- [plt.show()](#11)
- [df[['X', 'Y']].corr()](#12)
- [plt.pie(category_counts, labels=category_counts.index, autopct='%1.1f%%')](#13)
- [...](#Z)
- [...](#Z)

## 1 
```Python3
pd.read_csv(‘data-file.csv’)
```
# Read a CSV file using pandas into a DataFrame
Read a CSV file using pandas into a DataFrame| This method read_csv() reads the data-file.csv using pandas (pd) and returns a DataFrame object. A DataFrame object is similar to table with rows and columns but with lot more advanced data analysis and capabilities.It takes in the input the name of csv file in either single quotes or double quotes and returns output as DataFrame object (df)


## 2 
```Python3
df.isnull().sum()
```
# Count null values for every column and show total null values per column
Count number of missing values. This method isnull() looks through all the rows and columns in your DataFrame object (df) where there is value missing (null, NaN or NAN) and returns True if there is a missing value and False if not missing .sum() will add up all the missing True values for each columns and rows in your DataFrame. Input is the df object and output is the column name and the count of all null values in that column. If you do df.isnull().sum().sum() you get the total count of all missing (null) values.

## 3 
```Python3
df = df.dropna()
```
# Drop rows with one or more null values
By default, dropna() will drop any row that has at least one null value in any column.

## 4 
```Python3
plt.hist(df['column_name'])
```
# Create a histogram plot
The plt.hist() function in Matplotlib is used to create histograms, it takes in DataFrame an array-like object containing the values to be plotted, you can pass in a name of your column you want to plot the data in the 'column_name'.


## 5 
```Python3
df.shape
```
# Returns the dimensions (rows, columns) of the DataFrame
df.shape returns the dimensions of a DataFrame as a tuple. It provides two values: (The number of rows, The number of columns)

## 6 
```Python3
df.columns
```
# Shows all the columns you have in your DataFrame
df.columns returns an Index object containing the column labels of a DataFrame. This allows you to see the names of all the columns in the DataFrame.

## 7 
```Python3
len(df)
```
# Count the number of rows you have in your DataFrame
 len(df) returns the number of rows in a DataFrame. It provides a quick way to determine how many records or observations are present.

## 8 
```Python3
df.dtypes
```
# Display data type of each column in DataFrame
df.dtypes returns a Series with the data types of each column in a DataFrame. This is useful for understanding the types of data you are working with, such as integers, floats, or objects (strings).

## 9 
```Python3
sns.barplot(data=df['Make'].value_counts(), orient='h')
```
# Draws a horizontal bar plot using Seaborn library
```sns.barplot(data=df['Make'].value_counts(), orient='h')``` uses the Seaborn library to create a horizontal bar plot. Here’s a breakdown of what it does: ```df['Make'].value_counts()```: This counts the occurrences of each unique value in the 'Make' column of the DataFrame df.```sns.barplot(...)```: This creates a bar plot based on the counts, with the counts on the x-axis (since orient='h' specifies a horizontal orientation).

## 10 
```Python3
plt.figure(figsize=(15,10))
```
# Draws a figure with 15 inches wide and 10 inches tall
The line ```plt.figure(figsize=(15,10))``` is used in Matplotlib to create a new figure for plotting with a specified size.
```plt```: Refers to the Matplotlib library alias, which is commonly imported as import matplotlib.pyplot as plt.
```figure(figsize=(15,10))```: Sets the figure size to 15 inches wide and 10 inches tall. This is useful for ensuring that your plots have the desired dimensions, making them clearer and more visually appealing.

## 11 
```Python3
plt.show()
```
# Show all the figures (plots) created
The line ```plt.show()``` in Matplotlib is used to display all the figures that have been created. It renders the plot to the screen, allowing you to view the visualizations you have generated. You typically call ```plt.show()``` after defining your plots, including any titles, labels, or legends. Without this command, the plot may not be displayed, especially in non-interactive environments. Note you would also need to have run ```%matplotlib inline``` which is a magic command used in Jupyter notebooks to enable the inline display of Matplotlib plots. Make sure to run this command at the beginning of your notebook to activate inline plotting.

## 12 
```Python3
df[['X', 'Y']].corr()
```
# Calculate Pearson correlation between X and Y columns of data
code snippet ```df[['X', 'Y']].corr()``` calculates the correlation matrix between the columns X and Y in the DataFrame df. ```df[['X', 'Y']]```: This selects the columns X and Y from the DataFrame. .corr(): This method computes the Pearson correlation coefficients, which measure the linear relationship between the selected columns. The result will be a 2x2 matrix showing the correlation values between X and Y, as well as each column's correlation with itself (which is always 1).

## 13 
```Python3
plt.pie(category_counts, labels=category_counts.index, autopct='%1.1f%%')
```
# Draws a pie chart visualizing proportions of each category
The line plt.pie(category_counts, labels=category_counts.index, autopct='%1.1f%%') creates a pie chart using Matplotlib. Here's a breakdown:

```category_counts```: This should be a Series or array containing the data for the pie chart (e.g., counts of categories).
```labels=category_counts.index```: Sets the labels for each slice of the pie to the index of the category_counts.
```autopct='%1.1f%%'```: Formats the labels to show the percentage with one decimal place.
This generates a pie chart visualizing the proportions of each category. The ```autopct='%1.1f%%'``` parameter in the ```plt.pie()``` function specifies the format for displaying the percentage values on the pie chart slices. %1.1f: This part formats the percentage as a floating-point number with one digit before the decimal and one digit after the decimal point (e.g., 25.0).
%%: This represents the literal percent sign % in the output. So, each slice of the pie will show its percentage with one decimal place, like 25.0%.

## More coming soon... 
```Python3
..
```
# ..
..

