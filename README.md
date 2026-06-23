# Email-spam-dector
# 📧 Email Spam Detector using Machine Learning

## Overview

The Email Spam Detector is a Machine Learning-based web application that classifies emails or messages as **Spam** or **Not Spam (Ham)**. The project uses Natural Language Processing (NLP) techniques to preprocess text data and a trained Machine Learning model to predict whether an email is spam.

## Features

* Detects spam emails/messages in real time.
* User-friendly web interface built with Streamlit.
* Text preprocessing using NLP techniques.
* Machine Learning model trained on a labeled spam dataset.
* Fast and accurate predictions.

## Technologies Used

* Python
* Streamlit
* Scikit-learn
* Pandas
* NumPy
* NLTK (Natural Language Toolkit)
* Pickle

## Dataset

The model was trained using a spam email dataset obtained from **Kaggle**. The dataset contains labeled messages categorized as:

* Spam
* Ham (Not Spam)

## Machine Learning Workflow

### 1. Data Collection

Spam and non-spam messages were collected from the Kaggle dataset.

### 2. Data Preprocessing

The text data undergoes several preprocessing steps:

* Convert text to lowercase
* Tokenization
* Remove special characters and punctuation
* Remove stopwords
* Apply stemming using Porter Stemmer

### 3. Feature Extraction

Text is converted into numerical vectors using **TF-IDF Vectorization**.

### 4. Model Training

A **Multinomial Naive Bayes** classifier is trained on the processed dataset.

### 5. Model Saving

The trained model and vectorizer are saved as:

* model.pkl
* vectorizer.pkl

### 6. Prediction

When a user enters a message, the application:

1. Preprocesses the text.
2. Converts it into TF-IDF features.
3. Uses the trained model to predict the result.
4. Displays either:

   * Spam
   * Not Spam



## Installation

1. Clone the repository:

```bash
git clone <repository-url>
```

2. Install required packages:

```bash
pip install -r requirements.txt
```

3. Run the application:

```bash
streamlit run app.py
```

## Sample Input

**Input:**
Congratulations! You have won a free iPhone. Click here to claim your prize.

**Output:**
Spam

---

**Input:**
Hello, can we schedule a meeting tomorrow at 10 AM?

**Output:**
Not Spam

## Future Improvements

* Support for multiple languages.
* Deep Learning models (LSTM, BERT).
* Email attachment analysis.
* Enhanced accuracy with larger datasets.

## Conclusion

This project demonstrates the use of Machine Learning and Natural Language Processing for email spam detection. The system preprocesses incoming text, converts it into numerical features using TF-IDF Vectorization, and classifies messages using a trained Multinomial Naive Bayes model. The trained model is stored in `.pkl` files and deployed through a Streamlit web application, enabling users to quickly identify spam and legitimate emails.
