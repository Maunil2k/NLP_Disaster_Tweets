# Natural Language Processing with Disaster Tweets
<img align="right" width="200" height="300" src="https://storage.googleapis.com/kaggle-media/competitions/tweet_screenshot.png">
<p align="left">
Twitter has become an important communication channel in times of emergency.
The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies). But, it’s not always clear whether a person’s words are actually announcing a disaster.</p><br />
<p align="left">
Take this example shown on right, the author explicitly uses the word “ABLAZE” but means it metaphorically. This is clear to a human right away, especially with the visual aid. But it’s less clear to a machine.
</p><br/>
<p align="left">
In this competition, the challenge was to build a machine learning model that predicts which tweets are about real disasters and which one’s were not. It consists a dataset of 10,000 tweets that were hand classified. 
</p><br/>

# Approach
Since this is one of my few beginner level competitions in the domain of Natural Language Processing(NLP), I decided to keep things pretty simple i.e. I did simple data cleaning by removing punctuation marks, HTML tags, emojis and converting every characters to lower case. Next, I created a simple BiLSTM based 6 layered RNN using tensorflow-keras which resulted in 876,577 parameters. After the text was cleaned, the dataset was tokenized to a max length of 256 tokens. The model was then trained with validation split of 20% for 100 epochs with callbacks, but the training eventually stopped after 28th epoch due to deteriorating validation loss.

# Results
The training accuracy was 88.26% whereas the validation accuracy was 74.98%. Similarly, the training loss recorded was 0.3785 whereas validation loss recorded was 0.5974. <br/>
<img align="right" width="500" height="300" src="https://github.com/Maunil2k/NLP_Disaster_Tweets/blob/master/images/model_accuracy.jpg">
<img align="left" width="500" height="300" src="https://github.com/Maunil2k/NLP_Disaster_Tweets/blob/master/images/model_loss.jpg">
