# AIproject_tweeter

Step 1: Install and Import Libraries
Before analysis, you need to install textblob and tweepy libraries using !pip install command on your Jupyter Notebook.
# Install Libraries
!pip install textblob
!pip install tweepy
You need to import libraries that you will use in this sentiment analysis project.
# Import Libraries
from textblob import TextBlob
import sys
import tweepy
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
import os
import nltk
import pycountry
import re
import string
from wordcloud import WordCloud, STOPWORDS
from PIL import Image
from nltk.sentiment.vader import SentimentIntensityAnalyzer
from langdetect import detect
from nltk.stem import SnowballStemmer
from nltk.sentiment.vader import SentimentIntensityAnalyzer
from sklearn.feature_extraction.text import CountVectorizer
Tweepy supports both OAuth 1a (application-user) and OAuth 2 (application-only) authentication. Authentication is handled by the tweepy.AuthHandler class.
OAuth 2 is a method of authentication where an application makes API requests without the user context. Use this method if you just need read-only access to public information.
You first register our client application and acquire a consumer key and secret. Then you create an AppAuthHandler instance, passing in our consumer key and secret.
Before the authentication, you need to have Twitter Developer Account. If you don’t have, you can apply by using this link. Getting Twitter developer account usually takes a day or two, or sometimes more, for your application to be reviewed by Twitter.
Step 2: Authentication for Twitter API
# Authentication
consumerKey = “Type your consumer key here”
consumerSecret = “Type your consumer secret here”
accessToken = “Type your accedd token here”
accessTokenSecret = “Type your access token secret here”
auth = tweepy.OAuthHandler(consumerKey, consumerSecret)
auth.set_access_token(accessToken, accessTokenSecret)
api = tweepy.API(auth)
