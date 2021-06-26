# Project3
This contains all the stuff for Project3
## Problem Statement
KiddyToy sells wonderful and liable children toys. From last year, KiddyToy made decision to move their business online and also provided online customer feedback service. Customer service team will categorize customer's feedback as "customer complain" or "customer support". This increases company's revenue significantly. However, KiddyToy faces the problem that receive drastic amount of customer feedback each day. The current system only allows employees to categorize customer feedback manually which is time-consuming. As the company's data science team member, we initialize a project to build up a text classifier to automate this process.

## Executive Summary
It's estimated that around 80% of all information is unstructured, with text being one of the most common types of unstructured data. Because of the messy nature of text, analyzing, understanding, organizing, and sorting through text data is hard and time-consuming. KiddyAce's customer service team faces the same issue.

In this project, we develop a text classifier to help KiddyAce's customer service team. We select two subreddits, /r/Coffee and /r/Tea from reddit website. The choice of these two subreddits is motivated by their text-heavy posts. The goal of this project is to classify which subreddit a given post came from. We create and compare two models: logistic regression and naive Bayes classifier and choose the best model. Our best model can perform well with a test accuracy score of 92.05%.

By using this text classifiers, customer service team can automatically structure texts from customer feedback in a fast and cost-effective way. This allows companies to save time analyzing text data, automate business processes, and improve customer satisfaction.

## Table of Contents
1. [Project Files](#../data)
2. [Data Dictionary](#../data)
3. [Model Selection](#Model-Selection)
4. [Conclusion and Recommendations](#Conclusion-and-Recommendations)

## Model Selection
### 1st round Model Verification - Apply selected features
Model Name | Vectorizer |Train Score|Test Score|Train/Test Score gap
-|-|-|-|-
Logistic Regression|CountVectorizer|99.5%|91.8%|7.7%
Logistic Regression|TfidfVectorizer|97.1%|91.6%|5.5%
Naive Bayes|CountVectorizer|96.2%|90.8%|5.4%
Naive Bayes|TfidfVectorizer|96.7%|90.6%|6.1%

### 2nd round Model Verification - Add power 2 features
Model Name | Vectorizer |Train Score|Test Score|Train/Test Score gap
-|-|-|-|-
Logistic Regression|CountVectorizer|99.1%|91.2%|7.9%
Logistic Regression|TfidfVectorizer|97.2%|91.4%|5.8%
Naive Bayes|CountVectorizer|94.2%|90.4%|3.8%
Naive Bayes|TfidfVectorizer|96.6%|92.1%|4.5%

## Conclusion and Recommendations
Our naive Bayes classifier performed well with a test accuracy score of 92.05%. This is expected due to two similar subreddit topics we chose. There are many common words in their top20 words list, like 'cup', 'brew','taste', 'water' etc.
However, it still can be a good classifier for customer service team to categorize customer feedback with high accuracy.

There are still space for improvement for this classifier:

Optimize stop words, for example to identify the common words for these two topics and add into stopwords.
Try ensemble models, such as random forest classifier
May consider to model more than two topics to improve user's satisfaction.

## Reference
[1] https://towardsdatascience.com/text-classification-applications-and-use-cases-beab4bfe2e62                                                                                 
[2] https://towardsdatascience.com/generative-vs-2528de43a836                                                                                                                 
[3] https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html                                                                                   
[4] https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html
