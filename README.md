# Nepal Earthquake Analysis and Prediction

## Project Overview

This project analyzes earthquake data from Nepal with two main objectives:

1. **Find the top 10 epicenters with the highest earthquake frequency** to understand spatial patterns of seismic activity.
2. **Predict whether an earthquake will be strong or not** based on features such as location, time, and magnitude.

---

## Dataset Description

The dataset contains **1254 earthquake records** with the following key features:

| Feature       | Description                        |
|---------------|----------------------------------|
| B.S. Date     | Nepali calendar date (string)    |
| A.D. Date     | Gregorian calendar date (datetime)|
| Local Time    | Time of the earthquake (HH:MM)   |
| Latitude      | Geographic latitude of epicenter |
| Longitude     | Geographic longitude of epicenter|
| Magnitude     | Earthquake magnitude (float)     |
| Epicenter     | Location description (string)    |

Additional features were extracted for modeling:

- **Month:** Month of the year extracted from A.D. Date
- **Hour:** Hour of the day extracted from Local Time
- **Strong:** Target variable — 1 if Magnitude ≥ 5.0, else 0

---

## Methodology

1. **Data Preprocessing:**
   - Convert latitude, longitude, and dates to proper numeric and datetime types.
   - Extract month and hour features.
   - Define the binary target based on magnitude threshold (≥ 5.0).
   - Handle missing values and split data into train and test sets.
   - Scale features for models sensitive to feature scale.

2. **Model Training and Evaluation:**
   - Train multiple classification algorithms:
     - Logistic Regression
     - Decision Tree
     - Random Forest
     - Gradient Boosting (e.g., XGBoost alternative)
     - Support Vector Machine
     - K-Nearest Neighbors
     - Naive Bayes
     - Linear Discriminant Analysis
     - Quadratic Discriminant Analysis
   - Evaluate models using ROC AUC on test data.
   - Rank models by ROC AUC score.

---

## Results

The ROC AUC scores allow comparison of each model’s ability to distinguish between strong and weak earthquakes. The best-performing model can be used for practical earthquake strength prediction.

---

## Future Work

- Hyperparameter tuning to improve model performance.
- Cross-validation for robust evaluation.
- Incorporate additional geological or seismic features if available.
- Deploy model for real-time earthquake risk assessment.

---

## How to Use This Notebook

- Run preprocessing cells to prepare data.
- Execute training and evaluation cells to fit models and view results.
- Modify threshold or add new features to improve predictions.
- Visualize relationships between variables and magnitude.

---

## Contact

For questions or suggestions, please reach out!

---

*This notebook is designed for earthquake data analysis enthusiasts and disaster risk management practitioners seeking to leverage machine learning for seismic event classification.*

