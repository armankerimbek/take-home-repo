# Task 1: Vehicle Segmentation

In this task, I explored two clustering techniques: K-means and DBSCAN. Each method has its own advantages and disadvantages. K-means allows us to specify the number of clusters we want to identify, which aids in the explainability of the clusters. This is not the case with DBSCAN, where the number of clusters is not pre-defined. However, DBSCAN is more robust and makes fewer assumptions about the data. Ultimately, I chose the K-means technique to explain the clusters.

Based on the K-means results, the following cluster profiles can be created using the original features:
- Cluster 1: Composed of fully used cars with manual transmission. This is the largest cluster, primarily consisting of vehicles with lower horsepower and some of the lowest-priced vehicles.
- Cluster 2: Contains used cars with automatic transmission, typically newer models (lower vehicle age).
- Cluster 3: Includes all new cars, both manual and automatic, with the second-highest prices in the market.
- Cluster 4: Comprises fully automatic older cars with the highest mileage and some of the lowest prices. These vehicles take longer to sell.
- Cluster 5: Mostly consists of fully automatic older cars, featuring the highest horsepower and price range.
- Cluster 6: Contains older, fully automatic cars with the lowest horsepower, often among the oldest models. These vehicles also take longer to sell.

# Task 2: Anomaly Detection

In this report, I’ve explored a clustering approach to identify outliers in the data. Although DBSCAN does not show great performance based on the silhouette score, one of its benefits is its ability to create clusters and isolate outliers that do not belong to any cluster. As a result of my analysis, I can highlight the following characteristics of the outliers the the website may consider when identifying suspicious listings and taking action to remove them.

Price: Price has been a major driver of PCA, explaining a significant portion of the variability in the data. Vehicles with substantially higher prices are classified as outliers. This suggests that unusually high-priced vehicles may not fit typical market patterns and should be further examined.
Power (HP): There is a clear trend where outliers tend to have higher horsepower. This indicates that vehicles with extremely high power values might be flagged as outliers and warrant closer inspection.
Condition: There doesn’t appear to be a strong relationship between vehicle condition and outliers. The condition of the vehicle seems to have minimal impact on whether it is classified as an outlier, suggesting that other factors might be more significant in identifying outliers.
Transmission: Outliers occur more frequently in vehicles with automatic transmission when considering the ratios. This indicates that automatic transmission vehicles may be more prone to being classified as outliers, possibly due to pricing or other factors associated with these models.

# Task 3: Time-Based Analysis

Overall, the nature of the data makes it unsuitable for time-series analysis. With less than a month of quality data, there is limited scope to model seasonality. The data was collected through web scraping at a specific point in time. Since this is an ad listing website, once a deal is settled, the ad is typically removed, and the data point no longer exists. A potential solution would be to perform web scraping at regular intervals (e.g., weekly) to minimize data loss.# take-home-repo
