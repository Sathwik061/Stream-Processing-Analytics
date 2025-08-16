# Stream-Processing-Analytics
**Project: SMS Spam Detection with creme**
This project demonstrates how to build an online machine learning model to detect spam messages using the creme library. creme is designed for incremental learning, allowing the model to be trained on data as it arrives, making it suitable for real-time applications and datasets that are too large to fit into memory.

**About creme**
creme is a Python library for online machine learning. Unlike traditional libraries like scikit-learn that require the entire dataset to be loaded at once, creme models are trained one data point at a time. This makes it ideal for handling continuous data streams and resource-constrained environments.

**Dataset**
The model is trained and evaluated on the SMS Spam Collection dataset, which consists of 5,572 text messages labeled as either 'ham' (legitimate) or 'spam'.

**Project Structure**
The core of this project is a Jupyter notebook (creme.ipynb) that contains the following steps:

**Installation**: The necessary libraries, including creme, are installed.

**Data Loading**: The SMSSpamCollection.txt file is loaded into a pandas DataFrame.

**Data Splitting**: The dataset is split into training and testing sets.

**Pipeline Creation**: A machine learning pipeline is constructed using creme.compose.Pipeline. This pipeline automates the sequential steps of feature extraction and classification.

**Feature Extraction**: The feature_extraction.BagOfWords transformer converts the text messages into a bag-of-words representation, where each word is a feature.

**Classification**: The naive_bayes.MultinomialNB classifier is used to predict the class ('ham' or 'spam') of each message.

**Training**: The model is trained incrementally, one message at a time, using a for loop over the training data.

**Evaluation**: The model's performance is measured on both the training and test sets using creme.metrics.Accuracy.

**Results**
The model achieved the following performance:

**Training Accuracy**: 99.31%

**Test Accuracy**: 97.63%

These results demonstrate that a simple, online learning model can achieve high accuracy on a classic text classification problem.

**How to Run the Code**

Clone this repository.

Open the creme.ipynb notebook in a Jupyter environment (e.g., Google Colab, JupyterLab, or VS Code).

Ensure the SMSSpamCollection.txt file is in the correct directory as specified in the notebook.

Run the cells sequentially to reproduce the results.
