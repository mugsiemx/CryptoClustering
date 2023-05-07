# CryptoClustering
Module 19 Challenge - DUE 11 May 2023

![pexels-alesia-kozik-6780789](https://github.com/mugsiemx/CryptoClustering/blob/main/Images/pexels-alesia-kozik-6780789.jpg)

In this modern world of computers and new payment methods, we are here to analyze Cryptocurrency. The first cryptocurrency was Bitcoin, founded in 2009. Although there are thousands of cryptocurrencies, our dataset contains 41 entries which we are analyzing utilizing KMeans and Clustering of the original data, scaled and PCA calculations.

Will a significant difference show if we limit the number of components used to calculate variances in the data from the mean?

The process:
- First, we read in the crypto_market_data comma separated value file into a Pandas DataFrame utilizing jupyter notebooks. We generate summary statistics and plot the data to see the "features" we are working with. We do this with hvplot to show proficiency in a method we only touched on previously.
-Next, we use the scikit-learn StandardScaler module to normalize our data, create a DataFrame with the new values attached to the cryptocurrency ids.
-Find the best value for `k` using this original data by calculating the inertia from the scaled data, modeling with KMeans, and plotting a line chart (also known as an Elbow Curve) using all the inertia values for `k` so we can visually identify the optimal value for `k`.
    Predict the clusters for the cryptocurrencies and create a scatter plot using hvPlot to view the Crypto Currency Cluster Predictions.
-Find the best value for `k` using optimized clusters with PCA (Principal Component Analysis) by using 3 components. The total PCA explained variance is 89.5% which solidly covers the largest part of the data variances we are analyzing. However, using only 2 components would have been 71.9% of the overall variance. We could have made a poor prediction by not having enough data to provide confidence in the outcome. A fourth component would not have provided much value for the 5.7% contribution it would have made versus the additional resources used for the calculation.
    -In the PCA analysis we normalized our data and found that the best value for `k` is actually the same as the earlier scaled calculation with the elbow curve turning more linear after the `k` value of 4. The inertia variance clusters turned out to be a lower starting point also.

Charts of calculations and data:

![Inertia Raw Data](https://github.com/mugsiemx/CryptoClustering/blob/main/Images/inertia%20raw%20data.png)

![Separate Elbow Curve Comparisons](https://github.com/mugsiemx/CryptoClustering/blob/main/Images/Elbow%20Curves%20-%20Separate.png)

![Combined Elbow Curve Comparisons](https://github.com/mugsiemx/CryptoClustering/blob/main/Images/Elbow%20Curves%20-%20Combined.png)

![Crypto Currency Predictions](https://github.com/mugsiemx/CryptoClustering/blob/main/Images/Crypto%20Currency%20Predictions.png)


References:
Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only. https://static.bc-edx.com/data/dl-1-2/m19/lms/starter/Starter_Code.zip

Research of code and 'how to' ideas are located in the following webpage links but are not limited to the listed. The listed items were a major help to completion of this assignment.
-Data Visualization with hvPlot(II) by Dr Shouke Wei https://medium.com/@shouke.wei/data-visualization-with-hvplot-ii-most-widely-used-basic-plots-a0755bfd614d
- https://www.youtube.com/watch?v=PnwpoCDA5IM
- 3D Scatter Plot in Python - Matplotlib by Regenerative Today  #https://www.youtube.com/watch?v=PnwpoCDA5IM
-Stack Overflow https://stackoverflow.com/questions/67392824/plot-two-lines-in-one-graph-with-each-line-own-y-values
- definitions https://www.kaspersky.com/resource-center/definitions/what-is-cryptocurrency , https://www.forbes.com/advisor/investing/cryptocurrency/what-is-cryptocurrency/ , https://www.linkedin.com/pulse/what-cryptocurrency-how-does-works-guide-beginners-2023-edu-facts/
- Crypto Currency Photo credit to: pexels-alesia-kozik-6780789
