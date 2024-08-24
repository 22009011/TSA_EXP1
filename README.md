# Ex.No: 01A PLOT A TIME SERIES DATA

###  Developed by: Thanjiyappan k

###  Register No: 212222240108

###  Date:   

# AIM:
To Develop a python program to Plot a time series data of Ev sales.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Plot the data according to need and can be altered monthly, or yearly.
4. Display the graph.
# PROGRAM:
```py
import pandas as pd
import matplotlib.pyplot as plt


file_path = 'EV.csv'
ev_data = pd.read_csv(file_path)


ev_yearly_data = ev_data.groupby('year')['value'].sum().reset_index()

plt.figure(figsize=(10, 6))
plt.plot(ev_yearly_data['year'], ev_yearly_data['value'], marker='o', linestyle='-', color='b')
plt.title('Global EV Data: Yearly Trend')
plt.xlabel('Year')
plt.ylabel('Value (Aggregated)')
plt.grid(True)
plt.xticks(ev_yearly_data['year'], rotation=45)
plt.tight_layout()
plt.show()

```

# Dataset:
![image](https://github.com/user-attachments/assets/d279cac7-332d-4760-a233-4c78b3b1e9b8)

# OUTPUT:

![image](https://github.com/user-attachments/assets/bd563094-afa4-48dc-9cf0-fc6f3e28f7e7)






# RESULT:
Thus we have created the python code for plotting the time series of given dataset.
