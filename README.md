# Unsupervised Machine Learning: Playlist Clustering for Moosic

This case study project focuses on unsupervised machine learning.
Moosic is a startup that creates playlists for different music platforms such as Spotify, Apple Music, and YouTube Music. The goal is to automate playlist generation using machine learning, without relying on music experts to manually select songs.

Using a basic clustering algorithm like K-Means, a dataset collected from the Spotify API can be divided into several playlists. This dataset includes the following audio features:

* acousticness
* danceability
* duration_ms
* energy
* instrumentalness
* key
*liveness
* loudness
* mode
* speechiness
* tempo
* time_signature
* valence

### Central questions:
Can meaningful playlists — each reflecting a specific mood — be created exclusively through good feature selection and K-Means clustering? Or is this something only humans can achieve, since musical mood and emotion are highly subjective and emotionally driven?

### Data science context:
The dataset is unlabeled, meaning none of the songs are pre-assigned to playlists. The clustering algorithm groups the songs into *K* different clusters by minimizing the sum of squared deviations between each data point and the center of its cluster. These clusters are formed in the phase space defined by the audio features listed above.

