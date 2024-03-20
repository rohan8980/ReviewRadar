## ReviewRadar

This repository contains code for building a sentiment analysis model for classifying customer reviews as positive or negative. The model is trained on a dataset of Amazon product reviews for clothing, shoes, and jewelry.

### Data

The data used in this project is of the Clothing, Shoes and Jewelry Reviews from the Amazon Review Data dataset available [here](https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/). The dataset includes product reviews and metadata.

### Overview

The project follows below approach:

1. **Data Cleaning:** 
    * The `Data Cleaning` notebook cleans the raw data.
    * Ratings 1, 2, and 3 are considered negative, and 4 and 5 are considered positive.
    * The cleaned data is saved in the csv file.

2. **Data Preprocessing:**
    * The `Data Preprocessing` notebook performs text preprocessing on the cleaned data.
    * Preprocessing steps include:
        * Lowercasing text
        * Removing HTML tags
        * Expanding contractions
        * Removing digits
        * Removing accented characters
        * Removing special characters and emoticons
        * Removing extra whitespaces
    * The notebook also uses SpaCy and also has NLTK functions for:
        * Tokenization
        * Stopword removal
        * Stemming, and 
        * Lemmatization
    * The preprocessed data is saved in the csv file.

3. **Data Modeling:**
    * The `DataModelling` notebook trains a sentiment analysis model using TF-IDF vectorization and an SVM classifier.
    * The model achieves an accuracy of 88% on the test dataset.
    * Word clouds are generated for positive and negative reviews for both actual and predicted classes.
    