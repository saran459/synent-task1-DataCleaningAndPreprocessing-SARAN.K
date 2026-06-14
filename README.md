# Titanic Dataset Data Cleaning Project

## Problem Statement

Raw datasets often contain missing values, inconsistent formats, and unnecessary columns that can affect analysis and machine learning performance. The objective of this project is to clean and prepare the Titanic dataset by handling missing values, removing irrelevant data, converting data types, and creating a dataset ready for further analysis.

---

## Dataset Details

The Titanic dataset contains information about passengers who traveled on the Titanic.

### Features

| Column Name      | Description                          |
| ---------------- | ------------------------------------ |
| Passenger_ID     | Unique identifier for each passenger |
| Survived         | Survival status (0 = No, 1 = Yes)    |
| Passenger_Class  | Ticket class of passenger            |
| Passenger_Name   | Name of passenger                    |
| Sex              | Gender of passenger                  |
| Age              | Age of passenger                     |
| Siblings_Spouses | Number of siblings/spouses aboard    |
| Parents_Children | Number of parents/children aboard    |
| Ticket_ID        | Ticket number                        |
| cost             | Ticket fare paid                     |
| Cabin_ID         | Cabin number                         |
| Port             | Port of embarkation                  |

### Dataset Issues Identified

* Missing values in Age column
* Missing values in Port column
* Large number of missing values in Cabin_ID column

---

## Approach

### 1. Data Loading

* Imported the dataset using Pandas.
* Examined dataset structure using `head()`, `info()`, and `isnull().sum()`.

### 2. Handling Missing Values

* Filled missing values in the **Age** column using the median age.
* Filled missing values in the **Port** column using the mode (most frequent value).
* Removed the **Cabin_ID** column due to a high number of missing values.

### 3. Data Transformation

* Renamed column names to improve readability.
* Converted categorical values in the **Sex** column into numerical values:

  * Male → 1
  * Female → 0

### 4. Duplicate Check

* Checked for duplicate records using `duplicated().sum()`.
* No duplicate records were found in the dataset.

### 5. Validation

* Verified that all remaining columns contained no missing values.
* Reviewed data types and dataset structure after cleaning.

---

## Results

After data cleaning:

* Missing values in Age were successfully handled.
* Missing values in Port were filled.
* Cabin_ID column was removed.
* Sex column was encoded into numerical format.
* No duplicate records were present.
* Dataset became clean and suitable for data analysis and machine learning applications.

### Final Outcome

A cleaned Titanic dataset was generated and saved as:

`Titanic_Cleaned.csv`

The dataset is now ready for:

* Exploratory Data Analysis (EDA)
* Data Visualization
* Machine Learning Model Development
* Statistical Analysis

