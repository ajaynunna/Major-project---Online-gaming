# Player Engagement Level Prediction using Machine Learning

This project focuses on predicting player engagement levels (High, Medium, Low) in online gaming using supervised machine learning models. The goal is to understand which gameplay and demographic factors influence player engagement, and to build a model that can accurately classify user behavior.


# Project Overview

I used a  Kaggle-style dataset containing 40,034 players with features such as:

Age, Gender, Location

GameGenre, GameDifficulty

PlayTimeHours

SessionsPerWeek

AvgSessionDuration

PlayerLevel, Achievements

TotalPlayPerWeek (engineered feature)

AgeGroup (engineered feature)

I built five machine learning models, evaluated them, and optimized the best-performing ones using RandomizedSearchCV.

The final selected model is Gradient Boosting, achieving 91% accuracy.

#  Exploratory Data Analysis (EDA)

I analyzed distributions and relationships using:

Engagement level distribution plot

Boxplots: Age vs Engagement, PlayTime vs Engagement

SessionsPerWeek distribution

Correlation heatmap

Pair plots

 Key Insights:

Engagement levels were well balanced

SessionsPerWeek was the strongest predictor

Age had little effect

Low correlation across features → models perform well

# Data Preprocessing
 Separated numerical and categorical features
 Applied One-Hot Encoding → 27 final features
 Used StandardScaler for numerical scaling
 Performed train–test split (80/20)
 Ensured balanced target distribution in train & test sets

#  Model Building

I trained the following base models:

Logistic Regression

Decision Tree

Random Forest

Support Vector Machine (SVM)

Gradient Boosting

 Best Base Model: Gradient Boosting (90.5% accuracy)

#  Hyperparameter Tuning

Using RandomizedSearchCV, I optimized all five models.

 Final Best Model: Gradient Boosting

 Accuracy: 91.02%

Best Parameters:
{n_estimators=150, max_depth=5, learning_rate=0.05, min_samples_split=2}

# 5️ Feature Importance Analysis

Using the tuned Gradient Boosting model, I extracted the top 15 most important features.

 Top Predictors of Engagement:

AvgSessionDurationMinutes

SessionsPerWeek

AchievementsUnlocked

PlayerLevel

TotalPlayPerWeek

These features strongly influence whether a player becomes highly engaged.

 # Final Interpretation

Engagement is primarily driven by player activity frequency, not demographics.

Tree-based methods (GB, RF) significantly outperform linear models.

Hyperparameter tuning increased performance by 2–5%, especially for Decision Tree and Gradient Boosting.

The model can help game developers identify potential high-engagement or low-engagement players for retention strategies.

 # Results Summary
Model	Base Accuracy	Tuned Accuracy
Gradient Boosting	0.905	0.910
Random Forest	0.893	0.894
Decision Tree	0.828	0.878
SVM	0.879	0.853
Logistic Regression	0.821	0.824

# Best model: Gradient Boosting

 # Conclusion

This project demonstrates that player engagement can be accurately predicted using machine learning, with Gradient Boosting proving to be the most effective. The insights can support player retention, game design optimization, and personalized engagement strategies in the gaming industry.
