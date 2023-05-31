# Ex-08-Data-Visualization-

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
### Developed by: Sandhiya R 
### Register number:21222230129
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
tips

tips.head()

tips.info()

# Which day of the week has the highest total bill amount?

sns.barplot(x='day',y='total_bill',data=tips)
plt.title("Weekly highest total bill amount")

# What is the average tip amount given by smokers and non-smokers?

sns.barplot(x='smoker',y='tip',data=tips, palette='rainbow')
plt.title("Average tip amount given by smokers and non-smokers")

# How does the tip percentage vary based on the size of the dining party?

sns.boxplot(x='size', y='tip',data=tips)
plt.title("Tip percentage based on the sizes of the dining party")

# Which gender tends to leave higher tips?

sns.boxplot(x='sex', y='tip',data=tips)
plt.title("Higher tips based on gender")

# Is there any relationship between the total bill amount and the day of the week?

plt.plot(tips['day'],tips['total_bill'])
plt.title("Relationship between the total bill amount and the day of the week")
plt.show()

# How does the distribution of total bill amounts vary across different time periods (lunch vs. dinner)?

sns.violinplot(x='time',y='total_bill',data=tips)
plt.title("Distribution of total bill amounts vary across different time periods(lunch vs. dinner)")

# Which dining party size group tends to have the highest average total bill amount?

sns.barplot(x='size',y='total_bill',data=tips)
plt.title("Highest average total bill amount based party size")

# What is the distribution of tip amounts for each day of the week?

sns.boxplot(x='day',y='total_bill',data=tips)
plt.title("Distribution of tip amounts for each day of the week")

# How does the tip amount vary based on the type of service (lunch vs. dinner)?

sns.violinplot(x='time',y='tip',data=tips)
plt.title("Tip based on the type of service ")

# Is there any correlation between the total bill amount and the tip amount?

sns.scatterplot(data=tips, x='total_bill', y='tip')
correlation_coefficient = tips['total_bill'].corr(tips['tip'])
print("Correlation Coefficient:", correlation_coefficient)
# heatmap
tips.corr()
plt.subplots(figsize=(7,5))
sns.heatmap(tips.corr(),annot=True)
```


# OUPUT
### dataset
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/28593b17-0dba-4589-b9ec-718bcda4d79a)

### tips.head()
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/1223b6bf-d460-4128-8b18-e2333eff3b3a)
### tips.info()
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/682a7c3e-0ce7-42c7-a381-21575df45c98)
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/86be5204-f9bd-4ca6-92f5-e3e82a58aade)
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/dc2deec7-ba35-439a-b8d4-220f449df08f)
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/0ad3bbfa-cb40-43cb-9b72-5fddf526f2a6)
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/9e62a748-6f84-4cba-bad2-a7d86ffdceac)
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/691ed07c-f2ad-4a9e-84c5-c69d468f3c6d)
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/9b6bfe23-d25e-4144-ad04-be8efbf3bd00)
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/68157a59-dc3d-4809-9c8a-875153b001c2)
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/b80d5848-dccc-4068-a06c-ef3bcbb7dea8)
![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/280e9551-6bc3-4474-985b-87636575cbf6)
![Uploading image.png…]()

![image](https://github.com/SandhiyaR1/Ex-08-Data-Visualization_1/assets/113497571/eb04fc8c-a521-4c9e-b4e1-07282ee6ba56)
# RESULT:
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully based on tips dataset and the data is saved to file.

