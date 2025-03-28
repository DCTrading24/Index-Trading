# Index-Trading

Overview

This project explores the prediction of daily price movements for the S&P 500 index using machine learning models. It focuses on feature engineering, logistic regression, resampling techniques, and decision tree-based classifiers to determine whether the market will move up or down on a given day.

Contents

Target and Data Basis
Cleaning and Feature Engineering
Logistic Regression and Sampling Manipulation
Random Forest Classifier
Summary

Target and Data Basis
Goal: 
Predict if the S&P 500 price will increase or decrease the next trading day (open-to-close movement).
Data:
S&P 500 E-mini Futures (April 2012 – March 2025).
Daily timeframe with 10 technical indicators (trend, oscillators, internal indicators, and volume).
Categorical Prediction Choice:
Technical indicators are optimized for direction, not valuation.
A short-term, one-day prediction introduces significant noise.
Regression models showed poor predictive performance.

Cleaning and Feature Engineering
Adjusted features to strengthen correlation with price movement.
Feature selection through dropping, merging, and creating new indicators.

Logistic Regression and Sampling Manipulation
Initial model always predicted an intraday uptrend.
Various train-test splits, solvers, feature tuning, and scaling didn’t improve performance.
Resampling strategies:
SMOTE oversampling: Improved balance but introduced excessive errors.
TomekLinks undersampling: Improved downtrend prediction but introduced a negative bias.
Voting Classifier: Combined uptrend-biased and downtrend-biased models but did not significantly improve accuracy.

Random Forest Classifier
Applied after resampling, achieving:
Precision of ~98%
R² of 0.66

Summary
Technical indicators showed only slight correlation improvements with price movement.
Resampling had a significant impact on model performance.
The Voting Classifier approach can be useful for balancing predictions.
Logistic regression struggled with this prediction task, while decision tree models proved more effective.
Disclaimer: This analysis is not financial advice. Trading requires a robust strategy beyond model-based predictions.

Author
David Thrien – March 28, 2025
