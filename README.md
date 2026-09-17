# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 15-09-2026

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.

# PROGRAM:

```
# Import necessary libraries
import matplotlib.pyplot as plt
import pandas as pd 
# Step 1: Load Dataset (Example Data)
df=pd.read_csv("/content/Electric_Production.csv")
df.head()
df['DATE']=pd.to_datetime(df['DATE'])
df.dtypes
df.set_index('DATE',inplace=True)

# Step 2: Resampling and interpolating the data
df_resampled = df['IPG2211A2N'].resample('D').interpolate()

# Step 3: Visualize Data 

df_resampled.plot(kind='line',label='Total Sales', color='black')
plt.title('Time Series Plot of Number of passengers ecah day')
plt.xlabel('years')
plt.ylabel('Number of passengers')
plt.legend()
plt.grid(True)
plt.show()
```

# OUTPUT:

<img width="757" height="580" alt="image" src="https://github.com/user-attachments/assets/98bc270f-a9e9-41bc-88d8-9b48208ac755" />





# RESULT:
Thus we have created the python code for plotting the time series of given data.
