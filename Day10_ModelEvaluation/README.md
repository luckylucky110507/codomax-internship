# Day 10 – Model Evaluation Task

## Task
Evaluate the trained Linear Regression model's performance using MAE, MSE, and R² Score.

## Dataset
`student_scores_cleaned.csv`
- Feature (X): `weekly_self_study_hours`
- Target (y): `average_score`

## Steps Performed
1. Used the same trained Linear Regression model and test set (`X_test`, `y_test`) from Day 9.
2. Imported evaluation metrics from `sklearn.metrics`: `mean_absolute_error`, `mean_squared_error`, `r2_score`.
3. Calculated:
   - **MAE (Mean Absolute Error)** — average absolute difference between predicted and actual scores.
   - **MSE (Mean Squared Error)** — average squared difference between predicted and actual scores.
   - **R² Score** — how well the model explains the variance in the data (closer to 1 = better fit).

## Code
```python
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score

mae = mean_absolute_error(y_test, y_pred)
mse = mean_squared_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)

print(f"Mean Absolute Error (MAE): {mae:.2f}")
print(f"Mean Squared Error (MSE): {mse:.2f}")
print(f"R² Score: {r2:.2f}")
```

## Output
```
Mean Absolute Error (MAE): 4.54
Mean Squared Error (MSE): 31.71
R² Score: 0.26
```

## Expected Outcome
Model performance measured using MAE, MSE, and R² Score.

## Files in this Folder
- `ModelEvaluation.ipynb` – Notebook covering model evaluation (MAE, MSE, R²)
- `README.md` – Documentation for this day's task
- `screenshots/` – Proof of code and output
  - `jupyter_model_evaluation_output.png` – Evaluation metrics code and output (MAE, MSE, R²)
## Tools Used
- Python
- Pandas
- Scikit-learn (mean_absolute_error, mean_squared_error, r2_score)