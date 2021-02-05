# Cryptocurrencies

## Overview

On this project, I created a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for a new bank investment, who's interested in offering a new cryptocurrency investment portfolio. I used unsupervised learning to group the cryptocurrencies provided by CryptoCompare and decided on a clustering algorithm.

## Results

I started by preprocessing the data to only keep the cryptocurrencies that are actively trading, have a working algorithm, and have a complete set of data. This left me with 532 different cryptocurrencies. 

Then I applied PCA to reduce the dimensions to three principal components to create an elbow curve using hvPlot to find the best value for K. The elbow curve was produce using the K-Means method looping through 10 values for K.

<img width="896" alt="Screen Shot 2021-02-04 at 4 18 31 PM" src="https://user-images.githubusercontent.com/70611325/107093737-98cbc080-67ba-11eb-8578-384c0a4e72d6.png">

By looking at the graph, the best k-value appears to be 4, so we can conclude on an output of 4 clusters to categorize the cryptocurrencies.

After that, I created scatter plots with Plotly Express and hvplot, where we can visualize the distinct groups that correspond to the three principal components, then I created a table with all the currently tradable cryptocurrencies using the hvplot.table() function.

***3D-Scatter plot with clusters***

<img width="909" alt="Screen Shot 2021-02-05 at 2 10 53 PM" src="https://user-images.githubusercontent.com/70611325/107094578-1c39e180-67bc-11eb-83ed-bc4db4e8109b.png">

This 3-D scatter plot was obtained using the PCA algorithm to reduce the cryptocurrencies' dimensions to three principal components, and we can see how the different cryptocurrencies are grouped together. Two of the groups, containing Class #0 and #2, are clumped very closely together. Meanwhile, the group with Class #3 has a few different cryptocurrencies that are farther away from the others, and then is the last group, with Class #1, that only has one cryptocurrency.

***Tradable Cryptocurrencies Table***

<img width="720" alt="Screen Shot 2021-02-05 at 2 17 55 PM" src="https://user-images.githubusercontent.com/70611325/107095044-f7923980-67bc-11eb-90b6-319ad5ddcfda.png">

Based on this table, we can see that most of the cryptocurrencies are part of Class #0 and #2.

***2D-Scatter plot with TotalCoinMined vs TotalCoinSupply***

<img width="742" alt="Screen Shot 2021-02-05 at 2 18 59 PM" src="https://user-images.githubusercontent.com/70611325/107095136-1b557f80-67bd-11eb-859d-7c8ad29017b5.png">

This 2-D scatter plot shows the relationship between total coin supply and total coins mined, and how each currency compares to the rest. We can clearly see that there's only one cryptocurrency belonging to Class #1.

## Summary

This analysis shows that there are a lot of cryptocurrencies that perform similarly while there are a few that are outliers.

