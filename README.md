# CryptoClustering

### Project on Unsupervised learning
- In this Crypto Clustering assignment, I am utilizing my knowledge of Python and Unsupervised learning to predict if currencies are affected by 24-hour or 7-day price changes.

### Overview

- First I imported all the required libraries and dependencies and loaded the data into a Pandas DataFrame using pd.read_csv() function. After some exploratory analysis I plotted my data to see what's in my DataFrame.

- After that using `StandardScaler()` module from scikit-learn I normalized the dataset from the CSV file and created a new dataframe called, df_crypto_scaled, with scaled Data with coin_id column as an index.

- Now I found out the best value for K or optimum cluster number with the Original scaled Dataset by using KMeans Model and creating a new dataframe with a newly generated column of Crypto Cluster predictions in order to make a scatter plot that would give a meaningful visualization on the relationship between two types of price change percentages, they are, price percentage change in 24 hours and price percentage change in 7 days.The clusters seem to show how different cryptocurrencies behave in terms of price changes over these two different time periods.

- After that we optimized the clusters with Principal Component Analysis (PCA) and able to reduced the multiple features to only three pricicipal components/features those would still contribute to the maximum variance in the dataset. We made a new PCA dataframe with thereafter and by using the KMeans and elbow curve method , finally created a PCA dataframe with a new column for the predicted CryptoClusters numbers. And finally we generated a scatterplots with PCA1 and PCA2 columns in order to observe the relationship between these two newly generated featured columns.
- As a final part of the assignments I made composite plots for elbow curves with original data and PCA data. Additionally also generated composite scatter plots combining the plots from both, original dataset and PCA dataset side by side in order to understand the impact of using fewer features before and after using PCA analysis to cluster the data using K-Means. 

references for creating composite plots:
https://holoviz.org/tutorial/Composing_Plots.html

Thank you !

Regards,
Stuti Poudel
