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
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="944" height="169" alt="image" src="https://github.com/user-attachments/assets/de29f82f-3cb8-4f11-9310-c393fc82e46e" />


```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
```
<img width="600" height="388" alt="image" src="https://github.com/user-attachments/assets/4fd65109-2b96-47e3-b8c7-5ea78dc8de2b" />

```
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
```
<img width="600" height="399" alt="image" src="https://github.com/user-attachments/assets/a425b028-933f-4456-b9be-19478731d1e3" />

```
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
```
<img width="699" height="411" alt="image" src="https://github.com/user-attachments/assets/19f9d81d-88cb-47c2-bd59-ef6bb49fee01" />

```
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
```
<img width="617" height="376" alt="image" src="https://github.com/user-attachments/assets/d461b49e-0919-4505-ab44-014fc8ca5991" />

```
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
```
<img width="566" height="378" alt="image" src="https://github.com/user-attachments/assets/3ca52cf0-8be6-43a1-b477-4449d9e87896" />

```
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
```
<img width="626" height="387" alt="image" src="https://github.com/user-attachments/assets/ceee780e-f9a1-474d-aace-a73f6a1f0368" />

```
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
```
<img width="644" height="410" alt="image" src="https://github.com/user-attachments/assets/62917e03-a367-4af2-8010-4cdcb7cef147" />

```
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
```
<img width="636" height="372" alt="image" src="https://github.com/user-attachments/assets/eac7c3d2-9f32-4f47-ada0-aedb2d4620f8" />

```
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
```
<img width="638" height="378" alt="image" src="https://github.com/user-attachments/assets/53419dbd-efcf-46ec-817e-277f191a5c59" />

```
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
```
<img width="643" height="429" alt="image" src="https://github.com/user-attachments/assets/b619cedd-eb78-4e69-aa81-e45818241247" />

```
# Result:
 Include your result here
