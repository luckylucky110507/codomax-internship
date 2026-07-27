# Day 5 – Data Cleaning

## Task
Handle missing values, remove duplicate rows, and understand dataset statistics to prepare a clean dataset for further analysis.

## Concepts Covered
- Checking for missing values using `isnull().sum()`
- Filling missing numeric values using `fillna()` with column mean
- Detecting and removing duplicate rows using `duplicated()` and `drop_duplicates()`
- Understanding dataset statistics using `describe()`
- Reviewing dataset structure and data types using `info()`
- Saving the cleaned dataset to a new CSV file using `to_csv()`

## Dataset
Student scores dataset (sourced from Kaggle) containing student details such as scores, study hours, absence days, and other attributes — 2000 rows and 17 columns.

## Files in this Folder
-Day5_DataCleaning/
├── Data_cleaning.ipynb
├── student_scores_cleaned.csv
├── README.md
└── screenshots/
    ├── jupyter_data_cleaning_missing_values.png
    ├── jupyter_data_cleaning_describe.png
    └── jupyter_data_cleaning_info_save.png
## Key Findings
- No missing values were found in the dataset
- No duplicate rows were found in the dataset
- Dataset contains a mix of numeric, text, and boolean columns across 17 total fields

## Expected Outcome
Clean dataset prepared and saved, ready for visualization and modeling in the upcoming days.