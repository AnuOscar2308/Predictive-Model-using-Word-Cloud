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

### 2) Feature Engineering
Converted text into numerical vectors using:
TF-IDF Vectorizer
- max_features = 10,000
- min_df = 6

### 3) Models Trained

Multiple classification algorithms were trained and evaluated:
- Multinomial Naive Bayes
- Decision Tree
- Gaussian Naive Bayes
- Logistic Regression

Evaluation Metrics:
- Accuracy
- F1 Score
- Confusion Matrix

### _Stage 2 — Ensemble Learning (ensemble model.ipynb)_

To improve performance, multiple models were combined into a hybrid system.

### Ensemble Voting Classifier

Models used inside ensemble:
- Logistic Regression
- Decision Tree
- Support Vector Machine
- K-Nearest Neighbors

``` ensemble = VotingClassifier(estimators) ```
The ensemble aggregates predictions from all models and outputs the final category.

### Skills:
- **Natural Language Processing:** Text preprocessing, Lemmatization, Tokenization, Stopword filtering
- **Machine Learning:** Classification modelling, Model evaluation, Ensemble learning, Voting classifier
- **Feature Engineering:** TF-IDF Vectorization
- **Python Libraries:** Scikit-learn, NLTK, Pandas, Seaborn, Matplotlib
- **Data Science Concepts:** Model comparison, Bias-variance improvement, Confusion matrix interpretation

### Results
- Baseline models successfully classified news categories
- Performance improved significantly after ensemble learning
- The ensemble classifier provided more stable and reliable predictions compared to individual models

### Business Recommendation
Content platforms should deploy ensemble-based classifiers instead of single models because:
- Higher accuracy
- More robust predictions
- Reduced misclassification
- Better recommendation quality

This system can be integrated into content pipelines to automatically organize articles in real time.
