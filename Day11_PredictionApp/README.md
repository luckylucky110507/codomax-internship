# Day 11 – Prediction App

**Codomax AI/ML Internship — Daily Task Series**

## 📌 Objective
Build a simple Python program that takes study hours as input from the user and returns a predicted score, using the Linear Regression model trained on the student performance dataset.

## ✅ Expected Outcome
Working prediction program.

## 📂 Dataset
`student_scores_cleaned.csv` — cleaned student performance dataset (from Day 5), containing subject-wise scores (`math_score`, `history_score`, `physics_score`, `chemistry_score`, `biology_score`, `english_score`, `geography_score`) and `weekly_self_study_hours`.

An `average_score` column was engineered by averaging all seven subject scores, since the dataset does not have a single overall "Score" column.

## 🛠️ Approach
1. Load the cleaned dataset and inspect columns.
2. Create the `average_score` feature (mean of all subject scores).
3. Define `weekly_self_study_hours` as the independent variable (`X`) and `average_score` as the target (`y`).
4. Train a Linear Regression model on the full dataset.
5. Take study hours as user input and predict the score.
6. Re-train on an 80/20 train-test split to evaluate model performance (MAE, MSE, R²).

## 💻 Code Summary

```python
import pandas as pd
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score

# Load dataset
df = pd.read_csv("student_scores_cleaned.csv")

# Engineer target column: average of all subject scores
score_columns = ['math_score', 'history_score', 'physics_score',
                  'chemistry_score', 'biology_score', 'english_score', 'geography_score']
df['average_score'] = df[score_columns].mean(axis=1)

# Features and target
X = df[['weekly_self_study_hours']]
y = df['average_score']

# Train the model
model = LinearRegression()
model.fit(X, y)

# Prediction app — takes user input and predicts the score
hours = float(input("Enter weekly study hours: "))
predicted_score = model.predict(pd.DataFrame([[hours]], columns=['weekly_self_study_hours']))
print(f"Predicted Average Score: {predicted_score[0]:.2f}")

# Evaluate model performance on a train/test split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)

print("MAE:", mean_absolute_error(y_test, y_pred))
print("MSE:", mean_squared_error(y_test, y_pred))
print("R² Score:", r2_score(y_test, y_pred))
```

## 📊 Sample Output

```
Enter weekly study hours: 4
Predicted Average Score: 77.54

MAE: 4.54
MSE: 31.71
R² Score: 0.26
```

## 📷 Screenshot
- `Day11_PredictionApp_output.png` — Notebook run showing the user input and predicted score, along with model evaluation metrics.

## ▶️ How to Run
1. Open `Day11_PredictionApp.ipynb` in Jupyter Notebook.
2. Run all cells: **Kernel → Restart Kernel and Run All Cells**.
3. When prompted, enter a value for weekly study hours (e.g. `4`) and press Enter.
4. The predicted average score is printed below the cell, followed by evaluation metrics.

## 👩‍💻 Author
**Lucky Kumari** — B.Tech CSE, IIMT University
AI/ML Intern, Codomax Digital Solutions
