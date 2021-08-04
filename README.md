# trustpage-data-challenge
The coding exercise should be performed in Python 3 as a part of SDS challenge for Trustpage. The task is to develop an unsupervised method that can determine whether a movie review is positive or negative. The labels provided in the data set is used to evaluate your method.

# Introduction
Sentiment analysis, also popularly known as opinion analysis or opinion mining. The key idea is to use techniques from text analytics, NLP, Machine Learning, and linguistics to extract important information or data points from unstructured text. This in turn can help us derive qualitative outputs like the overall sentiment being on a positive, neutral, or negative scale and quantitative outputs like the sentiment polarity, subjectivity, and objectivity proportions.
Apart from supervised Learning, sentiment analysis also exists in Unsupervised Learning where tools/libraries are used to classify opinions with no cheatsheet, or already labeled output.

# Problem Statement
The main objective is to predict the sentiment for several movie reviews obtained from the Internet Movie Database (IMDb). This dataset contains 50,000 movie reviews that have been pre-labeled with “positive” and “negative” sentiment class labels based on the review content.



# Data
# Text Pre-processing
# Methodology 
For this experiment, I’ll be using two sentiment analyzers in Python: Textblob and VaderSentiments.
The first step was to instantiate the analyzer to be used. Then a function was created to help analyze all the reviews using the respective analyzers. To capture the predictions for each analyzer, new columns were created in the dataframe by using the apply function to call the function created.

# Evaluation
For this experiment, we’ll be using 4 classification metrics: confusion matrix, accuracy score, precision, and recall.




