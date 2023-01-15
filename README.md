# Cryptocurrencies
## Overview:
In the Challenge I have used unsupervised machine learning to complete the following deliverable.
-	Part 1: Preprocessing the Data for PCA
-	Part 2: Reducing Data Dimensions Using PCA
-	Part 3: Clustering Cryptocurrencies Using K-means
-	Part 4: Visualizing Cryptocurrencies Results

## Results:
-	Part 1: Preprocessing the Data for PCA (See [crypto_clustering](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_clustering.ipynb))
      - Firstly, I prepped the data by read the [crypto_data.csv](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_data.csv) file into the dataframe df_crypto. I dropped all the null values and used the get_dummies function to the Algorithm vaules in the variable df_newcrypto( see Out 10). I used the standardize the data method with StandardScaler in the variable crypto_scaled.

-	Part 2: Reducing Data Dimensions Using PCA (See [crypto_clustering](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_clustering.ipynb))
      - I initialized PCA model and stored the value in the pca variable. To reduce dimension to three principal components I used the fit_transform function and stored the value in crypto_pca. I then created a new dataframe df_crypto_pca and created columns PC 1, PC 2 and PC 3.
-	Part 3: Clustering Cryptocurrencies Using K-means (See [crypto_clustering](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_clustering.ipynb))
      - For clustering cryptocurrencies, I used a for loop to go through the df_crypto_pca dataframe to create km.fit, these values were then defined in the dataframe df_elbow to create the elbow curve. See image below
      
      - ![](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/Elbow.png)
      - I then copy the dataframe and create the variable proedictions to create return DataFrame with predicted clusters that has the values for "Class"
      - I concatentate the df_crypto and df_crypto_pca DataFrames to form one dataframe clustered_df
      - Also, I concatentate the df_coinname to add Coinname column and I add the Class column  by addfive_clusters dataframe to clustered_df dataframe (See In and Out 16).

-	Part 4: Visualizing Cryptocurrencies Results (See [crypto_clustering](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_clustering.ipynb))
      - To creating a 3D-Scatter with the PCA data and the clusters, I created the six_clusters to hold the values form df_crypto_pca dataframe
      - To plot the 3D-Scatter with x="PC 1", y="PC2" and z="PC 3" (See In 21 and image below)
      - ![](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/3D_Scater_plot.png)
      - Transform PCA data to a DataFrame plot_df = pd.DataFrame(data=coin_pca, columns=["TotalCoinSupply", "TotalCoinsMined"])
      - Create a hvplot.scatter plot using x="TotalCoinsMined" and y="TotalCoinSupply". 
      - The coin_clusters.hvplot.scatter(x="TotalCoinSupply", y="TotalCoinsMined")
      - ![](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/2D_Scater_plot.png)

## Summary:
- The crypto currency which is the most tradeable are bitcoin, ethereum, litecoin and monero
- Note I ran into programming errors while merging the dataframes.
- 
