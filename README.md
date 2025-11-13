# Predictive Analysis of Player Engagement & Retention in Online Gaming
# Project Overview

In this project, I focused on predicting player engagement levels (High, Medium, Low) using behavioral and demographic game metrics.
The main goal of my work is to understand which player behaviors contribute most to engagement and how these patterns can support game design and player retention.

# Research Question

I investigated whether different gameplay and behavioral metrics can accurately predict a player's Engagement Level and which features are the strongest predictors.

# Goal

I aimed to build a reliable classification model that predicts engagement levels and provides insights for improving player retention strategies.
# Dataset

I used the Predict Online Gaming Behavior dataset from Kaggle.

Rows: ~40,034

Columns: 13

Target Variable: Engagement Level (High / Medium / Low)

The dataset includes demographic information, gameplay frequency, playtime, in-game purchases, and more.

What I Did So Far (Methodology & Progress)
 1. Data Inspection & Cleaning

I started by loading the dataset into a Pandas DataFrame.
To understand the structure, I performed:

df.info() to check data types

df.describe() for summary statistics

df.isna().sum() to inspect missing values

What I observed:
There were no missing values in any important column, including the target. This allowed me to proceed without imputation.

# Exploratory Data Analysis (EDA)

Engagement Level Distribution

I plotted the distribution of the target variable to check for class imbalance.

Boxplot Analysis — What I Observed
Age vs. Engagement

I observed that the age distribution looks almost identical across High, Medium, and Low engagement.
→ Age may not be a strong predictor.

PlayTimeHours vs. Engagement

I did a boxplot for this feature and saw that the spread is very similar across the engagement levels.
→ This feature also doesn’t strongly separate classes.

SessionsPerWeek vs. Engagement

Here, I noticed a clear pattern:
Players with High Engagement tend to have higher session frequency.
→ This feature is more useful for prediction than Age or PlayTimeHours.


# Feature Engineering

To improve the model’s performance, I created two new features:

 1. TotalPlayPerWeek

I calculated this as:
TotalPlayPerWeek = PlayTimeHours × SessionsPerWeek

My intention was to capture total weekly gameplay volume.

 2. AgeGroup

I created age bins to simplify the relationship between age and engagement:

Teen (0–17)

YoungAdult (18–25)

Adult (26–40)

MidAge (41–60)

Senior (61–100)

This helps give structure to age-related patterns that linear models might miss.

# Preprocessing

I will encode all categorical variables (Gender, Location, GameDifficulty, GameGenre, AgeGroup, etc.).

I may scale numerical features depending on the models.

#  Model Training

I plan to train multiple classifiers such as:

Logistic Regression

Decision Tree

Random Forest

Gradient Boosting (optional)

# Evaluation

I will evaluate each model using:

Accuracy

Precision, Recall, F1-Score

Confusion Matrix

 Interpretation

I will analyze feature importance to understand:
Which variables contribute most to predicting engagement?


So far, I’ve cleaned the data, explored key patterns, and engineered new features, and I am now ready to advance into preprocessing and modeling.
