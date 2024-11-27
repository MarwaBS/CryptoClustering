# Cryptocurrency Clustering and Analysis with K-Means and PCA

This project explores the clustering of cryptocurrencies using the K-Means algorithm, both with the original scaled features and with reduced features using Principal Component Analysis (PCA). The goal is to cluster cryptocurrencies based on their price change percentages over various time intervals and analyze the optimal number of clusters.

## Project Overview

The project involves the following key steps:

1. **Data Preprocessing**: Scaling the data to prepare it for clustering.
2. **Finding the Best k**: Using the elbow method to determine the best value for the number of clusters (k).
3. **Clustering with K-Means**: Performing clustering with the K-Means algorithm on both the original scaled data and the PCA-reduced data.
4. **Visualizing Clusters**: Plotting the clusters on scatter plots for both original and PCA data.
5. **PCA Optimization**: Reducing the data dimensions using PCA and comparing clustering results.
6. **Explained Variance**: Analyzing the explained variance of the principal components and their influence on clustering.

## Requirements

To run this project, you will need the following libraries:

- **Python 3.x**
- **Pandas**: For data manipulation and analysis.
- **Matplotlib**: For data visualization.
- **Scikit-learn**: For implementing K-Means and PCA.
- **Numpy**: For numerical operations.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/cryptocurrency-clustering.git
   cd cryptocurrency-clustering

2. Install the required packages using pip:
`pip install -r requirements.txt`
3. Alternatively, if requirements.txt is not available, you can install the dependencies individually:
`pip install pandas matplotlib scikit-learn numpy`

## Steps in the Project
### 1. Data Preprocessing
The cryptocurrency dataset is loaded and scaled to standardize the features before applying the clustering algorithm. This ensures that each feature contributes equally to the clustering process.
### 2. Finding the Best k using the Elbow Method
The elbow method is used to determine the optimal number of clusters by plotting inertia values for different values of k (1 to 11).
The optimal k is selected by identifying the "elbow" point in the plot, where inertia decreases at a slower rate.
### 3. K-Means Clustering
Using the optimal value of k (determined from the elbow method), the K-Means algorithm is applied to cluster the cryptocurrencies based on price change percentages. The model is trained and the clusters are predicted.
### 4. PCA Optimization
Principal Component Analysis (PCA) is performed to reduce the dimensionality of the data. This helps in visualizing the data in 2 or 3 dimensions and improving the performance of clustering by eliminating correlated features.
The data is transformed into principal components, and the explained variance of these components is calculated to evaluate how much information is retained in the transformation.
### 5. Visualizing Clusters
Scatter plots are created to visualize the clustering results. One plot visualizes clusters based on the original features, and the other shows clusters based on the PCA-reduced features.
### 6. Determining Feature Weights in PCA
A DataFrame is created to show how much each feature contributes to the principal components. This helps in understanding which features are the most important for each component.
## Results
### Elbow Method
The best value of 𝑘 was determined to be 4, based on the elbow point in the inertia vs. k plot.
### Clustering Results
K-Means clustering was applied to both the original scaled data and the PCA-reduced data. The clustering showed that the cryptocurrencies were grouped into four distinct clusters, each representing a different pattern of price change across the specified time intervals (24h, 7d, and 30d).
### PCA and Explained Variance
The PCA transformation reduced the dimensionality of the data, allowing for better clustering performance. The explained variance of the principal components showed that the majority of the variance in the data was captured by the first few components, making the PCA-reduced data effective for clustering.
## Conclusion
This project successfully clusters cryptocurrencies using the K-Means algorithm and PCA. By analyzing price change percentages across different time intervals, we were able to identify groups of cryptocurrencies that exhibit similar price movement patterns. The elbow method provided the optimal number of clusters, and PCA helped reduce the data's dimensionality while retaining important information.

## Future Work
Exploring other clustering algorithms: We could experiment with other clustering algorithms, such as DBSCAN or hierarchical clustering, to compare performance and cluster quality.
Feature Engineering: Additional features, such as trading volume or market capitalization, could be included to improve clustering results.
Time-series Forecasting: Further analysis could involve time-series forecasting techniques to predict future price movements of cryptocurrencies.