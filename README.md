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
~~~
Developed by:RUCHITRA.T
Register no:212223110043
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,5,1,7,1]
sns.lineplot(x=x,y=y)
df=sns.load_dataset("tips")
df
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='dashed',legend="auto")
avg_total_bill=df.groupby('day')["total_bill"].mean()
avg_tip=df.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="total bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="tip")
plt.xlabel('day of the week')
plt.ylabel("amount")
plt.title("average total bill and tip by day")
plt.legend()
sns.barplot(x='day',y='total_bill',hue="sex",data=df,palette="Set2")
plt.xlabel("daya of the week")
plt.ylabel("total bill")
plt.title("total bill by day and gender")
import pandas as pd
t=pd.read_csv("/content/titanic_dataset (1).csv")
t
plt.figure(figsize=(8,5))
sns.barplot(x="Embarked",y="Fare",data=t,palette="Set1")
plt.title("fare of passenger by embarked town")
sns.scatterplot(x="total_bill",y="tip",hue="sex",data=df)
plt.xlabel("total bill")
plt.ylabel("tip amount")
plt.title("scatterplot of total bill vs tip amount")
import numpy as np
np.random.seed(1)
num_v=np.random.randn(1000)
num_v=pd.Series(num_v,name="Numerical Variable")
num_v
sns.histplot(data=num_v,kde=True)
sns.boxplot(x=df['day'],y=df['total_bill'],hue=df['sex'])
sns.boxplot(x='day',y='total_bill',hue='smoker',data=df,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
sns.violinplot(x='day',y='total_bill',hue="smoker",data=df,linewidth=2,width=0.6,palette='Set3',inner="quartile")
plt.xlabel("day of the week")
plt.ylabel("total bill")
plt.title("violin plot of total bill by day and smoker status")
sns.set(style='whitegrid')
sns.violinplot(x="day",y='tip',data=df)
sns.set(style='whitegrid')
sns.violinplot(x=df["total_bill"])
sns.kdeplot(data=df,x="total_bill",hue="time",multiple='fill',linewidth=3,palette="Set2",alpha=0.8)
sns.kdeplot(data=df,x="total_bill",hue="time",multiple="layer",linewidth=3,palette="Set2",alpha=0.8)
~~~
## output
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/2aae054f-409f-4d2c-96c5-ca1cb5ed913e)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/d3a9f4aa-7c7c-43d8-ace1-adb8a4e3ff28)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/1ec84cb8-fc97-4253-9e38-8c02b03935b3)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/4c94acda-12b9-44a7-8f47-37c3d1750e3e)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/59d62288-ec98-403e-aa08-3f9ca5f9d28d)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/4ab660da-d7ca-40b1-a93a-865f49183486)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/bd56040f-b31b-433f-8cf3-1d6e36e713b0)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/a676e1e0-2a0c-48e7-862c-a34c720df965)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/89730294-47f4-4a59-8cd5-ade7b0a0f244)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/f6d9169c-1266-4558-9ce0-a312cf4c2b9a)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/e6088d24-e109-47f3-93bf-3d01617fc22a)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/4be65981-f717-4e22-8bf3-93195dd137d9)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/d62b05af-abdb-4f21-9134-1c5d5550cf08)
![image](https://github.com/RuchitraThiyagaraj/EXNO-6-DS/assets/154776996/ed32a9ce-65ae-4d3a-b4d2-fb2362d68e7e)
# Result:
Thus to perform data visualiation using seaborn python library is successfully executed using given datas.
