# Cryptocurrencies

## Overview

Given a crytocurrencies dataset, we applied a classification Unsupervised Machine Learning algorithm, K-Means, which enabled us to group them based on their features.

## Resources

- Dataset:
  - [Crypto Dataset](https://github.com/harg74/Cryptocurrencies/blob/main/crypto_data.csv)

- Technolies used:
  - Python
  - SKlearn
  - hvplotlib
  - Jupyter Notebooks

## Results

To be able to successfully apply our Unsupervised Machine Learning algo, we need to previously preprocess and transform our dataset. Including dropping null values, using only tradaeble and mined cryptocurrencies, transforming categorical data into numerical data columns using the pandas.get_dummies method, and scaling the data with StandarScaler() method.

Another important aspect was the use of the Principal Component Analysis (PCA), which help us to reduce the dimensionality of the datasets and minimizing the information loss at the same time. PCA achieve this by creating new uncorrelated variables that maximizes variance.

![image](https://user-images.githubusercontent.com/78564912/151364197-ec98052f-afa4-48d7-af78-3d151bf8c09e.png)

The next step is to know in how many clusters (k) the dataset could be divided into. For this, we created an elbow curve plot, which is a visual aid to determine this parameter. We can see in the image below that the inflexion or "elbow" is made around 4, so we would use this as the signal to use our model with four clusters.

![image](https://user-images.githubusercontent.com/78564912/151367649-17212302-aeca-445a-b374-06245038ba1c.png)

After we determined our number of clusters we developed our K-Means model to fit the PCA analysis and predict the clustering class for each of the cryptos, which can be see in the below DataFrame.

![image](https://user-images.githubusercontent.com/78564912/151368207-86ed9954-038d-475e-ad53-06a98785d8ed.png)

TO have a better understanding of these classes and the clustering of these tokens, we developed a 3-D vizualization that includes our three Principal Components

![image](https://user-images.githubusercontent.com/78564912/151368702-55bb2dac-f924-4cbe-8e07-d9e890bd7da4.png)

## Summary

The purpose of the Unsupervised Machine Learning Algorithms is to discover patterns or groups, since want to figure out
if there is anything in the data can tell us.

In our particular analysis, we succesfully grouped the cryptocurrencies analyzed into four clusters and although we need to make further analysis, if would like to create an investment portfolio, this is a good starting point since the two most known cryptos, as of today (Bitcoin and Ethereum) are somewhere in the yellow and purple clusters that have less supply and mined coins in comparison to others.

