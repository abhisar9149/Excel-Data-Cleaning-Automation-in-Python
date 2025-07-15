# 🧹 Excel Data Cleaning Automation in Python

This project automates the process of cleaning and validating an Excel dataset using Python and pandas. It was designed for a real-world sales dataset and performs column-wise validation including ID formats, categorical standardization, numeric conversion, date parsing, and derived column verification.

---

## 📁 Dataset

- **Input File:** `sales.xlsx` (expected to be placed in the `data/` directory)
- **Output File:** `cleaned_sales.xlsx` (or with a timestamp)

---

## 🚀 Features

- ✅ **Drop Duplicates** from the dataset
- 🔍 **Validate IDs** (e.g., must match `TXN_1234567` format)
- 🏷️ **Categorical Text Cleaning** (standardize case, validate against allowed values)
- 🔢 **Numeric Column Validation** (convert invalid entries to `NaN`)
- 📅 **Datetime Parsing** (invalid dates converted to `NaT`)
- 🧮 **Derived Column Check**: Validates if `Total Spent = Quantity × Price Per Unit` and fixes incorrect values
- 🪵 **Column-wise Summary Logs** printed for transparency
- 📝 **Well-documented and modular code** using functions and docstrings

---

## 🧪 Validation Summary Example

```plaintext
--- Validation Report: Total Spent ---
Invalid rows found: 123
Sample invalid values:
   Quantity  Price Per Unit  Total Spent
0         3             5.0           14
1         2             7.0           15
...
