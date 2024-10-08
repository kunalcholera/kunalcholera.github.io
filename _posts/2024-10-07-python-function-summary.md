---
layout: post
title: Python data analysis functions summary (draft)
date: 2024-10-07 20:53 -0700
---

## Pandas
### Read a CSV file using pandas into a dataframe
```Python3
import pandas as pd
df = pd.read_csv(‘data-file.csv’) 
```
This method read_csv() reads the data-file.csv using pandas (pd) into a dataframe object.
A dataframe object is similar to table with rows and columns but with lot more advanced data analysis and capabilities.

### Check how many null values you have in your dataframe and drop 
```Python3
df.isnull().sum()
```
This method isnull() looks through all the rows and columns in your dataframe (df object) and returns True if null and False if not null .sum() will add up all the Null values for each columns in your dataframe.

### Drop rows with one ore more null values
```Python3
df = df.dropna()
```
By default, dropna() will drop any row that has at least one null value in any column.

### Create histograms
```Python3
plt.hist(df['column_you_are_interested_in'])
```
The plt.hist() function in Matplotlib is used to create histograms, it takes in dataframe an array-like object containing the values to be plotted, you can pass in a column of data to it for example..

### ..
```Python3
..
```
..

### ..
```Python3
..
```
..

### ..
```Python3
..
```
..

### ..
```Python3
..
```
..

### ..
```Python3
..
```
..

### ..
```Python3
..
```
..

### ..
```Python3
..
```
..