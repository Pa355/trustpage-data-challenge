# trustpage-data-challenge
The coding exercise should be performed in Python 3 as a part of SDS challenge for Trustpage. The task is to develop an unsupervised method that can determine whether a movie review is positive or negative. The labels provided in the data set is used to evaluate your method.

# Introduction
Sentiment analysis, also popularly known as opinion analysis or opinion mining. The key idea is to use techniques from text analytics, NLP, Machine Learning, and linguistics to extract important information or data points from unstructured text. This in turn can help us derive qualitative outputs like the overall sentiment being on a positive, neutral, or negative scale and quantitative outputs like the sentiment polarity, subjectivity, and objectivity proportions.
Apart from supervised Learning, sentiment analysis also exists in Unsupervised Learning where tools/libraries are used to classify opinions with no cheatsheet, or already labeled output.

# Problem Statement
The main objective is to predict the sentiment for several movie reviews obtained from the Internet Movie Database (IMDb). This dataset contains 50,000 movie reviews that have been pre-labeled with “positive” and “negative” sentiment class labels based on the review content.



# Data
# Text Pre-processing
Removing html strips and noise text:
Removing special characters: 
Text stemming:
Removing stopwords: 

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

