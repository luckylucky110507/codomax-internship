# Day 9 – Prediction Task

## Task
Use the trained Linear Regression model to predict a student's average score based on their weekly self-study hours.

## Dataset
`student_scores_cleaned.csv`
- Feature (X): `weekly_self_study_hours`
- Target (y): `average_score` (mean of math, history, physics, chemistry, biology, english, and geography scores)

## Steps Performed
1. Loaded the cleaned dataset using pandas.
2. Calculated the average of all 7 subject scores to create the `average_score` column.
3. Set `weekly_self_study_hours` as the independent variable (X) and `average_score` as the dependent variable (y).
4. Split the data into training and test sets (80% train, 20% test, `random_state=42`).
5. Fit a `LinearRegression()` model on the training data.
6. Generated predictions on the test data (`model.predict(X_test)`) and compared predicted vs actual scores.
7. Made a custom prediction — for a student studying **20 hours/week**, the predicted average score:

   **Predicted Score ≈ 81.41**

## Sample Output
```
Predicted Scores (first 5): [81.17, 76.80, 80.44, 77.77, 77.04]
Actual Scores (first 5):    [90.43, 79.86, 76.71, 74.57, 76.86]

Predicted average score for 20 study hours/week: 81.41
```

## Expected Outcome
Predictions successfully generated using the trained Linear Regression model.

## Files in this Folder
- `predict_scores.ipynb` – Notebook covering model training and prediction
- `README.md` – Documentation for this day's task
- `screenshots/` – Proof of code and output
  - `jupyter_prediction_output.png` – Prediction code and output

## Tools Used
- Python
- Pandas
- Scikit-learn (LinearRegression, train_test_split)

##Author
Lucky Kumari
AI&ML Intern(Codomax Digital Solutions)