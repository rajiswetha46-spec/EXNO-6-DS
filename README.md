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


<img width="1250" height="217" alt="Screenshot 2026-05-25 224750" src="https://github.com/user-attachments/assets/f9848424-d279-4cac-b0b8-62e37922ee57" />

```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```

<img width="534" height="435" alt="image" src="https://github.com/user-attachments/assets/6a2f306e-3cd2-48ee-8e5c-2683d195d7ce" />


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

<img width="534" height="435" alt="image" src="https://github.com/user-attachments/assets/c302e462-c427-4fd6-87e9-96891469e3b2" />



```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```

<img width="901" height="601" alt="image" src="https://github.com/user-attachments/assets/3d938b72-d51b-4ac1-8f7e-88c05c5c3462" />


```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```

<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/4c462bdd-1ef5-4c2f-b23c-5b78823df8cd" />


```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```

<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/775b68fe-e787-443c-8bc7-bf8b9b387380" />



```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/e21096a0-031d-4954-b02a-bb042232d918" />


```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```

<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/48633d75-74d5-4a3c-b155-9034aebad4f8" />


```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```

<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/dac15c54-5c54-449f-8148-663ac79341a4" />


```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```

<img width="584" height="455" alt="image" src="https://github.com/user-attachments/assets/2b4400bb-15ac-4df8-a842-7d0dd7dc321f" />


```
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```

<img width="596" height="505" alt="image" src="https://github.com/user-attachments/assets/59f1d485-5bfb-4e95-940a-fcb712de3e44" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
