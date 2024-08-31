# CryptoClustering: Unveiling Market Trends with K-Means and PCA

## Overview
This project uses Python and unsupervised learning techniques to analyze the impact of 24-hour and 7-day price changes on cryptocurrencies. The goal is to cluster cryptocurrencies based on their performance over these time periods using K-Means clustering and Principal Component Analysis (PCA).


### Steps Taken

1. **Prepare the Data**

- First I imported all the required libraries and dependencies and loaded the data into a Pandas DataFrame using pd.read_csv() function. After some exploratory analysis I plotted my data to see what's in my DataFrame.

- After that using `StandardScaler()` module from scikit-learn I normalized the dataset from the CSV file and created a new dataframe called, df_crypto_scaled, with scaled Data with coin_id column as an index.

2. **Finding the Optimal K and Clustering with K-Means**

- Now I found out the best value for K or optimum cluster number with the Original scaled Dataset by using KMeans Model and creating a new dataframe with a newly generated column of Crypto Cluster predictions in order to make a scatter plot that would give a meaningful visualization on the relationship between two types of price change percentages, they are, price percentage change in 24 hours and price percentage change in 7 days.The clusters seem to show how different cryptocurrencies behave in terms of price changes over these two different time periods.

3. **Optimize Clusters with PCA**

- After that we optimized the clusters with Principal Component Analysis (PCA) and able to reduced the multiple features to only three pricicipal components/features those would still contribute to the maximum variance in the dataset. We made a new PCA dataframe with thereafter and by using the KMeans and elbow curve method , finally created a PCA dataframe with a new column for the predicted CryptoClusters numbers. 

- And finally we generated a scatterplots with PCA1 and PCA2 columns in order to observe the relationship between these two newly generated featured columns.

4. **Vizualize and Compare Results**

- As a final part of the assignments I made composite plots for elbow curves with original data and PCA data. Additionally also generated composite scatter plots combining the plots from both, original dataset and PCA dataset side by side in order to understand the impact of using fewer features before and after using PCA analysis to cluster the data using K-Means. 

### Conclusion
Finally , we can make some inferences about the impact of using fewer features (via PCA) to cluster the data using K-Means:

i)Cluster Separation: The clusters in the original data are spread out, mostly along the x-axis (24-hour price change). Also, there is overlap between the clusters, suggesting that the features used may contain some amount of noise or irrelevant information that makes separation less distinct. Whereas, Clusters in the PCA-transformed data appear to be more distinct, particularly along the first principal component (PC1). This suggests that PCA has extracted the most significant features that contribute to the variance and thus helps to define clearer boundaries between clusters.

ii) Cluster Density: In the original Data, clusters are less dense, with more scattered points, which may indicate that the features have not captured the underlying structure of the data as effectively. Whereas, in PCA Data, clusters seem tighter and more cohesive, indicating that the reduced features may be more relevant for the clustering task.

iii) Noise Reduction: As the chart displays, the PCA process helped to filter out noise by consolidating the variance into fewer dimensions, which can lead to a more robust clustering performance.

In conclusion, using fewer, more relevant features via PCA for K-Means clustering appears to have a positive impact on the clarity and quality of the resulting clusters. It seems to enhance cluster separation, density, and possibly the interpretability of the clustering solution.

### Applications 

This project demonstrates the use of unsupervised learning techniques, specifically K-Means clustering and PCA, to analyze and group cryptocurrencies based on market performance. The results provide insights into how dimensionality reduction can impact clustering outcomes and offer a better understanding of cryptocurrency behavior.

References for creating composite plots:
https://holoviz.org/tutorial/Composing_Plots.html

Thank you !

Author

Stuti Poudel
