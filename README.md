# ML-socio-economic-clustering-of-countries

An international non-governmental organization (NGO), HELP has raised funds of 10 million $. HELP wants to use the funds for humanitarian projects in the countries that are in the direst need of aid. This problem problem fits very well in the category of clustering in an unsupervised learning setup of Machine Learning.

First step of the problem is EDA. Dataset contains 167 countries and about 9 variables. Univariate & bivariate analysis is done with histogram distribution, strip plots, box plots & heatmap, regplot, scatter plots. There are outliers in the data. These outliers can skew the cluster centroids and hence must be handled effectively. However, the data cannot be simply dropped because countries in need of aid might be one of these so-called outliers. Hover function of plotly was used to understand the countries which are outliers and based on the EDA, clustering was limited to the countries with gdpp below 20k. This makes sense because 10 million $ is impactful to countries with low gdpp & low income per person. Swarm plots was used to visualize the gdpp groups.

Second step is the modelling. Before that the dataframe was standardized to get sensible cluster centroids. Hopkins statistics was about 0.8 which suggests that the data is clusterable and not random in nature. Two different algorithms were applied. KMeans clustering with different number of clusters was studied with Elbow Curve & Silhouette scores. Hierarchical clustering was done with single and complete linkages. Both these algorithms led to an optimum cluster count of 5. Hierarchical clustering produced better results with more stable & more clearly demarcated clusters when compared to KMeans.

Third step is to do the cluster profiling with Box Plots & identify countries in direst need of aid. Two different logics were applied to narrow down to top-5 countries in direst need of aid. Both these logics produced similar results on both KMeans and Hierarchical clustering. This gives high confidence in the clustering predictions.

Fourth step is to visualize the clusters of countries. This was done with Plotly scatter plots on gdpp, child_mort and income. Results showed a visual confirmation of the clusters.

Finally, the study was concluded by visualizing the resulting clusters all the countries by plotting a choropleth. This gave a clear indication that most of the countries in direst need of aid are from African continent. 
