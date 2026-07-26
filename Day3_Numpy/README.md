# Day 3 – NumPy Fundamentals

**Codomax AI/ML Internship — Daily Task Series**

## 📌 Objective
Learn the fundamentals of NumPy: creating arrays, indexing & slicing, and performing mathematical operations on array-based data.

## ✅ Expected Outcome
NumPy fundamentals completed.

## 🛠️ Topics Covered
- Installing and importing NumPy
- Creating 1D and 2D arrays
- Special arrays: `zeros()`, `ones()`, `arange()`
- Indexing and slicing (1D & 2D arrays)
- Mathematical operations: addition, subtraction, multiplication, division
- Aggregate functions: `sum()`, `mean()`, `max()`, `min()`, `sqrt()`
- Mini practice task: calculating average, highest, and lowest student marks

## 💻 Code Summary

```python
import numpy as np

# 1D and 2D arrays
arr1 = np.array([10, 20, 30, 40, 50])
arr2 = np.array([[1, 2, 3], [4, 5, 6]])

# Special arrays
zeros = np.zeros((2, 3))
ones = np.ones((3, 3))
range_arr = np.arange(1, 11)

# Indexing & Slicing
print(arr1[0])        # first element
print(arr1[-1])       # last element
print(arr1[1:4])      # slicing
print(arr2[0, 1])     # 2D indexing (row, col)
print(arr2[:, 1])     # entire column

# Mathematical operations
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
print(a + b, a - b, a * b, a / b)
print(np.sum(a), np.mean(a), np.max(a), np.min(a), np.sqrt(a))

# Practice: student marks
marks = np.array([85, 90, 78, 92, 60])
print("Average marks:", np.mean(marks))
print("Highest marks:", np.max(marks))
print("Lowest marks:", np.min(marks))
```

## 📊 Sample Output

```
Average marks: 81.0
Highest marks: 92
Lowest marks: 60
```

## 📷 Screenshots
Notebook execution screenshots are included in this submission:
- `Day3_NumPy_Array.png` — Arrays (1D, 2D, zeros, ones, arange)
- `Day3_NumPy_Indexing_MathOps.png` — Indexing/Slicing + Mathematical operations
- `Day3_NumPy_Marks_Output.png` — Math operations output + student marks calculation

## ▶️ How to Run
1. Open `Day3_NumPy.ipynb` in Jupyter Notebook.
2. Run all cells: **Kernel → Restart Kernel and Run All Cells**.
3. Outputs will display below each code cell as shown in the screenshots.

## 👩‍💻 Author
**Lucky Kumari** — B.Tech CSE, IIMT University
AI/ML Intern, Codomax Digital Solutions
