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
```
 Developed by: D Vergin Jenifer
Register no:212223240174
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
```
![image](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/3d7db9e5-a2cd-441d-8c9f-61dfe72f4d24)
![image](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/f88157e4-e30c-43a3-a4aa-ca1365a67329)
![327994048-4b5ba758-c8ac-47f5-ba4a-15d3139a8e1e](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/f2804471-e587-4ff7-9ce6-cebf88053c92)
![327994060-e986993b-b696-447b-ab75-bde185b2e9ca](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/ca920469-88f6-44e4-8ed9-ffa207dc7e26)
![327994068-aeca82f1-32f9-49ac-9006-efee355424ef](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/ac5726cc-9f82-4757-af00-7646468ba513)
![327994079-9b286833-e4d6-4b12-9f9b-ca946de38991](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/79280ec4-2a77-4ae7-b42d-75a4514b6d1b)
![327994084-8a8cd0af-854a-40b0-b3e6-eae47b633099](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/51bf40f1-d904-41e2-84fe-d02609ac728b)
![327994093-e5eaa80e-7af6-4326-ad2a-04bf4117aafc](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/b48be620-5e08-4e7b-b1c1-e7f38948d896)
![327994100-f27dd708-d7f2-4be1-bd2f-7894cf51cce1](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/f343d9b8-3d21-452a-9179-b54568131c52)
![327994103-ebb06851-e7aa-4e49-84f2-f2893fcdfa72](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/5495a7c8-ab18-4263-a683-93e966b23a25)
![327994108-4cfdade5-efd3-4ada-aca3-9c104e79af1f](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/75458cf7-285e-4469-97d3-467114db3feb)
![327994113-5de8b997-b38c-4b66-a42a-c66c0218be6b](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/6e9b6f36-4f0b-4ddf-a558-861598aaa801)
![327994118-a4858d6d-9009-45fc-9674-c59aa683c143](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/e0e1a481-712b-47fc-a2a2-33403709d3e3)
![327994118-a4858d6d-9009-45fc-9674-c59aa683c143](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/568f65a9-7a1c-46e4-a0d2-2c4a584c4c11)
![327994124-938edd69-f5a9-46e2-80b1-53b5856979c2](https://github.com/VerginJenifer/EXNO-6-DS/assets/136251012/127424e2-c8b5-4729-a28f-f1441cf445f8)

# Result:
Thus to perform data visualiation using seaborn python library is successfully executed using given datas.
