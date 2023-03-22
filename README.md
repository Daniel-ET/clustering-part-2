# Clustering-part-2

This noteboook follows on from classification part 1. We will use the ```iris``` flower dataset once again. We will explore the solutions built by K-means, DBSCAN and agglomerative hierarchical clustering.

We plots the samples in the 2D space where the horizontal axis corresponds to the sepal length and the vertical axis to the sepal width.

![image](https://user-images.githubusercontent.com/96924468/224837758-e36a4246-a644-43a5-8a59-8043b17fecd4.png)

We can also use the first three attributes, ```sepal length```, ```sepal width``` and ```petal length```, to define a 3D space and plot the samples in this space

![image](https://user-images.githubusercontent.com/96924468/226051447-405481e3-6234-4faf-a42d-0bdba6b95358.png)

### Choosing the value of K in the K-means algorithm

Before applying the K-means algorithm we need to decide how many clusters we want to create. We will train the K-means algorithm with half of the iris dataset (training set) and then will obtain the overall distance between samples in the other half of the iris dataset (validation set) and the final centroid. This procedure will be carried out for several values of K, from 1 to 15.



