## Title:

News Article Classification using NLP and Ensemble Machine Learning

## Executive Summary:

This project builds an end-to-end Natural Language Processing (NLP) pipeline to automatically classify news articles into multiple categories (World, Sports, Business, Science). The system processes raw textual data, converts it into numerical features using TF-IDF vectorization, and trains several machine learning classifiers to predict article categories.

The project is implemented in two stages. The first stage develops baseline classification models and evaluates their performance. The second stage improves prediction accuracy by combining multiple models using an ensemble voting classifier. The final system demonstrates how ensemble learning can significantly enhance text classification performance compared to individual models.

## Business Problem:

Large news platforms and content aggregators receive thousands of articles daily. Manual categorization creates several issues:
- Time-consuming editorial work
- Inconsistent tagging
- Delayed publishing pipelines
- Poor recommendation accuracy

Organizations require an automated solution to:

- Categorize incoming articles instantly
- Improve search and recommendation systems
- Reduce manual moderation effort
- Enable real-time content organization

This project builds an intelligent text classification system capable of automatically assigning category labels to incoming news articles.

## Methodology:
### _Stage 1 — Baseline NLP Classification (main.ipynb)_
### 1) Data Preprocessing
Performed a complete text cleaning pipeline:
- Tokenization
- Lowercasing
- Punctuation removal
- Number removal
- Stopword removal
- Lemmatization
