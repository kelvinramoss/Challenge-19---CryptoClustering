# Challenge-19---CryptoClustering

## Prepare the Data

    -  Utilize scikit-learn's StandardScaler() module to scale the data retrieved from the CSV file.

    - Generate a DataFrame comprising the scaled data, and designate the 'coin_id' column from the original DataFrame as the index for this new DataFrame.

## Discover the optimal value for 'k' by employing the initial scaled DataFrame.

Utilize the elbow method to determine the optimal 'k' value through these steps:

1. Generate a list ranging from 1 to 11 to represent different 'k' values.

2. Initialize an empty list to store inertia values.

3. Employ a loop to calculate inertia for each 'k' value.

4. Formulate a dictionary containing data to construct the elbow curve.

5. Create a line chart depicting inertia values for various 'k' values to visually discern the best 'k'.

6. Document in your notebook: "What value of 'k' is considered optimal?"

## Cluster Cryptocurrencies with K-means Using the Original Scaled Data

Perform cryptocurrency clustering using the original scaled data by following these steps:

1. Initialize the K-means model, utilizing the optimal 'k' value.

2. Fit the K-means model using the original scaled DataFrame.

3. Predict the clusters to categorize cryptocurrencies based on the original scaled DataFrame.

4. Duplicate the original data and introduce a new column for the predicted clusters.

5. Create a scatter plot with hvPlot with "PC1" as the x-axis and "PC2" as the y-axis.

6. Colors to the graph points based on the K-means labels.

7. Include the "coin_id" column in the hover_cols parameter to identify each cryptocurrency represented in the data points.

## Optimize Clusters with Principal Component Analysis

- Utilize the original scaled DataFrame to conduct a PCA and condense the features into three principal components.

- Gather the explained variance to assess the information attributed to each principal component. Document the total explained variance of these three principal components in your notebook.

- Subsequently, generate a new DataFrame using the PCA data, setting the "coin_id" index from the original DataFrame as the index for this new DataFrame.

## Find the Best Value for k Using the PCA Data

Apply the elbow method to the PCA data to identify the best k value through the following steps:

1. Create a list containing k-values ranging from 1 to 11.

2. Establish an empty list to compile the inertia values.

3. Utilize a for loop to calculate inertia for each conceivable k value.

4. Formulate a dictionary with the data needed to plot the Elbow curve.

5. Generate a line chart displaying all inertia values calculated with different k values, aiding in the visual identification of the optimal k value.

6. Answer the subsequent question in your notebook: 
    - What is the most suitable k value when utilizing the PCA data?

7. Assess whether it differs from the optimal k value identified using the original data.

## Cluster Cryptocurrencies with K-means Using the PCA Data

Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

1. Initialize the K-means model with the best value for k.

2. Fit the K-means model using the PCA data.

3. Predict the clusters to group the cryptocurrencies using the PCA data.

4. Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.

5. Create a scatter plot using hvPlot  with the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".

6. Color the graph points with the labels found using K-means.

7. Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

8. Address the following question: What is the influence of using fewer features to cluster the data with K-Means?

## Credits

I crafted this script by leveraging the provided starter code and adhered closely to the challenge specifications. Additionally, I engaged in a tutoring session to seek guidance, address queries, and resolve any encountered bugs within the script.