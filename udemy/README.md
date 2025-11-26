# Notes  
NLP is part of AI Engineering course and I try some hands on with some NLP concepts like text processing, identifying speech and named entities, sentiment analysis,
vectorizing text, topic modelling, etc. And Finally work on course project. 

## Text Processing
Its important to preprocess data in order to feed high quality data into our ML algorithms. If you provide unprocessed data into the algorithm, its accuracy and efficiency will be low. Because unprocessed data contains noise. There are a number of steps involved in pre-processing our text data and getting it ready for further analysis.The first step is just general cleaning.So taking our data set, getting it organized, tidying up the text, you know, removing anything that
might throw us an error, anything like that.The second step is removing noise from our data set.So if we've got aspects in our data that aren't adding any value and they're just taking up space in memory, we can remove these and we'll be left with a smaller, cleaner dataset to work with.The third step is just getting that data in the right format for the machine learning algorithm we want to use.

- Lower casing: converting text data to lower case so that the machine treats data consistently. But its important to understand the difference between some words like US= United States and us=you and me. ```.lower()``` is used for turning text to lower case. This method works just not only for one sentence but  on any string.
- Removing stop words: In a sentence we use prepositions, conjunctions and other glue words to form a sentence. Those are stop words which doesn't have much sense for machine learning and natural language processing but are necessary to form a sentence. By removing them, we simplify the text and end up with a smaller, cleaner data set that's easier to process and often more useful for analysis. For which we use the ```nltk.download('stopwords')``` of NLTK package.NLTK considers Stopwords in English. In the exercise we have the list of stop words, check that to see what stop words will be removed from the sentence. There are some stop words for example **not** and **doesn't**, etc which adds value to the context -> negative sentiment for instance. Its possible to remove them from the list: ```en_stopwords.remove("not")```.
- Regular expressions:
- Tokenization
- Stemming
- Lemmetization
- N-grams

## Speech Tagging and Entity Recognition

## Sentiment Analysis

## Vectorizing Text

## Topic Modelling

