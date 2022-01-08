# BootCamp-Mod-18-Cryptocurrencies
Performing unsupervised machine learning to create a classification system.

## Overview of Project
The purpose of this analysis is to use unsupervised machine learning to create a classification system to generate a cryptocurrency investment portfolio. 

### Process
- First, the cryptocurrency data has to be preprocessed to be able to be used in the machine learning model.
  * Keep only the rows that contain cryptocurrencies that are being traded.
  * Keep only the rows where coins have been mined.
  * Keep only the rows that contain a working algorithm.
  * Remove rows that have null values. (Note: This is a decision made for this data only. Every data set is different and it may not be in the best interest of the data to drop null rows.) 
  * Remove columns that are not useful.
  * Convert all columns to number values.
  * Standardize the data by using the StandardScaler function.

- Second, reduce the dimension of the data with Principal Component Analysis (PCA) to make the data set easier to work with.
  * The PCA function was used to fit and transform the scaled data into 3 components:
    - PC 1
    - PC 2
    - PC 3

- Third, K-means was used to cluster the cryptocurrency data.
  * An elbow curve was created to determine how many clusters should be used.
  * <p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-18-Cryptocurrencies/blob/main/Graphics/Elbow_Curve.png"width="661" height="287"/></p>
  * The k-means function was run using 4 clusters.
  * The classification of each row into one of the four clusters was added to the data.

- Finally, visualizations were created to view the cryptocurrency classifications.
  * A 3-D scatterplot was created to initially view the clusters.
  * <p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-18-Cryptocurrencies/blob/main/Graphics/3_D_Scatterplot.png"width="613" height="393"/></p>
  * The MinMaxScaler function was used to scale the total coin supply and the total coins mined to create a scatterplot comparing these features.
<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-18-Cryptocurrencies/blob/main/Graphics/Supply_vs_Mined_Scatterplot.png"width="637" height="284"/></p>

