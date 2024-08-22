# 19-CryptoClustering-


## Usage:

1. Jupyter notebook or VS code can be used to visualize the code and charts.
2. Python and the libraries *`scikit-learn`* and *`hvPlot`* need to be installed. 
3. In this repository, the "Resources" folder contains the "crypto_market_data.csv" file with raw data. The "Crypto_Clustering.ipynb" file contains the code. 

## Description: 

Using knowledge of Python and unsupervised learning, this assignment aims to predict whether cryptocurrencies are influenced by 24-hour or 7-day price changes. The code is divided into seven sections:

- **Part 1**: Loading the raw data by reading the CSV file into a pandas DataFrame.

- **Part 2:** Preparing the data by scaling all numerical columns using the *`StandardScaler()`* module. The data is fitted and transformed, resulting in an array that is subsequently converted into a DataFrame.

- **Part 3:** Determining the optimal value for k (the optimal number of clusters) for the original data using the *`Elbow Method`*. A *`For Loop`* is utilized to iterate through a range of k values, with the calculated inertia values appended to an empty list. A dictionary is created to store the values of *`k`* and *`inertia`*, which are then used to construct a DataFrame for plotting the elbow curve.

- **Part 4:** The *`KMeans algorithm`* is applied to cluster the cryptocurrencies based on the original data (without the elbow method). The *`KMeans`* model is used to fit and predict the clusters, grouping the cryptocurrencies using the scaled data from Part 2. A DataFrame is then created to plot a scatter plot displaying the clusters.

- **Part 5:** To optimize the clusters, *`Principal Component Analysis (PCA)`* is applied with 3 components. The data is fitted and transformed to utilize the *`explained variance ratio`*, thereby determining the percentage of the original data attributed to each principal component. A DataFrame is created for the PCA-transformed data.

- **Part 6:** After optimizing the clusters using *`PCA`*, the *`Elbow Method`* is applied again to identify the optimal value of *`k`* for the optimized clusters. Similar to Part 3, a *`For Loop`*, dictionary, and DataFrame are created to plot the elbow curve.

- **Part 7:** Using the PCA-transformed data, cryptocurrencies are clustered again using the *`KMeans model`*, this time incorporating the *`Elbow Method`* and *  *`PCA-optimized clusters`*. The PCA data is fitted and transformed, and a DataFrame is created to plot a scatter plot that visualizes the distinct clusters.

- **Part 8:** A composite plot variable is created to contrast the elbow curves generated in Parts 3 and 6. Additionally, a composite plot variable is created to contrast the clusters formed in Parts 4 and 7.


## References:

- Xpert Learning Assistant
- AskBCS Learning Assistant
- Curriculum content
- Tutoring