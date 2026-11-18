# Practical Work No. 2 - Pandas: Working with Tables

This repository contains my solution for Practical Work No. 2. The goal of the work is to master the core Pandas structures - **DataFrame** and **Series** - and to learn how to import data from files, inspect it, and perform indexing, filtering and sorting of tabular data.

## Repository contents

| File | Description |
|------|-------------|
| `karpiuk_practice2.ipynb` | Practical part (Steps 1-8): creating a DataFrame from a dictionary, reading a CSV file from Google Drive, inspecting data (`info()`, `describe()`), indexing with `loc` / `iloc`, filtering with boolean masks, sorting, and saving the result to CSV. |
| `karpiuk_tasks2.ipynb` | Individual tasks 1-7 and the additional ★ task, plus answers to the self-check questions. |
| `README.md` | This file. |

## Dataset

The notebooks use `sales.csv` - a coffee shop transactions dataset:

| Column | Description |
|--------|-------------|
| `date` | Transaction date |
| `datetime` | Transaction date and time |
| `cash_type` | Payment type (`card` / `cash`) |
| `card` | Anonymised card identifier (empty for cash payments) |
| `money` | Transaction amount |
| `coffee_name` | Name of the drink |

If `sales.csv` is not found on Google Drive, the notebooks automatically generate a small synthetic sample with the same structure (60 rows), so every cell can be run without extra preparation.

## How to run

1. Open [Google Colab](https://colab.research.google.com) and sign in with your Google account.
2. Choose **File → Upload notebook** and select one of the `.ipynb` files (or open it directly from GitHub).
3. Upload `sales.csv` to the root of your Google Drive (`MyDrive`), or skip this step to use the generated sample.
4. Run the cells in order with **Shift + Enter**. When prompted by `drive.mount('/content/drive')`, grant access to your Drive.

> Note: the notebooks save their output (`filtered_sales.csv`, `coffee_name_counts.csv`) to the root of Google Drive.

## Requirements

- Python 3 (pre-installed in Google Colab)
- `pandas`
- `numpy`

## What was covered

- Creating a `DataFrame` from a dictionary; the `Series` / `DataFrame` relationship
- Reading CSV files with `pd.read_csv()` and inspecting data: `head()`, `tail()`, `info()`, `describe()`, `columns`
- Label-based (`loc`) and position-based (`iloc`) indexing, and the difference between them after sorting
- Filtering with boolean masks and combining conditions with `&`
- Sorting with `sort_values()` (including `ascending=False`)
- Chaining filtering and sorting, and saving results with `to_csv(index=False)`
- Converting a text column to a datetime type with `pd.to_datetime()`
- A reusable function built on `value_counts()` and `sort_values()` (★ task)

## Author

Karpiuk
