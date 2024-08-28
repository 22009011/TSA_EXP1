# Ex.No: 01A PLOT A TIME SERIES DATA

###  Developed by: Thanjiyappan k

###  Register No: 212222240108

###  Date:   

# AIM:
To Develop a python program to Plot a time series data of Ev sales.
# ALGORITHM:
1.Import Libraries: Import the necessary libraries like pandas for data manipulation and matplotlib.pyplot for plotting graphs.

2.Load Dataset: Use pandas to read the dataset from the CSV file into a DataFrame.

3.Aggregate Data: Group the data by the "year" column and sum the "value" column to get the total value for each year.

4.Plot Data: Use matplotlib to plot the aggregated data as a time series. Customize the plot with titles, labels, and formatting.

5.Display Graph: Render the plot using plt.show().
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
The Python code successfully plotted the time series data for EV sales, showing the yearly trend. The graph includes labeled axes, a title, and a grid for clarity in visualizing the data.
