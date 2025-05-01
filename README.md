# Unsupervised Machine Learning: Playlist Clustering for Moosic

## Contents:

A short introduction to the project is provided below. The raw data used in this project can be found in `Data`. There is also a small warm-up in `kmeans_warmup.ipynb`, in which I introduce the use of the unsupervised ML method K-Means.  
The code for the actual project can be found in `cluster_songs.ipynb`.


## Project description

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


## Choosing the Right Number of Clusters (K)

One key step in K-Means clustering is selecting an appropriate value for `K`, the number of clusters.
Each time we increase K, the total intra-cluster variation (also called inertia) decreases, since the data points are grouped into more specific clusters. In the extreme case, if each point forms its own cluster, the variation becomes zero.
To determine the optimal K, we use the Elbow Method.
This involves plotting the inertia score (total within-cluster variation) against different values of K.
As K increases, the inertia decreases—but the rate of improvement slows down at some point. The "elbow point" on the curve—where the line starts to flatten—indicates a suitable value for K.
In my code example in “cluster_songs.ipynb”, `K = 23` is selected using the Elbow method, so that I get 23 playlists from the 5235 songs Spotify data set, which are all characterized by a certain “mood”.






