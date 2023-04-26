#### Machine Learning Project

Our problem space is predicting sentiments of text, and in this case specifically tweets. In the training data we have, the sentiment value of a tweet was based on whether the tweet had a smiley or frowny face. This rather deterministic metric was then removed from the tweet and the predictions were made again. The range of predictions is on a scale of 0-4, 0 being negative sentiment, and 4 being positive sentiment. As there are 1.6 million tweets with this associated sentiment value, we have some great training and validation data, with which we think we can train a powerful model to predict the sentiment of other text under 250 words. Specifically, we will target Amazon Reviews as our test data.
Our dataset comprises of 1.6 million entries (tweets). Each entry has six features, one for target which is the sentiment value, the id of the entry which is the number associated with that tweet, the date of that tweet, the flag of the tweet, the user who typed the tweet, and the actual text of the tweet. Out of these six features, the most crucial features are the target (sentiment value), id of the tweet, and the text of the tweet. The outcome variable of this project will be the target (sentiment value) since this is what we are trying to predict. These features are not just crucial, but also important for building a relatively simple model within the constraints of the semester. Further down the line we can add other features from the training model to add complexity and value to our predictions.
	Our approach to this problem will be as follows: train a model on the tweets with their associated sentiments from the tweets with emojis removed. We then will predict on the aforementioned training and validation data to confirm our accuracy. Once this accuracy reaches a sufficient level, we will subsequently train a model on test data that is completely novel to our model. This will most likely be reviews from Amazon, or some source of short text responses under 250 characters to not completely deviate from the original model, but provide a new direction for us to move in. Our overall goal is to be able to detect sentiments from text under 250 characters from any source, without needing an emoji to make our predictions. This kind of research is useful for fake news detection, marketing, business analytics, and much more. It especially can be useful for product vendors who want to discern the approval of a product they have put on the market. This can also be used for advertisement selection for users in the current day and age of big data.
