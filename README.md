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
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```

# Output

![image](https://github.com/user-attachments/assets/82225779-cf68-49c5-95c4-f2fbfe6ac211)


```
df = sns.load_dataset("tips")
df
```
# Output

![image](https://github.com/user-attachments/assets/0203b1a8-f158-4fe7-8fe4-0eb29be2266b)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```

# Output

![image](https://github.com/user-attachments/assets/875f7582-7612-475d-b2ef-73072a7a8f35)


```
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
```

# Output

![image](https://github.com/user-attachments/assets/a8801f0f-2a6c-4731-b5af-0dfec0dd5520)


```
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
```

# Output

![image](https://github.com/user-attachments/assets/dc98878a-7ee6-4ccd-84e0-b61c4a61b57f)


```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```

# Output


![image](https://github.com/user-attachments/assets/8b8bc602-fe37-4acf-ad09-ae16cdd83f5c)


```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```

# Output

![image](https://github.com/user-attachments/assets/790afe20-710f-420a-947a-7a5dc577b604)


```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```

# Output

![image](https://github.com/user-attachments/assets/6628a297-6bf7-49bd-890a-15e3e89ceec1)


```
ti=pd.read_csv("titanic_dataset.csv")
ti
```

# Output


![image](https://github.com/user-attachments/assets/32ff21b1-5ce3-4786-b646-0d7953399c99)


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=ti, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```

# Output

![image](https://github.com/user-attachments/assets/61177564-3cea-4a70-a0f6-385dfad486bd)


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=ti, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```

# Output

![image](https://github.com/user-attachments/assets/3c9bdf58-588a-4604-8dcd-9e365bc2c386)


```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

# Output

![image](https://github.com/user-attachments/assets/f3241119-efe3-46eb-9aec-484fc87e5828)


```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```

# Output

![image](https://github.com/user-attachments/assets/c024532e-cd3a-48e6-a102-983ef4d35bce)


```
sns.histplot(data = num_var, kde = True)
```

# Output

![image](https://github.com/user-attachments/assets/a39614d9-8822-4a40-9b6d-105e73f64ee3)


```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

# Output

![image](https://github.com/user-attachments/assets/6f64fc48-30bb-4667-895c-8fcd9e2d15d0)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
# Output

![image](https://github.com/user-attachments/assets/aee3c334-7291-48de-b4a5-cf70389e9bfe)



```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

# Output

![image](https://github.com/user-attachments/assets/cfd6977f-2ffa-4cdc-a13d-28c1c094778e)


```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

# Output

![image](https://github.com/user-attachments/assets/ebe442b2-82ce-4bcc-b09a-4e94639460e2)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```

# Output

![image](https://github.com/user-attachments/assets/91421083-e19a-45c0-8b52-246831287021)


```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```

# Output

![image](https://github.com/user-attachments/assets/e4126fe7-ba75-42ac-a59d-ebb8aa41682b)

```
sns.kdeplot(data=mart,x='PassengerId')
```

# Output

![image](https://github.com/user-attachments/assets/3aa53bbc-8dac-46ef-92ff-267a1c1613ae)


```
sns.kdeplot(data=mart,x='Age')
```

# Output

![image](https://github.com/user-attachments/assets/c09e761b-b31a-4244-8832-56130c1c3fc6)


```
sns.kdeplot(data=mart)
```

# Output

![image](https://github.com/user-attachments/assets/5ddeecf3-8d56-4d3b-865b-f50246f19902)


```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```

# Output

![image](https://github.com/user-attachments/assets/5c52d0c9-9c89-4610-a099-3e08cc05404a)


```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```


# Output

![image](https://github.com/user-attachments/assets/36932409-724e-4719-a76f-9c9a12c4c426)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```


# Output

![image](https://github.com/user-attachments/assets/afc62557-afa1-4309-b012-1cefdeb8614c)


```
hm=sns.heatmap(data=data)
```

# Output

![image](https://github.com/user-attachments/assets/b91efa27-28bd-4dd5-815b-a7e0e3ec0611)


# Result:
Thus, all the data visualization techniques of seaborn has been implemented successfully.
