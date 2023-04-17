# Identifying Entities in Healthcare Data

> BeHealthy require predictive model which can identify disease and treatment from the patients interaction with doctor or ordering medicines online.
> By observing the requirement, it is clearly visible that we have to process the textual sentence and identify the entities like Disease and Treatment. We can predict these all requirements using

- CRF (Conditional Random Field) classifier
- HMM (Hidden Markov Model).

## Table of Contents

- [Overview Business Understanding](#overview-business-understanding)
- [Problem Statement Business Objectives](#problem-statement-business-objectives)
- [Data in depth](#data-in-depth)
- [Approach](#approach)
- [Technologies Used](#technologies-used)
- [Conclusions](#conclusions)

<!-- You can include any other section that is pertinent to your problem -->

## Overview Business Understanding

Now, let’s consider a hypothetical example of a health tech company called ‘BeHealthy’. Suppose ‘BeHealthy’ aims to connect the medical communities with millions of patients across the country.

‘BeHealthy’ has a web platform that allows doctors to list their services and manage patient interactions and provides services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organise appointments, track past medical records and provide e-prescriptions.

So, companies like ‘BeHealthy’ are providing medical services, prescriptions and online consultations and generating huge data day by day.

Let’s take a look at the following snippet of medical data that may be generated when a doctor is writing notes to his/her patient or as a review of a therapy that he or she has done.

“The patient was a 62-year-old man with squamous cell lung cancer, which was first successfully treated by a combination of radiation therapy and chemotherapy.”

As you can see in this text, a person with a non-medical background cannot understand the various medical terms. We have taken a simple sentence from a medical data set to understand the problem and where you can understand the terms ‘cancer’ and ‘chemotherapy’.

Suppose you have been given such a data set in which a lot of text is written related to the medical domain. As you can see in the dataset, there are a lot of diseases that can be mentioned in the entire dataset and their related treatments are also mentioned implicitly in the text, which you saw in the aforementioned example that the disease mentioned is cancer and its treatment can be identified as chemotherapy using the sentence.

But, note that it is not explicitly mentioned in the dataset about the diseases and their treatment, but somehow, you can build an algorithm to map the diseases and their respective treatment.

Suppose you have been asked to determine the disease name and its probable treatment from the dataset and list it out in the form of a table or a dictionary like this.

<p>
<img src ="https://images.upgrad.com/0891d77b-b9ca-4e9d-8934-d9a9b078a51c-syntactic%20sol%20pic1.png" alt='Figure 1'>
<center> <b>Figure 1.</b> </center> 
 </br>  
</p>

## Problem Statement Business Objectives

BeHealthy require predictive model which can identify disease and treatment from the patients interaction with doctor or ordering medicines online.
By observing the requirement, it is clearly visible that we have to process the textual sentence and identify the entities like Disease and Treatment. We can predict these all requirements using

- CRF (Conditional Random Field) classifier
- HMM (Hidden Markov Model)

### Want to

- Identifying Entities in Healthcare Data using CRF (Conditional Random Field) classifier

## Data in depth

It contains four data file for this activity to proceed, they are

- Train Sentence Dataset
- Train Label Dataset
- Test Sentence Dataset
- Test Label Dataset

  Sentence file contains all interations between patients and doctor and Label file contains all enitiy tags for particular words arranged as per sentence. We need to do few preprocessing while accessing dataset we will explore that in further steps.
  We have the train and the test datasets; the train dataset is used to train the CRF model, and the test dataset is used to evaluate the built model.

## Approach

#### Understanding the Dataset

- To gain insights from data we must look into each aspect of it very carefully. We will start with observing few rows and columns of data both from the starting and from the end.

#### Preprocessing

- We need to process and modify the data into sentence format. This step has to be done for the 'train_sent' and ‘train_label’ datasets and for test datasets as well.
- After that, we need to define the features to build the CRF model.
- Then, you need to apply these features in each sentence of the train and the test dataset to get the feature values.
- Once the features are computed, you need to define the target variable and then build the CRF model.
- Then, we need to perform the evaluation using a test data set.
- After that, we need to create a dictionary in which diseases are keys and treatments are values

#### Build Model after Dataset split

- Build model & validate results after split dataset in train & test repsectiviey using CRF (Conditional Random Field) classifier

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions

Based on our analysis and as per our Model, below are observationn:

- Predicted F1-score for Medical Entity Dataset is: **92.5 %**

Also the predicted the treatment for the disease name: 'hereditary retinoblastoma' is:

- Identified Disease: **retinoblastoma**.
- Identified Treatment: **radiotherapy**.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Technologies Used

- Python
- Numpy
- Panda
- pycrf
- sklearn-crfsuite
- spacy
- Jupyter Notebook

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact

Created by [@pravin691983] - feel free to contact me!

<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
