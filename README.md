# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 Include the necessary coding and corresponding screenshots
 import seaborn as sns
import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

x = [1, 2, 3, 4, 5]

y = [3, 6, 2, 7, 1]

sns.lineplot(x=x,y=y)

![image](https://github.com/user-attachments/assets/7ad152e5-65ee-4178-8349-d738568c68d9)

df = sns.load_dataset("tips")

df

![image](https://github.com/user-attachments/assets/4a1205c5-9bd6-40c0-b375-ca3efef115cb)

sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")

![image](https://github.com/user-attachments/assets/9e8c9779-afcb-4f43-b49c-b7342622b4e5)

x=[1, 2, 3, 4, 5]

y1=[3, 5, 2, 6, 1]

y2=[1, 6, 4, 3, 8]

y3=[5, 2, 7, 1, 4]

sns.lineplot(x=x, y=y1)

sns.lineplot(x=x, y=y2)

sns.lineplot(x=x, y=y3)

plt.title("Multi-Line Plot")

plt.xlabel('X Label')

plt.ylabel("Y Label")

![image](https://github.com/user-attachments/assets/6bfbc9bb-d17d-4715-8411-d57e00d230cd)

tips=sns.load_dataset('tips')

avg_total_bill = tips.groupby('day')['total_bill'].mean()

avg_tip = tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8, 6))

p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')

p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')

plt.xlabel('Day of the Week')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Day')

plt.legend()

![image](https://github.com/user-attachments/assets/003414e4-54cf-4e0a-ad3e-13b9ae8b9c73)

avg_total_bill = tips.groupby('time')['total_bill'].mean() 

avg_tip=tips.groupby('time') ['tip'].mean()

p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)

p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)

![image](https://github.com/user-attachments/assets/4e16ce22-fbfb-46f7-99f6-c4b40164d787)

years=range(2000, 2012)

apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 

oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]

plt.bar(years, apples)

plt.bar(years, oranges, bottom=apples)

![image](https://github.com/user-attachments/assets/d88efcbd-db66-45ab-b328-c94b46e2106c)

import seaborn as sns

dt= sns.load_dataset('tips')

sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')

plt.xlabel('Day of the Week')

plt.ylabel("Total Bill")

plt.title('Total Bill by Day and Gender')

![image](https://github.com/user-attachments/assets/9ffdff0e-aeb2-4ad2-8a9d-1c54ab0ab0ba)

tit=pd.read_csv("/content/titanic_dataset (1).csv")

tit

![image](https://github.com/user-attachments/assets/ce5774f1-7b18-4172-a350-7c9f79311e40)

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 

plt.title("Fare of Passenger by Embarked Town")

![image](https://github.com/user-attachments/assets/cf4f389b-2db3-4e9c-9bce-472f17b4da9b)

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 

plt.title("Fare of Passenger by Embarked Town, Divided by Class")

![image](https://github.com/user-attachments/assets/631b0285-ffc6-49eb-89ae-6cb1d7323152)

tips=sns.load_dataset('tips')

sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)

plt.xlabel('Total Bill')

plt.ylabel("Tip Amount")

plt.title('Scatter Plot of Total Bill vs. Tip Amount')

![image](https://github.com/user-attachments/assets/b4785d3e-67e9-4e1f-8214-f9f76946c7dd)

num_var = np.random.randn(1000)

num_var=pd.Series(num_var, name = "Numerical variable")

num_var

![image](https://github.com/user-attachments/assets/9a9fde5e-6b25-431f-8421-29f844d7afa0)

sns.histplot(data = num_var, kde = True)

![image](https://github.com/user-attachments/assets/7d33cbe3-1df0-44c2-a408-1cb979915434)

df=pd.read_csv("/content/titanic_dataset (1).csv")

sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)

![image](https://github.com/user-attachments/assets/816e83df-28c3-4b53-b0b5-1467080b5f19)

tips=sns.load_dataset('tips')

sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])

![image](https://github.com/user-attachments/assets/4edc4628-1fb8-4da1-8879-f5f96f545798)

sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},

whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})

![image](https://github.com/user-attachments/assets/b443913d-75ba-4a44-82e7-5038ae1511b9)

sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")

plt.xlabel("Day of the Week")

plt.ylabel("Total Bill")

plt.title("Violin Plot of Total Bill by Day and Smoker Status")

![image](https://github.com/user-attachments/assets/17aa34e6-33fe-41ad-a0ce-bfb54fa1799c)

mart=pd.read_csv("/content/titanic_dataset (1).csv")

mart

![image](https://github.com/user-attachments/assets/428fe084-cbc9-4f9a-b190-cf774cc326bf)

sns.kdeplot(data=mart,x='PassengerId')

![image](https://github.com/user-attachments/assets/7ab88c42-6bdb-4cb1-88d6-0549111fd5e8)


sns.kdeplot(data=mart,x='Age')

![image](https://github.com/user-attachments/assets/3beab84f-1802-4487-b40e-77e2dcd0754a)

sns.kdeplot(data=mart)

![image](https://github.com/user-attachments/assets/3bfcf7c7-adc8-4b01-bd72-73ca88671567)

sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')

![image](https://github.com/user-attachments/assets/5464bec1-1281-47ac-9406-63bfb4951193)

sns.kdeplot(data=mart,x='PassengerId',y='Survived')

![image](https://github.com/user-attachments/assets/16acb0f0-f3bc-4f7e-8054-36b203710eaa)

data = np.random.randint(low = 1, high = 100, size = (10,10))

hm=sns.heatmap(data=data,annot=True)

![image](https://github.com/user-attachments/assets/7bef97b2-f78c-4b21-8a85-29c8d91ba402)

hm=sns.heatmap(data=data)

![image](https://github.com/user-attachments/assets/1570b27e-cc54-4318-ace3-d96a2656c5d4)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
