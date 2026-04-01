# Super Dirty Students: End-to-End Data Cleaning Pipeline

## Project Overview
This project focuses on one of the most critical steps in data analytics: **Data Cleaning and Preprocessing**. Using a highly "dirty" dataset of student records, I developed a comprehensive Python pipeline to transform inconsistent, missing, and complex nested data into a structured, analysis-ready format.

The project demonstrates advanced data manipulation techniques, including regex-based cleaning, JSON flattening, and record validation.

## Problem Statement
The original dataset (`super_dirty_students.csv`) contained several data quality issues:
* **Inconsistent Formatting:** Mixed cases in gender and course names.
* **Complex Data Types:** Nested JSON structures and raw address strings.
* **Validation Issues:** Incorrect email formats and non-standardized phone numbers.
* **Structural Noise:** Duplicate rows, missing values (NaN), and inconsistent date formats.

## Project Workflow

### 1. Data Exploration & Initial Cleaning
* Identified missing values and data types across all columns.
* Performed string stripping and handled null values.

### 2. Numeric & Date Standardization
* Cleaned and converted `Age`, `Score`, `GPA`, and `Money Spent` into proper `int` and `float` types.
* Standardized multiple date formats into a single `YYYY-MM-DD HH:MM:SS` format using Pandas.

### 3. Advanced Validation (Regex)
* **Email Validation:** Standardized all emails to lowercase and identified invalid formats.
* **Phone Standardization:** Cleaned and formatted phone numbers to a unified international standard (e.g., `+998...`).

### 4. Handling Nested Structures (JSON & Address Parsing)
* **JSON Flattening:** Extracted and flattened the `profile_json` column into separate attributes: `hobbies`, `skills`, `family`, and `devices`.
* **Address Decomposition:** Parsed raw address strings into granular columns: `addr_city`, `addr_district`, and `addr_postal`.

### 5. Normalization & Deduplication
* Standardized categorical data (Gender: Male/Female/Unknown; Course: Data Science/Python/Other).
* Identified and removed duplicate records to ensure data integrity.

## Technical Highlights
* **Language:** Python
* **Libraries:** Pandas, NumPy, JSON, Re (Regular Expressions)
* **Techniques:** Lambda functions, JSON normalization, Regex patterns, Type casting, and Data validation.

## Results
* **Input:** `super_dirty_students.csv` (Raw, inconsistent data)
* **Output:** `super_dirty_students_cleaned.csv` (Fully cleaned and structured data)
* **QA Check:** Verified row counts, validated numeric ranges (GPA, scores), and confirmed zero duplicates in the final export.

---

## Project Presentation
For a detailed visual walkthrough of the challenges and solutions in this project, view my presentation here:
[View Project Presentation on Canva](https://www.canva.com/design/DAGgAPkRKvg/Dgc2MDymJjk6yKVKZS8tug/edit?utm_content=DAGgAPkRKvg&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
