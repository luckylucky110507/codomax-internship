# Day 8 – Build the Model

## Task
Create a Linear Regression model using Scikit-learn and train it with the dataset.

## Concepts Covered
- Importing and using `LinearRegression` from Scikit-learn
- Splitting the dataset into training and testing sets
- Training (fitting) a Linear Regression model on the training data
- Understanding model coefficients (slope) and intercept

## Files in this Folder
- `Build_model.ipynb` – Notebook containing the model creation and training code
- `README.md` – Documentation for this day's task
- `screenshots/` – Proof of code and output
  - `jupyter_model_training_output.png` – Model training code and output

## Output
Model trained successfully!
Coefficient (slope): [0.4306625]
Intercept: 75.67235954861998


## Key Observations
- The model learned a positive relationship between weekly study hours and math score
- For every additional hour of weekly study, the predicted math score increases by approximately 0.43 points
- The intercept (~75.67) represents the predicted score when study hours are 0

## Expected Outcome
Linear Regression model successfully created and trained on the student scores dataset.