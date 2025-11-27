# Notes  
NLP is part of AI Engineering course and I try some hands on with some NLP concepts like text processing, identifying speech and named entities, sentiment analysis,
vectorizing text, topic modelling, etc. And Finally work on course project. 

## Text Processing
Its important to preprocess data in order to feed high quality data into our ML algorithms. If you provide unprocessed data into the algorithm, its accuracy and efficiency will be low. Because unprocessed data contains noise. There are a number of steps involved in pre-processing our text data and getting it ready for further analysis.The first step is just general cleaning.So taking our data set, getting it organized, tidying up the text, you know, removing anything that
might throw us an error, anything like that.The second step is removing noise from our data set.So if we've got aspects in our data that aren't adding any value and they're just taking up space in memory, we can remove these and we'll be left with a smaller, cleaner dataset to work with.The third step is just getting that data in the right format for the machine learning algorithm we want to use.

- Lower casing: converting text data to lower case so that the machine treats data consistently. But its important to understand the difference between some words like US= United States and us=you and me. ```.lower()``` is used for turning text to lower case. This method works just not only for one sentence but  on any string.
- Removing stop words: In a sentence we use prepositions, conjunctions and other glue words to form a sentence. Those are stop words which doesn't have much sense for machine learning and natural language processing but are necessary to form a sentence. By removing them, we simplify the text and end up with a smaller, cleaner data set that's easier to process and often more useful for analysis. For which we use the ```nltk.download('stopwords')``` of NLTK package.NLTK considers Stopwords in English. In the exercise we have the list of stop words, check that to see what stop words will be removed from the sentence. There are some stop words for example **not** and **doesn't**, etc which adds value to the context -> negative sentiment for instance. Its possible to remove them from the list: ```en_stopwords.remove("not")```.
- Regular expressions: Regular expression is special way to write patterns, to search through text.Regex lets you describe a rule like any three numbers in a row, or any word that starts with a capital letter.With regex, you can **find filter and check text** based on the pattern you define. Some common functions to remember:
  - ```re.search()```: searches whether a specified pattern appears within a string
  - ```re.sub()```: searches a specific text within a string, and replaces it with new content.
  - ```re.split()```: function returns a list where the string has been split at each match.
- Tokenization: Breaking text into smaller units. This process is called tokenization. Smaller units -> **tokens**. Which can be words, sentences, subwords, characters. In order to tokenize sentences we use the package : ```nltk.download('punkt_tab')```, table used to figure out where sentences begin and end.
**word_tokenize, sent_tokenize**: In word_tokenize the individual words are tokenized output:list of word tokens, or sometimes characters, sent_tokenize: individual sentences are tokenized output:list of sentences.
- Stemming: reduces words to their base form. f.e connected, connecting -> connect. It works by chopping of endings or suffixes. Stemming reduces number of unique words.Reduces complexity and keeps dataset easier to manage. The Porter stemmer is a classic rule based algorithm that reduces English words to a simpler base ```from nltk.stem import PorterStemmer```.
- Lemmetization: reduces a word to meaningful baseform while preserving its meaning. WordNet is an extensive lexical database of English.
Basically a built in dictionary that the Lemmatizer uses to make sure the base forms it produces are real words.Then import the WordNet lemmatizer from NLTK.
- N-grams: N-gram helps us analyze relationship between neighboring words. Its sequence of N-tokens. How many words are grouped. When N=1, Unigram. When N=2,Bigram, when N=3,Trigram.

## Speech Tagging and Named Entity Recognition  
Two types of tagging - 1. Parts of Speech tagging 2. Named entity recognition.  
- **Parts of Speech:** Where we take each of our tokens and tag them with the associated parts of speech. Parts of speech we mean whether that token is a verb, a noun, an adjective, etc.  
 - **Named Entity Recognition:** The second method is named entity recognition.So instead of going through each of the tokens and tagging them, this method searches through our text and pulls out named entities. For example: person, location, ordinal, geopolitical.

## Sentiment Analysis

## Vectorizing Text

## Topic Modelling

