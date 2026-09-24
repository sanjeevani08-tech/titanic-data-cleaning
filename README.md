# Titanic Dataset - Data Cleaning & Preprocessing

This repository contains the data cleaning pipeline and processed output for the public Titanic dataset.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sanjeevani08-tech/titanic-data-cleaning/blob/main/titanic_cleaning.ipynb)

## Project Structure
* `raw_titanic.csv` — Original raw dataset downloaded from source.
* `cleaned_titanic.csv` — Processed output ready for analysis/modeling.
* `titanic_cleaning.ipynb` — Executable Jupyter Notebook containing Python cleaning code.
* `README.md` — Project documentation.

## Summary of Data Cleaning Operations

| Issue Type | Feature / Column | Action Taken |
| :--- | :--- | :--- |
| **Missing Values** | `Age` | Imputed missing values using the median age grouped by `Pclass` and `Sex`. |
| | `Cabin` | Dropped column due to >75% missing entries. |
| | `Embarked` | Imputed missing values with mode (`'S'`). |
| **Duplicates** | All columns | Verified and dropped duplicate passenger rows. |
| **Data Types** | `PassengerId` | Cast to string identifier. |
| | `Pclass`, `Sex` | Cast to Pandas `category` type for efficiency. |
| **Formatting** | `Sex`, `Embarked` | Stripped whitespace and standardized text case. |
