# heart_stroke_prediction
Overview
This project focuses on predicting the likelihood of a stroke occurrence based on various health and demographic features. The dataset used for this project is the "healthcare-dataset-stroke-data.csv," which contains information about patients' age, gender, marital status, work type, residence type, and smoking status.

Project Structure
The project can be divided into several key steps:

Data Importing and Preprocessing: The initial phase involves importing the dataset and performing data preprocessing tasks. This includes handling missing values, encoding categorical variables using LabelEncoder, and scaling numerical features using StandardScaler.

Exploratory Data Analysis (EDA): EDA is performed to gain insights into the dataset. Visualizations, such as count plots and correlation heatmaps, are used to understand the relationships between variables and the distribution of the target variable (stroke).

Training Models: Various machine learning models are trained on the preprocessed data to predict the occurrence of strokes. The following models are used:

Random Forest Classifier
LightGBM Classifier
Linear Support Vector Classifier (LinearSVC)
Logistic Regression
XGBoost Classifier
Decision Tree Classifier
Handling Class Imbalance: To address class imbalance (since stroke cases are relatively rare), the project explores oversampling and undersampling techniques using the SMOTE and RandomUnderSampler from the imbalanced-learn library. The models are retrained on the balanced data.

Pipeline Creation: A machine learning pipeline is created to streamline the process of preprocessing and prediction. The pipeline includes LabelEncoder transformation, scaling, and the Logistic Regression model trained on balanced data.

Evaluation: Model performance is assessed using various metrics, including accuracy, F1-score, and confusion matrices. The pipeline is applied to predict strokes on a separate, unprocessed test dataset.

Results
The project reveals that Logistic Regression on the oversampled+undersampled training data performs well, yielding high accuracy and F1-score. However, it is essential to avoid modifying the test data using oversampling or undersampling, as this can lead to a loss of model generalizability.

Usage
To use the pipeline for stroke prediction on new data:

Import the required libraries.
Load the trained model and the preprocessing functions.
Apply the pipeline to preprocess and predict on new data.
Conclusion
This project demonstrates the process of building a machine learning pipeline for stroke prediction, addressing class imbalance, and achieving promising results. However, careful consideration must be given to handling test data to maintain model robustness and generalizability.
