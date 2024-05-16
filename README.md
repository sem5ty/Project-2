PredictingSongPopularity

Introduction
Hundreds of songs are released every year, but very few of them make it to the top charts. Music analysis has made it possible to generate metadata of a song. Similarly, such features are available for artists and genres. We aim to answer the question - “Is it possible to predict the popularity of a song using these attributes in Machine Learning algorithms?”. Along with that, we learn more about the features involved, how important (or unimportant) they are and what are the possible limitations. Our key contributions are the following -
We explore a suitable dataset which contains the requisite features and tune it to our needs.
We perform Exploratory Data Analysis (EDA) on the data.
We apply several machine learning algorithms to predict the popularity of a song. We use both regression, classification and ensemble learning algorithms. Inferences are gained at every step and further work is decided based on that.
The model hyper parameters are tuned to fetch the best possible results. Different models are compared.

Data
Spotify has a public API which serves information about tracks, albums, artists, genres etc. [6] We obtained our dataset by making calls to different routes on Spotify’s Web API which is a collection of information of more than 175,000 songs. The catch here is that we use songs which are only Indian resulting in our dataset being limited to about 4000 songs. Features such as acousticness, danceability, energy etc. are available for tracks, artists, genres and years which forms the basis of our prediction.

Explanation of Features
Since the data was collected by using Spotify's API, each column has detailed descriptions to be used as reference. Below is the table that was used to interpret each column.  

Key	Description
acousticness	A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.
danceability	Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.
duration_ms	The duration of the track in milliseconds.
energy	Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.
instrumentalness	Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.
key	The key the track is in.
liveness	Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.
loudness	The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typical range between -60 and 0 db.
mode	Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.
speechiness	Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.
tempo	The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.
time_signature	An estimated overall time signature of a track. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure).
valence	A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).
popularity	The popularity of a track is a value between 0 and 100, with 100 being the most popular. The popularity is calculated by algorithm and is based, in the most part, on the total number of plays the track has had and how recent those plays are. Generally speaking, songs that are being played a lot now will have a higher popularity than songs that were played a lot in the past. Duplicate tracks (e.g. the same track from a single and an album) are rated independently. Artist and album popularity is derived mathematically from track popularity. Note that the popularity value may lag actual popularity by a few days: the value is not updated in real time.
Results

Below are the results for our classification models ranked by their accuracy in correctly predicting popular songs:

Model Type	Accuracy
Ensemble Model	79.23%
Random Forest	79%
Logistic Regression	78.8%
Naive Bayes	77.62%
KNN	76.8%
Decision Tree	68.7%
