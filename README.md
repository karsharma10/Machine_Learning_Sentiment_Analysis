
### Sentiment Analysis of Short Text: Predicting Twitter and Amazon Reviews

**Problem Space:**

In this project, our focus revolves around the challenging task of sentiment prediction for short-text content, utilizing a dataset predominantly comprised of Tweets. The sentiment labels assigned to each Tweet were determined by a combination of metrics, with a noteworthy emphasis on the exclusion of emoticons—a deliberate choice made to ensure a more comprehensive analysis. The spectrum of sentiment predictions ranges from 0 to 4, with 0 representing negative sentiment and 4 indicating a positive sentiment. With an extensive dataset of 1.6 million Tweets, each with associated sentiment values, we possess a robust foundation for training a potent model capable of predicting sentiments for various texts under 250 words. Our test data includes Amazon reviews, chosen for their suitability in assessing the model's performance.

Diverging from conventional methodologies, such as those typically employed in Kaggle competitions, our approach entails using the Twitter dataset to train our model. Once trained, the model is applied to predict sentiment values within the Amazon reviews dataset. This innovative approach imbues the Twitter dataset with enhanced value, extending its application beyond its original context to real-world scenarios.

**Approach:**

Our journey begins by meticulously cleaning the Twitter dataset. We first transform the problem into a binary classification task, focusing on Tweets with sentiment values of either 0 (negative) or 4 (positive). Our data refinement involves removing extraneous columns, retaining only the sentiment value and the lowercase text of each Tweet. This text is then subjected to preprocessing steps including the removal of stopwords, usernames, URLs, and non-alphabetic characters. Tokenization, stemming, and lemmatization further refine the text. Similar cleaning procedures are applied to the Amazon reviews dataset, which comprises sentiment scores ranging from 1 to 5 (where 1 is negative and 5 is positive).

The key steps in our approach include performing TF-IDF (Term Frequency-Inverse Document Frequency) on the text column, followed by model fitting. We experiment with different algorithms, starting with K-Nearest Neighbors (KNN) for initial testing. However, its performance falls short of our expectations. We subsequently explore logistic regression and achieve considerably improved results after refining parameter settings.

The model that emerges from this process is initially fitted using the Twitter dataset and logistic regression. This fitted model is then applied to the 'cleaned' Amazon reviews dataset to predict sentiment values. Our overarching goal extends beyond individual prediction to the broader domain of sentiment detection from text across diverse sources. This research holds value in applications like fake news detection, marketing strategies, business analytics, and product approval assessment. It is particularly relevant in today's era of data-driven decision-making and personalized advertising.

This endeavor aligns with the broader context of machine learning, as it demonstrates the power of training on one dataset and predicting on another to yield meaningful insights. It underscores the importance of building versatile models with optimized hyperparameters that can perform effectively on varied datasets—a crucial skill in the realm of machine learning.

Join us on this voyage as we delve into sentiment analysis, unraveling the nuances of predicting emotions from succinct text and extrapolating its applicability to real-world challenges. Feel free to explore our codebase and methodology to gain a deeper understanding of this pioneering project.



