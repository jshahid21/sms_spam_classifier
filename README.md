# SMS Spam Collection Classification

This notebook demonstrates a basic text classification task using the SMS Spam Collection dataset. The goal is to build models that can classify SMS messages as either "ham" (not spam) or "spam".

## Steps Performed:

1.  **Data Loading and Exploration:**
    *   Loaded the dataset from the "SMSSpamCollection" file into a pandas DataFrame.
    *   Examined the structure and initial rows of the data.
    *   Checked for missing values.

2.  **Feature Extraction:**
    *   Used **CountVectorizer** to convert the text messages into a matrix of token counts. Stop words were removed, and the vocabulary was limited to the top 1000 features.
    *   Used **TF-IDF Vectorizer** to convert the text messages into a matrix of TF-IDF features, which reflect the importance of words in the context of the entire dataset. Stop words were also removed.

3.  **Model Training:**
    *   Split the data (for both CountVectorizer and TF-IDF features) into training and testing sets (80% training, 20% testing).
    *   Trained a **Logistic Regression** model on the training data for both sets of features.

4.  **Model Evaluation:**
    *   Evaluated the performance of both trained Logistic Regression models on their respective test sets using accuracy as the metric.

## Results:

*   **Logistic Regression with CountVectorizer:** Achieved an accuracy of approximately **0.9865**.
*   **Logistic Regression with TF-IDF:** Achieved an accuracy of approximately **0.9596**.

Based on the accuracy score, the Logistic Regression model trained with CountVectorizer features performed slightly better on this dataset.

## Further Possible Steps:

*   Detailed comparison of model performance (e.g., confusion matrix, precision, recall, F1-score).
*   Experiment with different classification algorithms (e.g., Naive Bayes, SVM).
*   Hyperparameter tuning for the models.
*   Preprocessing techniques like stemming or lemmatization.
*   Exploring n-grams.
