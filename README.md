# Geospatial-Clustering

Exploratory analysis of geolocation data of taxi ranks and clustering them with the aim of building service stations in the most densely populated clusters.

The following techniques were used sequentially to identify these clusters:

1. KMeans
2. DBSCAN
3. HDBSCAN

After the evaluation of above algorithms using silhouette scores, a method to classify the outliers to already classified clusters was developed. Using this method, all the outlier geographical points (longitude and latitude) were treated as test data points and training a K nearest neighbors classifier on the already classified clusters, the rest of the points were classified and score re-evaluated.

Although the new silhouette score was slightly lower, it was good enough for our use case as some clusters contained a high density of points within them, making them the hotspots for building service stations.
