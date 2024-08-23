# Ex.No: 01A PLOT A TIME SERIES DATA

###  Developed by: Thanjiyappan k

###  Register No: 212222240108

###  Date:  

# AIM:
To Develop a python program to Plot a time series data of Ev sales.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("EV.csv")
data.head()
data['year']=pd.to_datetime(data['year'])
data.set_index('year',inplace=True)
plt.plot(data.index,data['value'],label='value')
plt.title("Year Wise EV Sales")
plt.xlabel("year")
plt.xticks(rotation=45)
plt.ylabel("value")
plt.grid(True)
plt.legend()
plt.show()
```

# Dataset:
![image](https://github.com/user-attachments/assets/c0372d6d-54d4-42c5-ad03-d47c1490acb9)


# OUTPUT:

![image](https://github.com/user-attachments/assets/2250e440-9195-4e93-bc62-443dff721ef2)







# RESULT:
Thus we have created the python code for plotting the time series of given dataset.
