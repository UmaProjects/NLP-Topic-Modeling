# Topic Modelling:

Topic Modelling is different from rule-based text mining approaches that use regular expressions or dictionary based keyword searching techniques. It is an unsupervised approach used for finding and observing the bunch of words (called “topics”) in large clusters of texts.

# Data:

The dataset I am using here is a list of over one million news headlines published over a period of 15 years.

# Gensim:

Gensim is one of the extremly useful NLP library which was primarily developed for Topic Modelling.

#  Latent Dirichlet Allocation (LDA):

LDA is an example of topic model and is used to classify text in a document to a particular topic.

# Data Preprocessing:

!)Tokenization
2) Words less than 3 characters are removed.
3)stopwords are removed
4)lemmatization
5)Stemming

# Steps after Preprocessing:

	1)I am using Gensim library for preprocessing the text(using gensim.utils.simple_preprocess(text) method).
	2)After preprocessing, we create a dictionary of bag of words(Bag of words corpora in the Gensim library are based on dictionaries and contain the ID of each word along with the frequency of 		occurrence of the word).
		i) Using Gensim filter_extremes method, we are filtering out the tokens which appeared in less than 15 documents, more than 0.5(fraction of the total corpus size) and then keep only first 			100000 most frequent words.
		ii)For each document we create a dictionary reporting how many words and how many times those words appear using doc2bow method from Gensim
	3)Then create TF-IDF(Term frequency-Inverse Document Frequency) model object using TfidfModel class from models module in gensim.
	4)Train our lda model using gensim.models.LdaMulticore.
	5)Run LDA model with both bag of words and TF-IDF and evaluate the performance.











