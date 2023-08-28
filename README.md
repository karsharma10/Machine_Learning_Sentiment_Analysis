#### Sentiment Analysis


## Problem Space:

Our problem space is predicting the sentiment value of short-text trained on a dataset of Tweets. In the training data we have, the sentiment value of a Tweet was based on several metrics. Most importantly to point out, it was not based on emoticons, which were stripped from the Tweets before training. The range of predictions is on a scale of 0-4, 0 being negative sentiment, and 4 being positive sentiment. As there are 1.6 million tweets with this associated sentiment value, we have some great training and validation data, with which we think we can train a powerful model to predict the sentiment of other text under 250 words. Specifically, we will target Amazon reviews as our test data. 

This is different from what was done before, such as Kaggle, because we are going to be using the Twitter dataset to fit our model and then use that already fitted model to predict the Amazon reviews dataset to get predicted sentiment values. This adds value and novelty to the use of this dataset because we are extrapolating its use to other real-world applications. Because people are sometimes too honest on Twitter, we felt that the sentiment of these Tweets would be a great baseline to predict other sentiments of short-text.

## Approach:

Our approach to solve this problem was to first ‘clean’ the Twitter dataset. First and foremost, we turned this problem into a binary problem by going through the dataset and selecting where the sentiment value of the tweets that were either equal to zero or four. Where zero is negative and four is positive. This is because we aren’t very interested in predicting or training on ‘neutral’ Tweets, because detecting negative or positive sentiment provides the most value. Once we had a dataset composed of only binary sentiment values we then removed all unnecessary columns and only kept the sentiment value and the text of the Tweet which we converted to lowercase. We then removed stopwords, usernames, URLs, and non-alphabets from the Tweet column of the dataset. After that, we tokenized our text column, stemmed the text, and did lemmatization. For the Amazon reviews, we cleaned it the same way as we did the Tweet dataset, except the Amazon reviews dataset’s sentiment values (scores), which ranged from one to five, so we only took the one and five scored reviews. (Where one is negative and five is positive). Finally, we performed TFIDF on the text (Tweets) column and then fitted our model. 
We then predicted the aforementioned training and validation data to confirm our accuracy. We did this by predicting and fitting our model using the Twitter dataset using KNN, to be able to tweak the parameters and test how well the model was doing. It didn’t perform well, so we then tried using logistic regression which performed far better after some change in the parameters, so we decided to go with that as our model. 
Once we had our model fitted using the Twitter dataset with logistic regression, we then used our ‘cleaned’ Amazon reviews dataset to predict the sentiment value on the Amazon reviews using the previously fitted model on the Twitter dataset. 
	Our overall goal is to be able to detect sentiments from text from any source. This kind of research is useful for fake news detection, marketing, business analytics, and much more. It especially can be useful for product vendors who want to discern the approval of a product they have put on the market. This can also be used for advertisement selection for users in the current day and age of big data.
	This fits into a broader understanding of machine learning because we do not need to specifically fit and predict a model on the same dataset to get results. Often, the most meaningful and valuable results are a product of training on some labeled data, and using that to predict on some unknown. There will be cases where you can be given a similar dataset and need to predict new labels off that set. Being able to train a model with good hyperparameters that can work for other data as well is a very important skill. 



