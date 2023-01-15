# Cryptocurrencies
## Overview:
In the Challenge I have used unsupervised machine learning to complete the following deliverable.
-	Part 1: Preprocessing the Data for PCA
-	Part 2: Reducing Data Dimensions Using PCA
-	Part 3: Clustering Cryptocurrencies Using K-means
-	Part 4: Visualizing Cryptocurrencies Results

## Results:
-	Part 1: Preprocessing the Data for PCA (See [crypto_clustering](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_clustering.ipynb))
      - Firstly, I prep the data by read the [crypto_data.csv](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_data.csv) file into the dataframe df_crypto. I drop all the null values and used the get_dummies funcation to the Algorthm vaules in the variable df_newcrypto( see out10). I used standardize the data with StandardScaler in the variable crypto_scaled.

-	Part 2: Reducing Data Dimensions Using PCA (See [crypto_clustering](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_clustering.ipynb))
      - I initialize PCA model and store the value in pca variable. To reduce dimension to three principal components i used the fit_transform funcation and store the value in crypto_pca. I then create a new dataframe df_crypto_pca and create columns PC 1, PC 2 and PC 3.
-	Part 3: Clustering Cryptocurrencies Using K-means (See [crypto_clustering](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_clustering.ipynb))
      - For clustering cryptocurrencies, I used a for loop to go through the df_crypto_pca dataframe to create km.fit, these values were then  define in the dataframe df_elbow to create the elbow curve. See image below
      
      - ![](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/Elbow.png)

      - I then copy the dataframe and create the variable proedictions to create return DataFrame with predicted clusters that has the values for "Class"
      - I concatentate the df_crypto and df_crypto_pca DataFrames to form one dataframe clustered_df 

-	Part 4: Visualizing Cryptocurrencies Results (See [crypto_clustering](https://github.com/JaredTMurray/Cryptocurrencies/blob/main/crypto_clustering.ipynb))

## Summary:
