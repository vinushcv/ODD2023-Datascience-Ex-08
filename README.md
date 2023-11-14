# Ex-08-Data-Visualization-
# AIM

To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
- STEP 1:
 Read the given Data
- STEP 2:
 Clean the Data Set using Data Cleaning Process
- STEP 3:
 Apply Feature generation and selection techniques to all the features of the data set
- STEP 4:
 Apply data visualization techniques to identify the patterns of the data.

# PROGRAM:
```
Developed By: vinush.cv
Reg No: 212222230176
```
### READING THE GIVEN FILES
```python
import pandas as pd
df=pd.read_csv("/content/Superstore.csv",encoding='unicode_escape')
df.head()
```
### DATA VISUALIZATION USING SEABORN :
```
import seaborn as sns
from matplotlib import pyplot as plt
```
- <B>_LINE PLOT:_</B>
```python
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/ebf5d018-c31c-4610-b26e-6395daeb5448" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/f50bd4c8-8840-4d61-afa9-f090d98716d2" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/dddc0ce1-5d37-463d-af9d-d9a39cf33def" height=300 width=350>

- <B>_SCATTERPLOT:_</B>
```python
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/23b30b9e-cb60-4dd5-a7a7-be941b7e291d" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/e422342a-4fff-487e-9780-aa92e2db6b19" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/8f9e780a-bcdd-47e0-a21e-25e8dca37cab" height=300 width=350>

- <B>_BOXPLOT:_</B>
```python
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/68af3f52-c256-452b-b987-afc6767d09ac" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/27f1e245-2725-436d-a68b-df3b3c5c1660" height=300 width=350>

- <B>_VIOLIN PLOT:_</B>
```python
sns.violinplot(x="Profit",data=df)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/19b590d7-641d-47ed-af0f-40e52df39587" height=300 width=350>

- <B>_BARPLOT_</B>
```python
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/16ece634-b224-42df-82be-c4a731f908af" height=500 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/32fcf2ae-85be-4bfa-bacb-0839304efe5b" height=300 width=350>

- <B>_POINTPLOT_</B>
```python
sns.pointplot(x=df["Quantity"],y=df["Discount"])
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/cc5c01fb-bc88-4f6e-8f53-08e45f679e08" height=300 width=350>

- <B>_COUNT PLOT_</B>
```python
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/b6e8298d-0a6c-4a58-85b6-6a0e5c53508f" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/a9e07021-4889-490c-8451-69864bf6f778" height=300 width=350>

- <B>_HISTOGRAM_</B>
```python
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
``` 
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/6e5a4fab-1cfd-4415-9a76-6e398571742b" height=300 width=350>

- <B>_KDE PLOT_</B>
```python
sns.kdeplot(x="Profit", data = df,hue='Category')
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/2129a043-381c-4b04-a0da-5b6745ba0adf" height=300 width=350>

### DATA VISUALIZATION USING MATPLOTLIB :
- <B>_PLOT_</B>
```python
plt.plot(df['Category'], df['Sales'])
plt.show()
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/5f621aad-c520-4e01-96cf-1701acefa1e7" height=300 width=350>


- <B>_HEATMAP:_</B>
```python
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/d133809e-1704-4f91-8332-0041d7ca3e33" height=300 width=350>

- <B>_PIECHART:_</B>
```python
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/09b81541-1b03-4017-bd64-e20c6894898b" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/76eb96a0-0bec-4d40-af21-f906b45b9c16" height=300 width=350>

- <B>_HISTOGRAM:_</B>
```python
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/5d549a00-18a3-4126-af87-1652098f826d" height=300 width=350>

- <B>_BARGRAPH:_</B> 
```python
plt.bar(df.index,df['Category'])
plt.show()
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/bee209ed-e0f9-4968-94c7-babc9140edfb" height=300 width=350>

- <B>_SCATTERPLOT:_</B>
```python
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/82653e8a-3f2a-4a58-ae41-0631925cd402" height=300 width=350>

- <B>_BOXPLOT:_</B>
```python
plt.boxplot(x="Sales",data=df)
plt.show()
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/9515bcd2-15ba-453a-a02e-e3e6e3ea875c" height=300 width=350>

# Inference:
# RESULT: 
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.
