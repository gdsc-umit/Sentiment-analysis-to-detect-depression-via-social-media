# Sentiment-analysis-to-detect-depression-via-social-media
<b> PROBLEM STATEMENT </b> <br> Social media platforms are becoming an integral part of people’s life. They reflect the user’s personal life. In recent years, messages and social media have ended up being a very close representation of a person's life and his mental state. This is a huge stockpile of data about a person's behaviour and can be used for detection of various mental illnesses (depression in our case) using Natural Language Processing. Hence, we used one such platform - twitter to identify the causes of depression and detect it. Twitter is the most suitable social media network for getting enough data and also to protect us from privacy laws.
Sentiment analysis intends to find the nature of text and classifies into positive, negative and neutral. Based on a curated word list, the tweets are classified as positive or negative.
The project aims to exploit machine learning techniques for conducting emotion analysis focusing on depression. For this purpose, we trained and tested classifiers to distinguish whether a user is depressed or not using features extracted from the activities in the network and tweets.

PHASE 1 
RESEARCH
Dataset
There are two kinds of tweets that are required at this project: random tweets that do not indicate depression and tweets that show the user may have depression. Both the datasets i.e. random tweets dataset and depressive tweets dataset could be downloaded from the kaggle website. 
Link for the depressive tweets dataset - https://raw.githubusercontent.com/eddieir/Depression_detection_using_Twitter_post/master/depressive_tweets_processed.csv
After reading some research papers about using different Machine Learning and artificial intelligence techniques to detect depression on Social Media, we decided to apply sentiment analysis through a powerful theorem. The model was written in python and it will tell whether a given tweet is depressive or not.

PHASE 2
PRE-PROCESSING
Tweets can be divided into 3 parts:
contains the people whom the tweet is intended to, denoted by “@”. ex: @Hickman.
contains the actual message.
contains the hashtag denoted by “#”.
Tweets are pre-processed to filter the first part and third part since they do not hold very less to zero significance in sentiment analysis. 



Later, the remaining message part of the tweet is pre-processed further for obtaining useful keywords which accounts much significance in identifying the emotions.
As an example: 
Before Cleaning:

After Cleaning:


After cleaning the data, we concatenated depressive and positive tweets, to generate a single CVS. 
Now,  a word cloud was generated with the most used keywords contained in depressive tweets. The words that caught our attention in these tweets are: Anxiety, depression, help, treatment, symptom, suffer, hard, issue, suffering, sleep, sad, suicide, struggle, severe, stress, feeling, emotional, food, illness. All these words in tweets are characteristic of depression.




PHASE 3
TRAINING & TESTING
In the training process, we had two tasks,
a. Creation of bag of words model
b. Creation of predictive model

a. Creation of bag of words model
In this model, a text like tweets is represented as the bag of its words, disregarding grammar and even word order but keeping multiplicity. 
The Bag-of-words model is mainly used as a tool of feature generation. The most common type of characteristics, or features calculated from the Bag-of-words model is term frequency, namely, the number of times a term appears in the text.
b. Creation of Predictive model
A total of 5 Predictive models were created, namely - Multinomial Naive Bayes, Random Forest Classifier, Logistic Regression, Gaussian Naive Bayes and Support Vector Machine. The data file will have two columns with one column representing whether the tweet is positive or negative and the other will contain the actual tweet. The column with tweets is pre-processed. The pre-processed data is used to create a bag of words model which will be used as training data to build the predictive models.
Testing
In the testing phase, the 30% of data is split randomly from the dataset and is tested on the predictive model. The test data is pre-processed and classified either positive or negative.



DEPLOYMENT OF MODEL
We have deployed our model on mia. 
A string input parameter is required which would be the tweet that needs to be analysed. The output indicates and prints whether the input tweet is depressive or non depressive. 

The link of the same can be found here: https://miamarketplace.com/apps/i3zM28I1GlEgh47X2mG0XhWpRxikx_YEOU6pu7KWUAYN 


FUTURE SCOPE
In future, we want to improvise the work with the same dataset but using deep learning techniques. 
Moreover, using a larger data with more number of tweets would give more accurate and efficient results. 
Depression can be detected in other features, such as the time when a person tweets. People with depression usually post late night tweets. There are many factors we can analyze in order to make better conclusions.
An extension for the project would be to detect early symptoms of depression and make a chatbot who can chat with the person and then contact the therapist. 
By analyzing depression in twitter posts, this machine learning model can give an individual insight into his/her mental health far earlier than traditional approaches.
We can use more models to do analysis of tweets and more social media outlets along with emails to determine various mental health issues other than depression such as PTSD, stress and anxiety.

CONCLUSION
We presented a novel approach word embedding for classification tasks to detect the depressive tweets from Twitter. Moreover, we have done a comparative analysis among all the 5 approaches. And among all these methods we found that Random Forest Classifier has the highest accuracy to detect the depressive tweets from twitter. 
The model works well in predicting tweets sentiment but it can get better with more data. 
This project can be considered as a step towards building a complete social media-based platform for analyzing and predicting mental and psychological issues and recommending solutions for these users. We would extend this step in the future by considering more ML models that are highly unlikely to over-fit the used data and find a more dependable way to measure the features’ impact.

