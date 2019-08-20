# Emotion Recognition in tweets
## Summary:
```
Submitted to: Project Showcase Challenge of Udacity and for the study group, #sg_caffeine_coders.
Usecase: It is used to recognize emotions from texts. 
Dataset: EmotionIntensity Dataset by WASSA-2017
Implementations: Federated learning along with GRU and LSTM are used.
```

## Objective 
Ever felt confused reading what others' are writing about what they want to say??? Wouldn't it be an amazing thing if we already get the emotion of someone just by reading their texts? Then, this project of ours will come handy for you. Here, we used *Gated Recurrent Unit* to recognize people's emotions from what they write on social media. However, we all understand how much privacy is important to everyone and by keeping that in mind, we used *Federated Learning* to secure user privacy. 

*This project was created during the Udacity Facebook Secure & Private AI challenge scholarship and is covering the topic 'Emotion Recognition in text'
which is the process of identifying human emotion in text messages like tweets on [Twitter](https://twitter.com/home).*

<!---For the data we used a dataset given WASSA-2017 Shared Task on Emotion Intensity.--->

<!--- The project will be submitted to the [Project Showcase Challenge](https://sites.google.com/udacity.com/secureprivateai-challenge/community/project-showcase-challenge#h.p_E1Kba6yZtw4O)     
by Udacity and to the study group #sg_caffeine_coders project challenge. --->


## Dataset
We used 
[EmotionIntensity Dataset](http://saifmohammad.com/WebPages/EmotionIntensity-SharedTask.html) for our project where the data is collected from twitter.

An interactive visualization of the Tweet Emotion Intensity Dataset is here:
[Interactive Dataset](http://saifmohammad.com/WebPages/TweetEmotionIntensity-dataviz.html)

The dataset provides a trainings set, a development set, and a test set and on each set it contains the information of a user's tweet, its emotion and the intensity. Four different emotions were marked for the emotion data which are *Happy, fear, joy and, sadness*.

For our project, we used the training dataset to train our model and testing dataset to check our accuracy. Besides, we did various proecessing of the data which will be discussed in detail on *Data Cleaning* section.

#### Reference:
WASSA-2017 Shared Task on Emotion Intensity. Saif M. Mohammad and Felipe Bravo-Marquez. In Proceedings of the EMNLP 2017 Workshop on Computational Approaches to Subjectivity, Sentiment, and Social Media (WASSA), September 2017, Copenhagen, Denmark.BibTex

## Data Cleaning
The data cleaning is necessary to improve the quality of the data to work with.
The text will be cleaned from extra unnecessary characters like '@' or '#' which are often used in Twitter tweets.
Also, links and unreadable not interpretable characters are removed. All words are put in lowercase.

## Data Preprocessing
In the preprocessing part the tweets are split into smaller pieces, or tokens. The process itself is called tokenization.
A dictionairy is created to map words to index and then create the input tensors for the neural network.


## Machine Learning Model


## Federated Learning


## Deployment
The deployment should be done with FLASK. It will load a screen where it is possible to enter a message. After submitting, the message will be analyzed.
When finished analyzing, it will show the results screen, saying the percentage of each emotion the message is carrying.
For now the Machine Learning Model is not implmented in the deployment code, It will only show the screens.

Currently, the application will scrape Twitter data and analyze it. 

## Code Reference 
1.[Raw Dataset Emotion Detection Tweets](http://saifmohammad.com/WebPages/EmotionIntensity-SharedTask.html)
2.[Facebook Color Set](https://encycolorpedia.de/3b5998)
3.[Cleaning Data](https://towardsdatascience.com/another-twitter-sentiment-analysis-bb5b01ebad90)
4. [Udacity Facebook Secure and Private AI Scholarship Challenge Course](https://www.udacity.com/facebook-AI-scholarship)
5. REFERENCE
