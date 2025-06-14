﻿
# 📰 Fake News Detection based on News Title

This repository provides a pipeline for fake news detection using classical machine learning and deep learning models. It covers data exploration, feature engineering, multiple text vectorization strategies, model training, hyperparameter tuning, and evaluation.

## Features

* **Exploratory Data Analysis (EDA):**

  * Visualizations of fake/real news distribution
  * Feature engineering (e.g., all-caps word counts, month extraction)
  * Word clouds for fake and real news

* **Text Preprocessing:**

  * Custom tokenization, stopword removal, stemming
  * Handling of abbreviations and normalization

* **Vectorization Methods:**

  * Bag of Words (BoW)
  * TF-IDF
  * FastText embeddings
  * BERT embeddings

* **Model Training & Evaluation:**

  * Logistic Regression
  * Random Forest
  * XGBoost (with RandomizedSearchCV hyperparameter tuning)
  * Deep Neural Network (TensorFlow/Keras)
  * Metrics: accuracy, F1-score, confusion matrix 📊

## 📓 Notebooks

* **EDA\_and\_embedings.ipynb:**
  Data exploration, feature engineering, and embedding generation.

* **models.ipynb:**
  Model training, hyperparameter tuning, evaluation, and comparison across different vectorization techniques.

## ⚙️ Usage

1. **Install requirements:**
   Install dependencies from `requirements.txt` (e.g., `scikit-learn`, `xgboost`, `tensorflow`, etc.).

2. **Run EDA and feature engineering:**
   Open and run `EDA_and_embedings.ipynb`.

3. **Train and evaluate models:**
   Open and run `models.ipynb`.

4. **Model Saving:**
   Trained models are saved in the `models/` directory.


## 📊 Performance Summary

| Vector Type        | Model                  | Train Acc. | Train F1 | Test Acc. | Test F1 |
| ------------------ | ---------------------- | ---------- | -------- | --------- | ------- |
| BoW                | LogisticRegression     | 0.9723     | 0.9723   | 0.9440    | 0.9441  |
| BoW                | RandomForestClassifier | 0.8679     | 0.8677   | 0.8502    | 0.8498  |
| BoW                | XGBClassifier          | 0.9172     | 0.9172   | 0.9009    | 0.9008  |
| TF-IDF             | LogisticRegression     | 0.9459     | 0.9459   | 0.9322    | 0.9322  |
| TF-IDF             | RandomForestClassifier | 0.8719     | 0.8719   | 0.8539    | 0.8539  |
| TF-IDF             | XGBClassifier          | 0.9235     | 0.9236   | 0.8976    | 0.8976  |
| FastText           | LogisticRegression     | 0.8532     | 0.8532   | 0.8452    | 0.8452  |
| FastText           | RandomForestClassifier | 0.9282     | 0.9281   | 0.8449    | 0.8446  |
| FastText           | XGBClassifier          | 0.9923     | 0.9923   | 0.8874    | 0.8874  |
| BERT               | LogisticRegression     | 0.9760     | 0.9760   | 0.9683    | 0.9683  |
| BERT               | RandomForestClassifier | 0.9790     | 0.9790   | 0.9329    | 0.9329  |
| BERT               | XGBClassifier          | 1.0000     | 1.0000   | 0.9662    | 0.9662  |
| BERT (with tuning) | XGBClassifier          | 0.9997     | 0.9997   | 0.9645    | 0.9645  |
| BoW                | FNN                    | 0.9750     |          | 0.94      | 0.94    |

