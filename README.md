# Clustering-part-2

This noteboook follows on from classification part 1. We will use the ```iris``` flower dataset once again. We will explore the solutions built by K-means, DBSCAN and agglomerative hierarchical clustering.

We plots the samples in the 2D space where the horizontal axis corresponds to the sepal length and the vertical axis to the sepal width.

![image](https://user-images.githubusercontent.com/96924468/224837758-e36a4246-a644-43a5-8a59-8043b17fecd4.png)

We can also use the first three attributes, ```sepal length```, ```sepal width``` and ```petal length```, to define a 3D space and plot the samples in this space

![image](https://user-images.githubusercontent.com/96924468/226051447-405481e3-6234-4faf-a42d-0bdba6b95358.png)

## Choosing the value of K in the K-means algorithm

Before applying the K-means algorithm we need to decide how many clusters we want to create. We will train the K-means algorithm with half of the iris dataset (training set) and then will obtain the overall distance between samples in the other half of the iris dataset (validation set) and the final centroid. This procedure will be carried out for several values of K, from 1 to 15.

Now plot the overall distance between samples in each cluster and their centroid as a function of K for the train and validation sets.

![image](https://user-images.githubusercontent.com/96924468/227001079-d54ea9a5-c24f-4037-8c1c-0e79c0c7ffa9.png)

## DBSCAN

The DBSCAN algorithm builds clusters based on the notion of connectivity. We will first visualise a clustering solution on the 2D space formed by the ```sepal length``` and the ```sepal width``` attributes. In addition to 2 clusters (red and blue samples), DBSCAN returns outlier samples that are not assigned to any cluster.

![image](https://user-images.githubusercontent.com/96924468/227001655-85242c47-bc9c-4d1f-8af0-8aa49980051e.png)

DBSCAN proceeds by obtaining the density of samples around each sample. The density is estimated by counting the number of samples within a given radius. If this number is greater than a pre-specified threshold, DBSCAN treats the sample as a core sample, otherwise it will be a border sample.

Different thresholds produce different solutions. We obtain and plot the number of clusters and outliers identified by DBSCAN for different threshold values. Note that the 4 attributes of the dataset are used by DBSCAN.

![image](https://user-images.githubusercontent.com/96924468/227003012-b9fda095-2cd1-46c5-b9cc-ad009562d0ea.png)
![image](https://user-images.githubusercontent.com/96924468/227003111-90452127-8e49-4ac9-9c13-58bb51650dc3.png)

Note how the number of clusters decrease as we increase the threshold.

## Hierarchical Clustering

Hierarchical clustering builds clustering arrangements at different levels. We can apply an agglomerative clustering algorithm on the iris dataset and obtain the resulting dendrogram

![image](https://user-images.githubusercontent.com/96924468/228095407-5a7cdc03-ac94-43f0-bfe6-8757550d3ea5.png)

Branching in the dendrogram represents one of the clusters at one level being split. Note that the dendrogram includes the number of samples in each cluster at the lowest level between parenthesis or the sample index if the cluster consists of just one sample.

