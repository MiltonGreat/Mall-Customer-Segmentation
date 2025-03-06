# Customer Segmentation using Agglomerative Clustering

### Overview

This project applies unsupervised learning techniques to segment mall customers based on their demographics and spending behavior. By clustering customers using Agglomerative Clustering, we identify distinct customer groups that share similar characteristics, providing valuable insights for businesses to optimize marketing strategies.

### Business Value

Understanding customer segmentation helps businesses:

- Create targeted promotions and discounts for specific customer groups.
- Identify high-value customers (e.g., those with high spending scores) and develop loyalty programs.
- Understand customer demographics and spending patterns to inform product placement and service offerings.
- Re-engage at-risk customers (e.g., those with low spending scores) through personalized incentives.

### Dataset

The dataset, Mall_Customers.csv, contains the following columns:

- CustomerID: Unique ID of each customer (not relevant for clustering).
- Genre: Gender of the customer (Male/Female).
- Age: Age of the customer (numeric).
- Annual Income (k$): Annual income of the customer (in thousands).
- Spending Score (1-100): Spending score assigned to the customer based on behavior and spending patterns (1-100 scale).

### Methology

1. Data Preprocessing

- Dropping unnecessary columns: Removed the CustomerID column as it's not useful for clustering.
- Encoding categorical variables: The Genre column (Male/Female) is encoded as numerical values (0 for Female, 1 for Male).
- Scaling the data: Features are standardized using StandardScaler to ensure all features contribute equally to the clustering process.

2. Applying Clustering

- Used Agglomerative Clustering to segment customers.
- Selected the optimal number of clusters using Silhouette Score and Davies-Bouldin Score.
- Applied Principal Component Analysis (PCA) for visualization and dimensionality reduction.

3. Cluster Analysis

- Analyzed cluster sizes, means, and medians for key features.
- Examined spending behaviors and demographics within each cluster.
- Created pivot tables to explore gender distribution per cluster.

4. Key Findings

- High-spending customers were segmented, allowing businesses to target them with loyalty programs.
- Low-spending customers were identified, enabling strategies to re-engage them with personalized offers.
- PCA visualization confirmed clear separations among clusters, indicating effective segmentation.

The clustering revealed distinct segments of customers that can help the business tailor marketing strategies:

#### Clustering Analysis

Five distinct customer segments were identified, each with unique spending behaviors and income levels.

- Cluster 0: Young customers with high spending scores and moderate income.
- Cluster 1: Customers with higher income but low spending scores.
- Cluster 2: Older customers with moderate income and spending scores.
- Cluster 3: Young customers with lower income but high spending scores.
- Cluster 4: Older customers with moderate income and low spending scores.

### Source

Dataset: [Mall Customers Dataset on Kaggle](https://www.kaggle.com/datasets/shwetabh123/mall-customers)
