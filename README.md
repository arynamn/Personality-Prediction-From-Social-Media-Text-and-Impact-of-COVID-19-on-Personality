# Personality Prediction From Social Media Text  and   Impact of Covid-19 on personality
## Introduction
Personality-Prediction-From-Social-Media-Text is my BTech final Year project under the guidance of Prof. Amitabha Acharaya, HITK, Kolkata.<br/>
My group member in this project were : Anisha Chhetri, Ankit Kumar, Abhisekh. <br/>
Under the guidance of the professor, I extended the same project to understand the impact of covid-19 on the personality. </br>

## Abstract
Personality has been studies extensively in social science and psychology as it reflects the way people behave and react in online social media and in the society. For instance, it correlates with music taste, Extroverted people tend to like popular music, while open to experience people are more likely to enjoy unpopular one. Personality is also related to the formation of social relations, the pages that people like on Facebook, and the language that people use to communicate. <br />
People are increasingly using social media platforms, such as Twitter, Facebook, and Pinterest, to share their thoughts and opinions with their friends or people who are interested. Such scale of social media platforms provides us with an unprecedented opportunity to understanding psychological attributes on a large user base. In this project, we want to analyse and predict personality by constructing a bridge between personality and language in popular social media such as Twitter. Specifically, we aim to find the linguistic features that distinguish people with different personality types and explore how these features can be explain by personality. Further, using the these features we want to understand the degree to which we can predict personality traits from social media language.<br />
	However, little research has touch upon understanding personality through social media because of a few reasons. First, language on social media has richer content that makes the typical linguistic analysis tool perform poorly. For example, Twitter, an online social networking service that enables users to send and read short 140-character messages called “tweets”, contains many Twitter specific language such as hashtag (#), at-mention (@), URL, and emoticons. People tend to use shorten version of phrases on Twitter, for example, “iono” means “I don’t know”. Twitter poses additional challenges due to the conversational nature of the text, the lack of conventional orthography, and 140-character limit of each message (tweet).<br />
	 In this project, we try to solve the aforementioned problem by designing new richer linguistic analysis tools which can extract language feature in social media context and introducing a mechanism to automatically extract personality from text in social media. Using Twitter as a case study, we investigate the relationship between language features in tweets and personality traits, which leads to further experiment in predicting personality from language. <br />
   The outbreak of Covid-19 and the precautionary strategies have drastically impacted our lives in all dimensions. These may have an impact in our psychology too. In this study we have examined whether this pandemic have affected Five Factor Model personality traits using deep learning based document modeling. Using five different deep learning models we have analyzed tweeter data following the pretest posttest design.<br /><br />


## Requirements :
Language - Python3 <br />
Machine Learning Tools - Tensorflow, Scikit-Learn. <br />
Natural Language Processing Tools and Utilities - NLTK, spaCy, Gensim + Word2Vec(Google News Vectors), NRCEmotions Lexicons.<br />
Other Libraries - Pandas, Tweepy, Matplotlib<br />

## Specification :


Store the essays.csv and nrc_emotions_lex.xlsx in the inputs folder

## Dataset :
Training and Development - essays.csv [4] dataset by J.W. Pennebaker and L.A. King <br />
Testing - Social media text extracted from Twitter <br />

## Project Details
This project is mainly divided into 4 major components: <br />
1. Extracting texts from Twitter : We store the twitter ids of required number of users in input_files/twitter_ids.json along with the countries they belong to. We then use the extractor script to fetch tweets using tweepy and store them in json script. We have compiled input_files/country_dates.json which store the date around which lockdown was imposed in their respective countries. We use this to store the tweets of an individual before and after COVID-19 lockdown separately keeping a week margin.
2. Processing the texts using NLP tools : We use various natural language processing techniques to clean and extract relevant features from text. We process the essays.csv  as well as the extracted tweets. Although there is a slight difference in their processing eg. the essays dataset does not require removing links and mentions present in twitter. Texts from twitter create stronger challenges for nlp tools as it contains many irregularities.
3. Preparing Machine Learning Models and apply them to extracted texts : We use Google-news-vectors to extract embeddings for the texts. We use these embedding as input to various ML models. We trained and tested the models using the Pennebaker essays dataset and applied them to the extracted tweets. We tried CNN based Neural Network using Tensorflow,  Naive Bayes, Logistic Regression, SVC, Random Forest Classifier using SKlearn.
4. Compilation and Analysis : We compile the results from various models and analyse the predictions to study the effect of Covid-19

![image](https://user-images.githubusercontent.com/83718299/129464825-da79f464-3ea8-48ec-b149-30f0f8269dce.png)

## References :
[1] Karsten J, Penninx BW, Riese H, Ormel J, Nolen WA, Hartman CA. The state effect of depressive and anxiety disorders on big five personality traits. JPsychiatr Res. 2012;46:644–50. pmid:22349302

[2] Roberts BW, Luo J, Briley DA, Chow PI, Su R, Hill PL. A systematic review of personality trait change through intervention. Psychol Bull. 2017;143:117–41. pmid:28054797

[3] Navonil Majumder, SoujanyaPoria, Alexander Gelbukh, Erik Cambria. “Deep Learning-Based
Document Modeling for Personality Detection from Text”, IEEE Intelligent Systems (Volume: 32, Issue: 2, Mar.-Apr. 2017)

[4] J.W. Pennebaker and L.A. King, “Linguistic Styles: Language, Use as an Individual Difference,” J. Personality and Social Psychology, vol. 77, no. 6, 1999, pp. 1296–1312.

[5]  Nazar Akrami, Johan Fernquist, Tim Isbister, Lisa Kaati, Björn Pelzer, “Automatic Extraction of Personality from Text: Challenges and Opportunities”,   2019 IEEE International Conference on Big Data (Big Data).

[6] Saif M. Mohammad, Sentiment Analysis: Automatically Detecting Valence, Emotions, and Other Affectual States from Text. https://arxiv.org/pdf/1308.6297.pdf


