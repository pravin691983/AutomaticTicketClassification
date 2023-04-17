# Automatic Ticket Classification

> In this case study, we will create a model that can automatically classify customer complaints based on the products and services that the ticket mentions.

## Table of Contents

- [Overview Business Understanding](#overview-business-understanding)
- [Problem Statement Business Objectives](#problem-statement-business-objectives)
- [Data in depth](#data-in-depth)
- [Approach](#approach)
- [Technologies Used](#technologies-used)
- [Conclusions](#conclusions)

<!-- You can include any other section that is pertinent to your problem -->

## Overview Business Understanding

For a financial company, customer complaints carry a lot of importance, as they are often an indicator of the shortcomings in their products and services. If these complaints are resolved efficiently in time, they can bring down customer dissatisfaction to a minimum and retain them with stronger loyalty. This also gives them an idea of how to continuously improve their services to attract more customers.

These customer complaints are unstructured text data; so, traditionally, companies need to allocate the task of evaluating and assigning each ticket to the relevant department to multiple support employees. This becomes tedious as the company grows and has a large customer base.

In this case study, you will be working as an NLP engineer for a financial company that wants to automate its customer support tickets system. As a financial company, the firm has many products and services such as credit cards, banking and mortgages/loans.

## Problem Statement Business Goal

You need to build a model that is able to classify customer complaints based on the products/services. By doing so, you can segregate these tickets into their relevant categories and, therefore, help in the quick resolution of the issue.

With the help of non-negative matrix factorization (NMF), an approach under topic modelling, you will detect patterns and recurring words present in each ticket. This can be then used to understand the important features for each cluster of categories. By segregating the clusters, you will be able to identify the topics of the customer complaints.

You will be doing topic modelling on the .json data provided by the company. Since this data is not labelled, you need to apply NMF to analyse patterns and classify tickets into the following five clusters based on their products/services:

- Credit card / Prepaid card
- Bank account services
- Theft/Dispute reporting
- Mortgages/loans
- Others

With the help of topic modelling, you will be able to map each ticket onto its respective department/category. You can then use this data to train any supervised model such as logistic regression, decision tree or random forest. Using this trained model, you can classify any new customer complaint support ticket into its relevant department.

## Data in depth

The data set given to us is in the .json format and contains 78,313 customer complaints with 22 features. We need to convert this to a dataframe in order to process the given complaints.

## Approach

We need to perform the following eight major tasks to complete the assignment:

- Data loading
- Text preprocessing
- Exploratory data analysis (EDA)
- Feature extraction
- Topic modelling
- Model building using supervised learning
- Model training and evaluation
- Model inference

Note: Once we have finalised the clusters/categories for customer complaints, the next step is to create a data set that contains the complaints and labels (which we found using NMF). This labelled data set will be used for model building using supervised learning.

We need to try at least any three models from logistic regression, naive Bayes, decision tree and random forest, then will select the model that performs the best according to the evaluation metrics.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions

Based on our analysis and as per our Model, below are observationn:

- Logistic Regression model is predicting well on custom data with F1 score : 0.93

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Technologies Used

- Python
- Numpy
- Panda
- pycrf
- sklearn-crfsuite
- spacy
- nlptk
- Jupyter Notebook

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact

Created by [@pravin691983] - feel free to contact me!

<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
