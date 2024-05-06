# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
### Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:

STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
Developed By : SANJAY T
Reg.no: 212222110039
```
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/61715c91-90d4-428c-bbf9-9eed2b8a7dc7)



### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/a417d2ec-4e3f-4fe6-9cf4-ece3cbf04d6a)


### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/f29af103-642f-42bb-984f-b1a55810f52d)



## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/0fac0442-a2eb-4c5c-ba54-8885c53890c1)

### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/b0491326-b02f-4538-94ae-75f03665b0d6)


### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/44aae5f1-305c-43de-9a5f-4c42b54caf4d)


## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/d1c50b7e-6ddc-4763-adcb-eeff314b6b13)


### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/4401d3ca-de45-485a-afa7-6dd331ab00ef)


### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/b781298c-ba63-42bb-8359-3750922d82c4)


### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/417432cb-c384-4bdc-8d00-a58a4eda2b5f)


### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/sanjaythiyagarajan/EXNO-6-DS/assets/119409242/1c343e50-512a-497e-80ca-1af713ef6ec2)



## Result:
  
  ### Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

