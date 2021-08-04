# trustpage-data-challenge
The coding exercise should be performed in Python 3 as a part of SDS challenge for Trustpage. The task is to develop an unsupervised method that can determine whether a movie review is positive or negative. The labels provided in the data set is used to evaluate the methods.

# Introduction
Sentiment analysis, also popularly known as opinion analysis or opinion mining. The key idea is to use techniques from text analytics, NLP, Machine Learning, and linguistics to extract important information or data points from unstructured text. This in turn can help us derive qualitative outputs like the overall sentiment being on a positive, neutral, or negative scale and quantitative outputs like the sentiment polarity, subjectivity, and objectivity proportions.
Apart from supervised Learning, sentiment analysis also exists in Unsupervised Learning where tools/libraries are used to classify opinions with no cheatsheet, or already labeled output.

# Problem Statement
The main objective is to predict the sentiment for several movie reviews obtained from the Internet Movie Database (IMDb). This dataset contains 50,000 movie reviews that have been pre-labeled with “positive” and “negative” sentiment class labels based on the review content.

# Data
The IMDB movie reviews dataset for this study contains 50,000 reviews — 25,000 positive and 25,000 negative reviews.

![image](https://user-images.githubusercontent.com/44107697/128204751-095c4ea3-1955-48fb-91a8-e6c0c1d97f1d.png)


# Text Pre-processing

Removing html strips and noise text: This removed the unnnecessary html links and noise from the data.

Removing special characters: This removes special characters like #,(,/, etc in order to retain only text.

Text tokenization and stemming: We will represent our data as a collection of words or tokens; we will also be performing word-level preprocessing tasks such as stemming. To achieve this, we'll utilize the natural language toolkit, or nltk. Stemming is a technic that reduces the inflectional forms, and sometimes derivationally related forms, of a common word to a base form.

Removing stopwords: A stop word is a commonly used word (such as “the”, “a”, “an”, “in”) that a search engine has been programmed to ignore. Removal of stop words is important as it reduces the dataset size and thus reduces the training time due to the fewer number of tokens.

WordCloud: WordCloud higlights based on the frequency of the words in both positive (worth, realism, etc) and negaitive (bad, worst, etc)reviews.

# Methodology 
For this experiment, I’ll be using two sentiment analyzers in Python: Textblob and VaderSentiments.
The first step was to instantiate the analyzer to be used. Then a function was created to help analyze all the reviews using the respective analyzers. To capture the predictions for each analyzer, new columns were created in the dataframe by using the apply function to call the function created.

# Evaluation
For this experiment, we’ll be using 4 classification metrics: confusion matrix, accuracy score, precision, and recall.
			
![image](https://user-images.githubusercontent.com/44107697/128193240-e71e0115-86a2-4f73-8be2-601f4f19d2b0.png)

# Interpretation from Results
For accuracy, the analyzer hit 65% for VADER; that is, for every 100 reviews it classified/predicted, 65 were correctly classified.

For precision, the VADER analyzer has a rate of 0.61 for positive reviews. This means that out of all the reviews the analyzer predicted as positive, 61% of them were actually positive reviews.

For recall, the TextBlob analyzer has a rate of 0.89 for positive reviews. This means that out of all the actual positive reviews, only 89% were correctly predicted.		

# Conclusion
Both the analyzers have overall good recall rate. However, the business situation of the problem statement will provide more insight as to what metric is more important for them to consider and the features can then be fine tuned to acieve that. This is only a first attempt and the performance of these analyzers used may be improved by feature engineering before analyzing.

The supervised models have proved to performed very robustly for this dataset. I have not included it in the analysis to respect and aligh with the question being asked to complete the assessment.

