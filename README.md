# Clustering Disaster Tweets

#### Matthew Kwee, 12 Nov. 2021

## Abstract
In this project, I created an LDA topic model in order to cluster tweets discussing various kinds of disasters.
Using a dataset from a [Kaggle competition](https://www.kaggle.com/c/nlp-getting-started), I trained a K-Means model and an LDA model, and created a Jupyter notebook for easy use.

## Design
The goal of this project was to create a model to cluster tweets about various kinds of disasters.


## Data
I downloaded my dataset from a classification contest on [Kaggle](https://www.kaggle.com/c/nlp-getting-started), which consists of 7,613 tweets. 4,342 are labeled “safe”, while the other 3,271 are labeled “disaster”.

Unfortunately, not all disaster-labeled tweets actually refer to a disaster, which creates some clutter in the models. For future work, these unrelated tweets will be removed.

## Algorithms
While I did not use the "safe" tweets to construct my model, I conducted sentiment analyses of all tweets and compared the mean polarity and subjectivity across all "safe" and "disaster" tweets; the results are shown in my slide presentation.

During preprocessing, I included bigrams in the tokens, and left out tweets with fewer than 4 usable tokens. I also discarded tweets which had identical sequences of tokens - duplicates.


## Models
I considered K-Means clustering and LDA topic models, but settled on LDA because it produced more-coherent clusters.
I created my LDA model with max_df=0.075 and min_df=0.005, and after filtering out irrelevant words, ended up with 307 features. 
Using its topic matrix, I then created both soft and hard-clustering algorithms to apply to any text (preferably disaster tweets - the model isn't trained to cluster book-review tweets).

## Tools
Python's NLTK library for text tokenization and lemmatization
RegEx library for noise removal
SKLearn's TFIDF Vectorizer for preparing data for the K-Means model - I turned off 'use-idf' for the LDA model.
SKLearn's K-Means clustering model
Gensim for LDA topic modeling
Tablaeu for introductory chart
Matplotlib for sentiment analysis visualization


## Communication
In addition to my [slide presentation](https://docs.google.com/presentation/d/1WA35xEMQqyselISOzxbRZvcjmtO82lr01MzwaJElUu4/edit#slide=id.g101738fc30f_0_188), I created a secondary [Jupyter notebook](https://github.com/MK38993/Metis-Project-5---NLP/blob/main/NLP%205%20-%20Model%20Use.ipynb) to allow for easy use of the clustering model.










