# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas and matplotlib.pyplot

2.Read the dataset and transform it

3.Import KMeans and fit the data in the model

4.Plot the Cluster graph

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: PARANTHAMAN S
RegisterNumber:  212224040232

import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []

for i in range(1,11):
    kmeans = KMeans(n_clusters=i, init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No. of clusters")
plt.ylabel("wcss")
plt.title("Elbow method")

km = KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])

y_pred = km.predict(data.iloc[:,3:])
y_pred

data["cluster"] = y_pred

df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster 0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster 1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster 2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster 3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster 4")

plt.legend()
plt.title("customer segmentation")

*/
```

## Output:
![Screenshot 2024-12-24 205904](https://github.com/user-attachments/assets/b8c500c3-9ed9-4b80-bfd7-e22348900c4d)
![Screenshot 2024-12-24 205939](https://github.com/user-attachments/assets/e7e4dc0d-2d25-4c10-ab0a-056b8c483b7d)
![Screenshot 2024-12-24 210008](https://github.com/user-attachments/assets/5a145bd4-1514-476a-b053-32d0d16e3759)
![Screenshot 2024-12-24 210033](https://github.com/user-attachments/assets/db74e8f3-ee84-4d78-b12a-7bf035e8079b)
![image](https://github.com/user-attachments/assets/410ad877-0b22-4dee-9502-63549d44140a)
![image](https://github.com/user-attachments/assets/67eaee6b-c012-468b-a1c0-48bea96c2d57)








## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
