# Customer Segmentation

This project involves customer segmentation using the K-Means clustering algorithm on the Mall Customers dataset. The goal is to find the optimal number of clusters to segment customers based on their age, annual income, spending score, and gender.

### Dataset Information
The dataset used is Mall_Customers.csv, which contains the following columns:
CustomerID: Unique ID for each customer
Gender: The gender of the customer
Age: The age of the customer
Annual Income (k$): Annual income of the customer in thousands of dollars
Spending Score (1-100): Score assigned by the mall based on customer behavior and spending nature

#### Data Preprocessing
Handling Missing Values: The dataset is checked for missing values.
Encoding Categorical Variables: The 'Gender' column is encoded as a numerical variable (0 for Male, 1 for Female).
Standardizing the Data: The features are standardized using StandardScaler to have a mean of 0 and a standard deviation of 1.

### Data Visualization
Pairplot: A pairplot is created to visualize the distribution and relationship between different features.
Correlation Matrix: A heatmap is used to visualize the correlation matrix of the standardized features.
Dimensionality Reduction
Principal Component Analysis (PCA) is applied to reduce the data to two dimensions for visualization purposes.

### Finding Optimal Number of Clusters
The silhouette score is used to determine the optimal number of clusters (k). The silhouette score measures how similar an object is to its own cluster compared to other clusters. The optimal k is found by plotting silhouette scores for different values of k and selecting the k with the highest score.

### Results
#### Before Optimization:
Davies-Bouldin Score: 1.3865633995098623
Inertia: 412.24931737946685
Silhouette Score: 0.2745743496298952

#### After Optimization:
Davies-Bouldin Score: 1.0779180646091977
Inertia: 291.3960724895503
Silhouette Score: 0.33641141484341075

### Interpretation:
Davies-Bouldin Score: Decreased from 1.39 to 1.08, indicating improved cluster separation.
Inertia: Decreased from 412.25 to 291.40, indicating tighter clusters.
Silhouette Score: Increased from 0.27 to 0.34, indicating better-defined clusters.
The metrics after optimization show a significant improvement in clustering quality. The clusters are more compact and better separated, leading to a more meaningful segmentation of the customers.
