# Metis Project 5: Disaster Tweets

The goal of this project is to analyze the differences between literal usage of "disaster keywords" and metaphorical usage.

In order to begin analysis, I collected several thousand tweets with "disaster keywords" from [Kaggle](https://www.kaggle.com/vstepanenko/disaster-tweets) and divided them into "literal disaster" and "metaphor" groups. For each group, I applied CountVectorizer and TFIDFVectorizer (ignoring stop words) to each, then tallied the count/importance of each word for each class.

Next, I saved the 1000 most common/important words into CSV files, which can be found in this repository.

["Safe" tweets - CountVectorizer](https://github.com/MK38993/Metis-Project-5---NLP/blob/main/safe_1000_words.csv)
["Disaster" tweets - CountVectorizer](https://github.com/MK38993/Metis-Project-5---NLP/blob/main/disaster_1000_words.csv)
["Safe" tweets - TFIDFVectorizer](https://github.com/MK38993/Metis-Project-5---NLP/blob/main/safe_1000_words_tf.csv)
["Disaster" tweets - TFIDFVectorizer](https://github.com/MK38993/Metis-Project-5---NLP/blob/main/disaster_1000_words_tf.csv)

The top 10 terms for each category can be found below.

## Preliminary Analysis
The top words in "disaster" tweets convey more concrete ideas than those in "safe" tweets, which often speak in the first person with more casual language.

### "Safe" tweet top word usage - out of 4342 tweets
|Word|Count|Percent Usage|
|-|-|-|
|like|253|1.82%
|i'm|244|1.76%
|just|234|1.69%
|[&]|209|1.51%
|new|170|1.23%
|don't|142|1.02%
|body|113|0.81%
|video|96|0.69%
|people|93|0.67%
|got|92|0.66%

### "Disaster" tweet top word usage - out of 3271 tweets
|Word|Count|Percent Usage|
|-|-|-|
|news|140|1.26%
|[&]|135|1.22%
|disaster|118|1.06%
|california|11|1.00%
|suicide|110|0.99%
|police|107|0.97%
|people|105|0.95%
|killed|93|0.84%
|like|92|0.83%
|hiroshima|90|0.81%


My next step is to filter out terms before topic modelling. For example, words like 'and' were automatically  by the 'stop words' argument during vectorization, but not '&'.






