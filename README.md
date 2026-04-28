# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 28.04.2026
### Reg no : 212223240151
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
import matplotlib.pyplot as plt 
import pandas as pd 
import numpy as np 
df = pd.read_csv(r"./AEP_hourly.csv")
df.head()
df.info()
df['Datetime'] = pd.to_datetime(df['Datetime'])
df['decimal_hr'] = [t.hour + t.minute/60 for t in df['Datetime']]
df['Date'] = df['Datetime'].dt.date 
df.head()
plt.plot(df['Date'],df['AEP_MW'], color='red')
plt.xlabel('Year')
plt.ylabel("Mega Watts")
plt.title("Energy Comsumption Over the years")
plt.show()

```


# OUTPUT:
<img width="1146" height="269" alt="image" src="https://github.com/user-attachments/assets/fff71dcb-ae37-448c-a08f-5c0ca05761c3" />

<img width="1165" height="785" alt="image" src="https://github.com/user-attachments/assets/20d86129-9de0-488e-bc24-e8aac840947d" />


# RESULT:
Thus we have created the python code for plotting the time series of given data.
