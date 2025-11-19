Predictive Analysis of Player Engagement and Retention

🌟 Project Overview

I performed a predictive analysis to understand and predict player engagement in online gaming. I focused on determining whether player behavioral metrics such as playtime, session frequency, and demographic information could accurately predict engagement level (High, Medium, Low).

The goal of this project is to develop classification models that can help inform strategies for improving player retention and optimizing game design.

Research Question:
I explored: Can various player behavioral metrics accurately predict player engagement level, and what are the strongest predictors?

Dataset:
I used the Predict Online Gaming Behavior Dataset from Kaggle: Link to Dataset

Number of rows: 40,034

Number of columns: 13

Target variable: EngagementLevel (Categorical: Low, Medium, High)

 Step 1 — Data Loading and Inspection

I loaded the dataset into a Pandas DataFrame and performed basic inspection:

I used df.info() and df.describe() to check the structure and summary statistics.

I observed that the dataset had no missing values in key columns.

I checked the target distribution and observed Low engagement players were the most common, followed by Medium and High engagement players.

 Step 2 — Exploratory Data Analysis (EDA)

I explored the relationship between player features and engagement:

Age vs Engagement: I observed that age distribution was fairly similar across engagement levels.

PlayTimeHours vs Engagement: I observed that total playtime was slightly higher for Medium and High engagement players.

SessionsPerWeek vs Engagement: I observed that High engagement players tend to have more sessions per week than Medium or Low players.

I visualized these patterns using boxplots and histograms to better understand the distributions.

🛠 Step 3 — Feature Engineering

I created new features to improve model prediction accuracy:

TotalPlayPerWeek — calculated as PlayTimeHours * SessionsPerWeek.
I observed that this feature captured the total weekly engagement more effectively.

AgeGroup — I binned age into categories: Teen, YoungAdult, Adult, MidAge, Senior.
I observed that this categorical feature could help models better capture age-related patterns.

I visualized these features:

Histogram of TotalPlayPerWeek

Boxplot of TotalPlayPerWeek vs EngagementLevel

Count of players in each AgeGroup

 Step 4 — Preprocessing

I performed preprocessing to prepare data for modeling:

I encoded categorical variables: Gender, Location, GameDifficulty, GameGenre, AgeGroup.

I scaled numerical features: Age, PlayTimeHours, SessionsPerWeek, TotalPlayPerWeek.

I split the dataset into train and test sets using an 80/20 split.

 Step 5 — Model Training and Hyperparameter Tuning

I trained multiple classification models:

Logistic Regression — I tuned C, penalty, and solver using RandomizedSearchCV.
I observed that adjusting regularization improved model performance slightly.

Decision Tree — I trained a default decision tree and observed moderate performance.

Random Forest — I tuned n_estimators, max_depth, and min_samples_split.
I observed that this model achieved higher accuracy than a single decision tree.

Gradient Boosting — I tuned learning_rate, n_estimators, and max_depth.
I observed this model performed the best among all tree-based models.

SVM — I tuned C, kernel, and gamma.
I observed that SVM performed well but slightly lower than Gradient Boosting and Random Forest.

 Step 6 — Model Evaluation and Comparison

I compared all models based on test accuracy:

Model	Test Accuracy
Gradient Boosting	0.905832
Random Forest	0.897340
SVM	0.877108
Decision Tree	0.835394
Logistic Regression	0.820907

I observed that Gradient Boosting achieved the highest accuracy.

IN my next steps for next supervission sessions 
I plan to analyze feature importance from tree-based models to identify the strongest predictors of engagement.

I may experiment with additional hyperparameter tuning and ensemble methods to further improve model performance.

I will also explore cross-validation results to ensure model stability.
