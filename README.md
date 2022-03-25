# Customer-Segmentation

Customer segmentation is the practice of dividing the customers into groups that reflects similarity among customers in each group.


**Understanding the data:**
* Importing useful and required libraries
* Briefly understanding the dataset
* Check for null values
* Preparing data for clustering



Data used is Mall Customer Dataset from kaggle. Which has the fields such as CustomerID, Genre, Age, Annual Icome, Spending score ranges from 1-100. By looking at this data we can say basically a customer is spending less amount of his income the spending score will be on lower side and vice versa.

**Perform Elbow Method to find optimal number of clusters:**
* Using KMeans to iterate from 1 to 11 clusters and plotting a Elbow plot.
* Deciding optimal number of clusters to be used.

Elbow method is fundamental step for any unsupervised algorithm to determine the optimal number of clusters into which the data may be clustered. And also one of the most popular method to determine its optimal value of K. When we plot the line chart it resembles a arm and a elbow that is the point of inflection on a curve which is the good indication, the underlined model fits best at that point which is optimal number of clusters. K-Means clustering is an Unsupervised Learning Algorithm which groups the unlabeled dataset into different clusters. Here the letter K defined is the number of predefined clusters that need to be created in the process. As if k=2 there will be 2 clusters so on. It allows us to cluster the data into different groups and convenient way to discover the categories of groups in the unlabeled dataset on its own without any need of training.

WCSS is stated as Within Cluster Sum of Square. For each value of K we are calculating WCSS. It is the sum of squared distance between each point and the centroid in the cluster. 

When we plot WCSS with K value the plot look like an elbow as the number of cluster increases the WCSS value will start to decrease. WCSS value is largest
when K=1. Iterate the K-Mean algorithm for data for I iterations from 1 to 11, since we assume maximum clusters possible is not more than 10. Here using initialize as kmeans++ this means k-means++ algorithm ensures a smarter initialization of the centroids and improves the quality of clustering. Basically k-means++ is the standard clustering algorithm coupled with a smarter initialization of centroid. In this code kmeans.inertia_ is the formula used to segregate the data points into clusters.

**Training model using unsupervised learning algorithm (KMeans):**
* Initializing our KMeans model with selected optimal number of clusters.
* Plot the clusters, and gain intuitions regarding our clusters.


**Intuitions extracted from this plot are:**
* The green cluster on the top left side represents the customer having comparatively less salary but their spending is quite high.
* On the other side, the red cluster represents the customer whose annual salary is quite high but their spending is comparatively less.
* Now for any organization the customers from this blue cluster is the target audience since the maximum customers are included in this blue cluster also they have decent salary and their spending also quite well, so the organization will promote their products more with the customers included in blue cluster than the customers included in other clusters.
