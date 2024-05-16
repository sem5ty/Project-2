PredictingSongPopularity

Introduction

Hundreds of songs are released every year, but very few of them make it to the top charts. Music analysis has made it possible to generate metadata of a song. Similarly, such features are available for artists and genres. We aim to answer the question - “Is it possible to predict the popularity of a song using these attributes in Machine Learning algorithms?”. Along with that, we learn more about the features involved, how important (or unimportant) they are and what are the possible limitations. Our key contributions are the following -
We explore a suitable dataset which contains the requisite features and tune it to our needs.
We perform Exploratory Data Analysis (EDA) on the data.
We apply several machine learning algorithms to predict the popularity of a song. We use both regression, classification and ensemble learning algorithms. Inferences are gained at every step and further work is decided based on that.
The model hyper parameters are tuned to fetch the best possible results. Different models are compared.

Data

Spotify has a public API which serves information about tracks, albums, artists, genres etc. [6] We obtained our dataset by making calls to different routes on Spotify’s Web API which is a collection of information of more than 175,000 songs. The catch here is that we use songs which are only Indian resulting in our dataset being limited to about 4000 songs. Features such as acousticness, danceability, energy etc. are available for tracks, artists, genres and years which forms the basis of our prediction.

Results

Below are the results for our classification models ranked by their accuracy in correctly predicting popular songs:

Model Type	Accuracy
Ensemble Model	79.23%
Random Forest	79%
Logistic Regression	78.8%
Naive Bayes	77.62%
KNN	76.8%
Decision Tree	68.7%
