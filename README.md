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
When we tweet or chat, we tend to be using various characters which are not part of English alphabets. However, in Natural Language Processing, it is really hard for the model to learn from data when it contains so many versatile characters and doesn't produce a good accuracy on that. So, to improve our accuracy we cleaned the data in the following process:
1. We removed the unnecessary characters like '@' or '#' which are pretty common in Twitter tweets.
2. We also removed links as those don't bear any meaning without the content.
3. We also removed all the unreadable characters and converted all the texts into lowercase.

For further clarity, we shared our Data Cleaning Code(https://github.com/rupaai/caffeine_coders_emotion_detection/blob/master/Training_Dataset_Cleaning.ipynb) here.

## Data Preprocessing

In Natural Language Processing, we can't directly feed the data as input to a model like we can do for any computer vision model. To turn the words into learnable input data, we used the following data preprocessing steps:
1. At first the tweets are split into words which are called tokens here, this process is known as *Tokenization*.
2. Later, we we used nltk word2vec model to convert the words into vector dictionary which is turned into a tensor as the input of the model.


## Model Structure
For model, we used a *Gated Recurrent Unit(GRU)* model which is a *6-Layer* neural network where first 2 layers are used as reset gate, next 2 layers are used as update gates and the last 2layers are used as new gates.

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
5. [Modified GRU - Federated Learning](https://github.com/andrelmfarias/Private-AI/blob/master/Federated_Learning/handcrafted_GRU.py)
6. [Our query on Openmined slack about the federated learning issue](https://openmined.slack.com/archives/C6EEFN3A8/p1566138140348300)
