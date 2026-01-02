# Predicting Online Gaming Player Engagement Using Machine Learning
 
# Project Overview

This project focuses on predicting player engagement levels (Low, Medium, High) in online gaming environments using supervised machine learning techniques.

I analysed player demographic and behavioural data to understand how gameplay patterns influence engagement and to build predictive models that can support data-driven decision making in the gaming industry.

The project follows a complete end-to-end data science pipeline, including exploratory data analysis, feature engineering, model training, hyperparameter optimisation, model interpretation, and validation using unseen data.

# Research Objective

The main research question addressed in this project is:

“Can player engagement levels in online games be accurately predicted using behavioural and demographic features?”

To answer this, I: Compared multiple machine learning models

Applied systematic hyperparameter tuning

Evaluated performance using multiple metrics

Selected and validated the best-performing model

# Dataset Description

Source: Kaggle – Online Gaming Behavior Dataset

Type: Structured tabular data

Records: ~ 40,000 players

Features include:

Demographics: Age, Gender, Location

Gameplay behaviour: SessionsPerWeek, PlayTimeHours, AvgSessionDurationMinutes

Progression metrics: PlayerLevel, AchievementsUnlocked

Target variable: EngagementLevel (Low / Medium / High)

The dataset is anonymised and suitable for academic research purposes.

# Methodology

The project was implemented in Python using Google Colab, following a modular and well-documented coding approach.

# 1. Exploratory Data Analysis (EDA)

Engagement level distribution

Behavioural comparisons across engagement groups

Correlation analysis

Pairwise feature relationships

# 2. Feature Engineering

Created TotalPlayPerWeek

Derived AgeGroup categories

Improved representation of player behaviour

# 3. Data Pre-processing

One-Hot Encoding for categorical variables

StandardScaler for numerical features

Stratified train-test split (80/20)

# 4. Models Implemented

Logistic Regression

Decision Tree

Random Forest

Gradient Boosting

Support Vector Machine (SVM)

# 5. Hyperparameter Optimisation

Used RandomizedSearchCV

Cross-validation applied

Tuned all models consistently

# Evaluation Metrics

Models were evaluated using:

Accuracy

Precision

Recall

F1-score

Confusion Matrix

This ensured balanced evaluation across all engagement classes.

# Key Results
Model	Tuned Accuracy
Gradient Boosting	~91% (Best)
Random Forest	~89%
Decision Tree	~89%
SVM	~87%
Logistic Regression	~82%

 Gradient Boosting was selected as the final model due to its superior accuracy and balanced class performance.

# Model Interpretation

Feature importance analysis revealed:

SessionsPerWeek

TotalPlayPerWeek

AvgSessionDurationMinutes

These behavioural features were the strongest predictors of player engagement.

# Unseen Data Validation

The final model was tested on manually defined unseen player data.
The model successfully predicted the engagement level, demonstrating good generalisation beyond the training dataset.









