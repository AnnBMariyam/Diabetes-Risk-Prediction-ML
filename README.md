# Diabetes-Risk-Prediction-ML

## Project Overview

This project focuses on predicting the risk of diabetes using machine learning techniques based on patient health indicators.  
The objective is to analyze medical attributes such as glucose level, BMI, age, blood pressure, and insulin levels to build models that can accurately classify whether a patient is diabetic or not.

Multiple machine learning algorithms were implemented and compared to evaluate performance and identify the most effective model for diabetes risk prediction.  
The project follows a complete data science workflow including data preprocessing, exploratory data analysis, model training, evaluation, and comparison of results.

This project demonstrates the application of supervised machine learning techniques in a healthcare analytics context and highlights how data-driven models can support early disease detection.


## Models Implemented
- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest Classifier
- Neural Network (Deep Learning)

## Results Summary

The performance of multiple machine learning models was evaluated using Accuracy, Precision, Recall, F1-Score, and AUC-ROC.

| Model               | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
|--------------------|----------|-----------|--------|----------|---------|
| Neural Network     | 0.9714   | 0.9588    | 0.6950 | 0.8058   | 0.9764  |
| Logistic Regression| 0.9587   | 0.8639    | 0.6130 | 0.7171   | 0.9612  |
| Random Forest      | 0.9708   | 0.9532    | 0.6915 | 0.8015   | 0.9637  |
| SVM                | 0.9614   | 0.9737    | 0.5626 | 0.7132   | 0.9056  |

**Best Performing Model:** Neural Network



### Model Performance Insights

- The Neural Network achieved the highest overall performance, with the best Accuracy, F1-Score, and AUC-ROC.
- Random Forest performed comparably to the Neural Network, indicating strong performance from tree-based models.
- Logistic Regression and SVM showed lower recall, suggesting difficulty in identifying all positive diabetes cases.
- Precision was high across most models, but recall proved to be the most challenging metric.
