# Titanic Survival Prediction - Data Science Project


---


This project aims to analyze the Titanic dataset to understand which features most influenced passenger survival, and to build and evaluate machine learning models to predict survival outcomes.

## Exploratory Data Analysis (EDA)

We began by performing EDA to uncover trends and relationships in the dataset. Key steps include:

* Checking for missing values and basic statistics
* Correlation analysis between numerical features and survival
* Visualizing survival rates across Sex, Pclass, and Age
* KDE and violin plots to examine age distributions by survival status

## Preprocessing & Feature Engineering

To prepare the data for modeling, we:

* Dropped irrelevant features: PassengerId, Name, Ticket, and Cabin
* Imputed missing values in Age and Embarked
* Encoded categorical variables (Sex and Embarked) using label encoding and one-hot encoding
* Created two new features:

  * FamilySize = SibSp + Parch + 1
  * IsAlone = 1 if the passenger had no family aboard, else 0

## Modeling

We used Logistic Regression as the baseline model with data scaled using StandardScaler. The model was evaluated using:

* Train/Test Split
* Cross-Validation (5-fold) for robustness
* GridSearchCV to tune hyperparameters (C, penalty, solver)

### Evaluation Metrics:

* Accuracy Score
* Classification Report (Precision, Recall, F1-score)

We also compared Logistic Regression with:

* Random Forest Classifier
* Gradient Boosting Classifier

## Feature Importance

We extracted and visualized feature importance from:

* Logistic Regression (based on coefficients)
* Random Forest
* Gradient Boosting

Top influential features:

* Sex
* Fare
* Pclass
* Age

## 📌 Conclusion

Our findings align with historical accounts of the Titanic tragedy:

* **Gender**: Women had a much higher chance of survival
* **Age**: Children, especially under 15, were more likely to survive
* **Socioeconomic Status**:

  * First-class passengers had higher survival rates
  * Higher fare prices indicated better chances of survival


