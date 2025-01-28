# Mall-Customer-Segmentation

### Overview

This project uses unsupervised learning techniques to segment customers based on their demographic information and spending habits. By applying K-Means clustering and Principal Component Analysis (PCA), this model identifies distinct customer groups that can help businesses improve their marketing strategies.

### Key Features

- Data Preprocessing: The dataset is cleaned and standardized to ensure accurate clustering results. Categorical variables (e.g., gender) are encoded, and numerical features (e.g., annual income, spending score) are scaled.

- Clustering with K-Means: K-Means is used to identify clusters based on customer demographics and spending behaviors. The optimal number of clusters is determined using the Elbow Method.

- Visualization: The clusters are visualized using PCA to reduce the dimensionality of the dataset and make the clusters easier to interpret.

- Model Evaluation: Silhouette score is used to assess the quality of the clusters.

### Dataset

The dataset, Mall_Customers.csv, contains the following columns:

- CustomerID: Unique ID of each customer (not relevant for clustering).
- Genre: Gender of the customer (Male/Female).
- Age: Age of the customer (numeric).
- Annual Income (k$): Annual income of the customer (in thousands).
- Spending Score (1-100): Spending score assigned to the customer based on behavior and spending patterns (1-100 scale).

### Steps

1. Data Preprocessing

- Dropping unnecessary columns: Removed the CustomerID column as it's not useful for clustering.
- Encoding categorical variables: The Genre column (Male/Female) is encoded as numerical values (0 for Female, 1 for Male).
- Scaling the data: Features are standardized using StandardScaler to ensure all features contribute equally to the clustering process.

2. Applying K-Means Clustering

- Elbow Method: Used to determine the optimal number of clusters by plotting the within-cluster sum of squares (WCSS) for different values of k.
- Clustering: After determining that 5 clusters offer a good fit, K-Means was applied with k=5.
- Cluster Analysis: Investigated the centers of each cluster to understand the typical characteristics of each group.

3. Visualizations

- Clusters: Used PCA (Principal Component Analysis) to reduce the dimensionality of the data to 2D for easy visualization and plotted the customer clusters.
- Cluster Summary: The mean, median, and standard deviation of the features for each cluster were calculated to understand the cluster characteristics.

4. Results

- Cluster Centers: The center values of each cluster (in original scale) were analyzed to interpret the characteristics of each segment, such as age, annual income, and spending score.
- Cluster Counts: The number of customers in each cluster was determined to understand the distribution across segments.
- Cluster Statistics: Additional analysis included the median and standard deviation of the features for each cluster.
  
![screenshot-localhost_8888-2025 01 28-13_34_11](https://github.com/user-attachments/assets/1effbacb-ff6f-4163-bfdf-e6db3f812c1d)

#### Conclusion

The clustering revealed distinct segments of customers that can help the business tailor marketing strategies:

- Cluster 0: Young customers with high spending scores and moderate income.
- Cluster 1: Customers with higher income but low spending scores.
- Cluster 2: Older customers with moderate income and spending scores.
- Cluster 3: Young customers with lower income but high spending scores.
- Cluster 4: Older customers with moderate income and low spending scores.

### Future Improvements

- Evaluation Metrics: Investigating more sophisticated clustering techniques like DBSCAN or Hierarchical Clustering.
- Feature Engineering: Adding new features such as customer behavior patterns or purchase history for better segmentation.
- Model Tuning: Exploring hyperparameter tuning or using different distance metrics for clustering.

### Source

Dataset: [Mall Customers Dataset on Kaggle](https://www.kaggle.com/datasets/shwetabh123/mall-customers)
