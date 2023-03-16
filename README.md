# Project 3: The Cloud-Splitter - An NLP Project to classify AWS and Azure posts

This project aims to apply web scraping and NLP concepts to classify comments related to AWS and Azure cloud services under General Assembly DSI course. 

# Table of contents
1. [Project description](#1-project-description)
    1.1. [Problem Statement](#11-problem-statement)
    1.2. [Background](#12-background)  
    1.3. [Dataset](#13-dataset) 
    1.4. [Overview](#14-overview)
2. [Results and learnings](#2-results-and-learnings)  
    2.1. [Training and evaluation results](#21-training-and-evaluation-results)    
    2.2. [Insights and Conclusions](#22-insights-and-conclusions)
<br>

## 1.1. Problem Statement ##
[[back to the top]](#table-of-contents)

This case study shows how to create a model for **text classification** to automatically **classify incident tickets for different cloud services**. In this project, we tackle the cold start issue that companies face when they try to create a machine learning model to classfiy incident and support tickets, by making use of publicly available data in subreddits. We use NLP techniques to train model to classify
tickets based on the contents raised by users, operations and development team in the company that uses both AWS and Azure services. This hope to automate the triaging process and reducing the turn-around time to meet the SLA.

## 1.2. Background ##
[[back to the top]](#table-of-contents)

Amazon Web Services and Azure are 2 of the major cloud providers. The other 2 are Oracle and Google Cloud Platforms. Cloud technologies decouples components of computers into different services based on a on-demand or subscription pricing model. This helps to lower the barrier of entry and provides access to computing resources at a fraction of the price for running expensive computations and to experiment POCs.

Cloud services like AWS and Azure are often compared and It is hard for companies to choose which cloud provider to use to leverage on the cloud technologies available. And most companies do utilise services provided by my both cloud services, hence it makes it very hard to differentiate issues or tickets raised.

A rough comparison:
|Cloud Service|AWS|Azure|
|---|---|---|
|Virtual Servers|Instances|VMs|
|Container|???|App Service|
|Docker Management|ECS|Container Service|
|Object Storage|S3 Bucket|Azure Blob|
|Kubernetes|EKS|AKS|
|Files|EFS|Azure Files|
|Content Delivery|CloudFront|CDN
|Data Warehouse|Redshift|SQL Warehouse|
|IoT|AWS IoT|Azure IoT|
|Data Stream|AWS Kinesis|Azure Event Hub|
|Data Lake|AWS S3|Azure Data Lake|
|ETL|AWS Glue|Azure DataBricks|
|ML|AWS SageMaker|Azure ML|
|Serverless|AWS Lambda|Azure Function|
|API|API Gateway|Azure API Management|

<br>

## 1.3. Dataset ##    
[[back to the top]](#table-of-contents)

- For this project, data have scraped from r/aws and r/azure. They are saved in csv format as follows:
* [AWS subreddit posts](./data/aws_subreddit.csv): <br>
* [Azure subreddit posts](./data/azure_subreddit.csv): <br>

- Distribution of values for each column:  

|Feature|Description|Type|
|---|---|---|
||||

## 1.4. Overview ##    
[[back to the top]](#table-of-contents)

1. Scrape
2. Data cleaning - Remove empty rows, select non-empty columns, change data type
3. EDA - Word cloud, Time range plot, Frequency plot, remove stop words, feature engineering, remove special characters, impute values?
4. Pre-processing - Tokenize, remove stop words, stemming/lemmatise, vectorise text
5. Model training, tuning - Logistic Regression, Decision Tree (XGBoost), Random Forest, SVM, Naive Bayes.
6. Model Evaluation and selection
7. Findings and Discussion

<br>

Summary:
- Prepare and Featurise Data
- Tokenise and prime text for tfidf vectoriser.
- Create, train and evaluate classification models using libraries like sklearn, nltk, pandas and numpy.

# 2. Results and learnings
[[back to the top]](#table-of-contents)

## 2.1. Training and evaluation results ##
[[back to the top]](#table-of-contents)

In order to train our models, we used the following:
1. Count Vectoriser
2. TF-IDF Vectoriser

To train models we tested 3 different algorithms: 
1. Naive Bayes
2. Logistic Regression
3. Random Forests

Below you can find results of the model to classify the category:

<br>


