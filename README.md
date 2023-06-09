<h1 align="left">UNSUPERVISED MACHINE LEARNING<br><i>Topic: Cryptocurrency Trends Forecasting</i> </h1> 

<p>This project investigates price fluctuations of various cryptocurrencies over time. The project leverages unsupervised machine learning to discern patterns in these fluctuations and subsequently groups cryptocurrencies into clusters to match the patterns. </p>

## Data Science Methods
- Data preprocessing and normalization using StandardScaler
- Finding the best value for K using the elbow method 
- Clustering cryptocurrencies using K-means with original scaled data
- Feature reduction using Principal Component Analysis (PCA)
- Clustering cryptocurrencies using K-means with PCA data

## Conclusion

In general, using fewer features for K-Means clustering can result in more distinct clusters, due to a reduction in complexity and noise, which allows the clustering algorithm to capture the primary patterns in the data more effectively. However, in our specific case, the two features chosen for our initial analysis (e.g. 24h vs 7d price change percentages) appear not to display a significant degree of variance between them, and this results in clusters that are relatively indistinct. Further analysis employing Primary Component Analysis (PCA) results in more distinct clusters. This makes sense, because PCA is a dimensionality reduction technique that distills the attributions of variance in a dataset down to a small set of composite features. In our case, PCA1 and PCA2 capture ~70% of the variance in the data, which may explain why the K-Means analysis of these features yields more distinct clusters than our initial analysis of 24h and 7d price change percentages only.

## Limitations and Further Analysis
- The dataset used in this project is both synthetic and static and will not reflect the actual state of the market. Incorporating real-time market data will improve the relevance of the analysis and provide a more accurate representation of the market trends.
- The clustering method used, K-means, may not be the most suitable for all types of data distributions. The project can be extended by using different clustering methods to compare performance.
- The PCA method reduces the features to a fixed number of principal components, which may lead to a loss of information. Other feature reduction methods can be explored to maintain more information while reducing the dimensionality of the dataset.
