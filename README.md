# fml-project
Fake News Detection using machine learning
The provided code is a Streamlit application that serves as a fake news detector using a logistic regression model. It allows users to input a news article, and the model predicts whether the input news is "Fake" or "Real." Here's a step-by-step explanation of the code:

Imports: You import necessary libraries, including Streamlit, NumPy, regular expressions, pandas, NLTK for natural language processing, and scikit-learn for machine learning.

Data Loading and Preprocessing:

You load a dataset from a CSV file named 'train.csv.'
The dataset is filled with empty strings for missing values, and a new 'content' column is created by combining the 'author' and 'title' columns.
Features (X) and labels (y) are separated.
Stemming Function: A stemming function is defined to preprocess the text data:

It removes non-alphabetical characters using regular expressions.
Converts the text to lowercase.
Splits the text into words.
Applies stemming to reduce words to their root forms using the Porter Stemmer.
Removes common English stopwords.
Stemming Applied: The stemming function is applied to the 'content' column in the dataset.

Feature Vectorization: The TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer is used to convert text data into numerical features.

Data Splitting: The dataset is split into training and testing sets using train_test_split. The 'stratify' parameter ensures that the class distribution in the training and testing sets is similar.

Logistic Regression Model: A logistic regression model is created and trained on the training data.

Streamlit Web Application:

You create a Streamlit web application with the title 'Fake News Detector.'
A text input widget allows users to enter a news article.
Prediction Function:

The prediction function takes the user's input text, vectorizes it using the TF-IDF vectorizer, and uses the trained logistic regression model to make a prediction.
The function returns the predicted class (1 for "Fake" and 0 for "Real").
Display Prediction: If the user provides input, the app uses the prediction function to make a prediction and displays the result as either "The News is Fake" or "The News Is Real."

This code provides a simple but functional fake news detection application using logistic regression and TF-IDF vectorization. Users can input news articles, and the model classifies them based on the features and labels from the training data. If you have any specific questions or need further clarification, please let me know.
