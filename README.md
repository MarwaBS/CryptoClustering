# **Cryptocurrency Clustering and Analysis with K-Means and PCA**

This project explores the clustering of cryptocurrencies using the **K-Means algorithm**, both with the original scaled features and with reduced features using **Principal Component Analysis (PCA)**. The goal is to cluster cryptocurrencies based on their price change percentages over various time intervals and analyze the optimal number of clusters.

---

## **Project Overview**

This project involves the following key steps:

1. **Data Preprocessing**: Scaling the data to standardize features for clustering.  
2. **Finding the Best k**: Using the **elbow method** to determine the optimal number of clusters.  
3. **Clustering with K-Means**: Applying the **K-Means algorithm** to both the original and PCA-reduced data.  
4. **Visualizing Clusters**: Creating scatter plots to visualize clustering results.  
5. **PCA Optimization**: Reducing dimensions with PCA and evaluating clustering performance.  
6. **Explained Variance**: Analyzing how much information the principal components retain.

---

## **Requirements**

To run this project, you will need the following libraries installed:

- **Python 3.x**
- **Pandas**: For data manipulation and analysis.
- **Matplotlib**: For creating visualizations.
- **Scikit-learn**: For implementing K-Means and PCA.
- **NumPy**: For numerical computations.

---

## **Installation**

To run this project, ensure you have the following Python libraries installed:
- Pandas: For data manipulation and analysis.
- Scikit-learn: For clustering (K-Means), dimensionality reduction (PCA), and preprocessing (StandardScaler).

1. Clone the repository:
   ```
   git clone https://github.com/your-username/cryptocurrency-clustering.git
   cd cryptocurrency-clustering```

2. Install the required libraries using pip:
   ```
      pip install pandas scikit-learn```
      
If you do not have Python installed, download it from the official Python website and ensure you have pip enabled during the installation process.

## Steps in the Project
### 1. Data Preprocessing
- The cryptocurrency dataset is scaled to standardize features.
- Standardization ensures all features contribute equally to clustering.
### 2. Finding the Best k (Elbow Method)
- The elbow method is used to identify the optimal number of clusters (k).
- A plot of inertia values is generated, and the "elbow" point is selected as the best k.
### 3. K-Means Clustering
- The K-Means algorithm is applied using the optimal k value.
- Cryptocurrencies are clustered based on price changes across different time intervals.
### 4. PCA Optimization
- PCA reduces the data’s dimensionality for improved visualization and clustering performance.
- The principal components are analyzed to evaluate the amount of information retained.
### 5. Visualizing Clusters
- Scatter plots are created to visualize clusters based on:
   - Original scaled data.
   - PCA-reduced data.
### 6. Feature Weights in PCA
- A feature importance DataFrame shows how each feature contributes to the principal components.
- This analysis highlights the most influential features.

---

## Results

### Elbow Method
T- he best value of `𝑘` was determined to be 4, based on the elbow point in the inertia vs. k plot.
### Clustering Results
- K-Means clustering was applied to both the original scaled data and the PCA-reduced data. The clustering showed that the cryptocurrencies were grouped into four distinct clusters, each representing a different pattern of price change across the specified time intervals (24h, 7d, and 30d).
### PCA and Explained Variance
- The PCA transformation reduced the dimensionality of the data, allowing for better clustering performance. The explained variance of the principal components showed that the majority of the variance in the data was captured by the first few components, making the PCA-reduced data effective for clustering.

---

## Conclusion
This project successfully clusters cryptocurrencies using the `K-Means algorithm` and `PCA`. By analyzing price change percentages across different time intervals, we were able to identify groups of cryptocurrencies that exhibit similar price movement patterns. 
- The elbow method provided the optimal number of clusters
- PCA enhanced clustering performance by reducing dimensionality while retaining critical information.
