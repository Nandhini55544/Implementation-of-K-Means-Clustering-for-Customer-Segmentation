# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import dataset and print head,info of the dataset
2.check for null values
3.Import kmeans and fit it to the dataset
4.Plot the graph using elbow method
5.Print the predicted array
6.Plot the customer segments 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Nandhini M
RegisterNumber: 212224040211

import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("Mall_Customers.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss = []

for i in range(1,11):
  kmeans = KMeans(n_clusters = i, init = "k-means++")
  kmeans.fit(data.iloc[:, 3:])
  wcss.append(kmeans.inertia_)
  
plt.plot(range(1, 11), wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

km = KMeans(n_clusters = 5)
km.fit(data.iloc[:, 3:])

y_pred = km.predict(data.iloc[:, 3:])
y_pred

data["cluster"] = y_pred
df0 = data[data["cluster"] == 0]
df1 = data[data["cluster"] == 1]
df2 = data[data["cluster"] == 2]
df3 = data[data["cluster"] == 3]
df4 = data[data["cluster"] == 4]
plt.scatter(df0["Annual Income (k$)"], df0["Spending Score (1-100)"], c = "red", label = "cluster0")
plt.scatter(df1["Annual Income (k$)"], df1["Spending Score (1-100)"], c = "black", label = "cluster1")
plt.scatter(df2["Annual Income (k$)"], df2["Spending Score (1-100)"], c = "blue", label = "cluster2")
plt.scatter(df3["Annual Income (k$)"], df3["Spending Score (1-100)"], c = "green", label = "cluster3")
plt.scatter(df4["Annual Income (k$)"], df4["Spending Score (1-100)"], c = "magenta", label = "cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:
## data head():
![image](https://github.com/user-attachments/assets/e0e1c9c5-3b7a-4a06-9b6d-843d0639e13d)

## data.info():
![image](https://github.com/user-attachments/assets/97c98a36-6d2a-4862-a4bd-6863190fc150)

## NULL values:
![image](https://github.com/user-attachments/assets/be42926e-224e-4b3e-b57f-a33af6cad766)

## Elbow graph:
![image](https://github.com/user-attachments/assets/c100ce74-4951-4b2d-8fcc-3a65bdd39008)

## Cluster:
![image](https://github.com/user-attachments/assets/d8c9298d-f0dc-4229-9e96-d5a87bcf6156)

## Predicted value:
![image](https://github.com/user-attachments/assets/8f7a3d48-fc99-4fa3-aa9d-96c3f7580b70)

## Graph:
![image](https://github.com/user-attachments/assets/d1c5cc34-43d2-417f-8e82-0a9b0c6ed670)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
