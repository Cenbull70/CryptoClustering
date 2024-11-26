# Cryptocurrency Market Clustering Analysis
This project analyzes cryptocurrency market data to identify clusters of cryptocurrencies based on their price change percentages over various time periods. The clustering process utilizes K-Means and Principal Component Analysis (PCA) to explore the relationships between cryptocurrencies and reduce dimensionality for optimization and visualization.

## Project Overview
This project uses clustering techniques to group cryptocurrencies based on their market behavior. Key methods include:

K-Means Clustering: To identify distinct clusters of cryptocurrencies.
Principal Component Analysis (PCA): To optimize clustering by reducing the number of features while preserving most of the variance.
Elbow Curve Analysis: To determine the optimal number of clusters for K-Means.
The analysis uses Python with libraries such as scikit-learn, hvPlot, and pandas.

## Technologies Used
- Python 3.10+
- Libraries:
    - pandas
    - hvPlot
    - scikit-learn
    - StandardScaler and PCA for data preprocessing
    - KMeans for clustering

## Key Steps
### Data Preparation
    - Load cryptocurrency market data from crypto_market_data.csv.
    - Normalize the data using StandardScaler to ensure all features contribute equally to the clustering process.
### Elbow Curve and Optimal k
    - Use the Elbow Method to plot inertia values for k ranging from 1 to 11.
    - Identify the optimal number of clusters (k) based on the "elbow point."
### Clustering Analysis
    - Apply K-Means clustering using the optimal k on the original and PCA-transformed datasets.
    - Assign cluster labels to the cryptocurrencies and visualize them in scatter plots.
### Principal Component Analysis (PCA)
    - Reduce the original feature set to 3 principal components.
    - Reanalyze the clusters using the PCA-transformed data for better computational efficiency and visualization.

## Results
### Clustering Results
    - The Elbow Curve suggested an optimal value of k=4 for both the original and PCA-transformed data.
    - Scatter plots visualize the clusters in both feature spaces, confirming similar patterns despite dimensionality reduction.
#### PCA Explained Variance
PCA retained 6.4219 of the total variance across 3 components, effectively summarizing the original dataset.

## Conclusion
Using PCA to reduce dimensionality enhanced the clustering process by simplifying the data without significant loss of information. The resulting clusters highlight distinct groupings of cryptocurrencies based on their price change trends, offering insights into market behavior. While both the original and PCA-transformed datasets yielded similar clusters, the PCA approach was computationally more efficient and allowed for better visualization.
