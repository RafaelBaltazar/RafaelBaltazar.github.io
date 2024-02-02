# *Music Recomendator and Visualization*

## *Description*
This project explores music metadata using Python and various data analysis tools to create a machine learning algorithm to sugest songs based similar atributes from the song you selected. Utilizing pandas, numpy, and Plotly, I analyzed a dataset containing music information, focusing on trends across genres and years. The project also involved dimensionality reduction techniques like PCA and clustering to uncover patterns and create visualizations.

## *Code Summary*

### *Data Loading and Exploration*

Loaded music data from CSV files and explored basic statistics. The database can be found [here](https://github.com/RafaelBaltazar/RafaelBaltazar.github.io/tree/main/projects/music_recomendator)

### *Data Cleaning*

Removed unnecessary columns and handled missing values.

### *Genre Analysis*

Utilized Plotly to visualize trends in loudness and other features over the years.

### *Dimensionality Reduction*

Employed PCA to reduce the dimensions of genre data and applied KMeans clustering for pattern discovery.

### *Cluster Visualization* 

Created interactive scatter plots to showcase clusters and their associated genres.


<img src="images/cluster_pca.JPG?raw=true"/>


### *Song Embedding*

Applied one-hot encoding and PCA to embed songs into a lower-dimensional space, allowing for clustering.

### *Song Recommendation*

Developed a song recommendation system based on Euclidean distances and recommended songs with visualization of the album covers.


<img src="images/recomendator.JPG?raw=true"/>


### *Conclusion*

This project not only explores the technical aspects of data analysis but also demonstrates the art of transforming raw data into meaningful insights and recommendations. The visualization component adds an interactive element, enhancing the user experience.

You can find the link to the code [here](https://raw.githubusercontent.com/RafaelBaltazar/RafaelBaltazar.github.io/main/projects/music_recomendator/music_recomendator)
