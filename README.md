# EDA-5# Healthcare Data Analysis & Exploratory Data Analysis (EDA)

A Python-based Exploratory Data Analysis (EDA) project analyzing patient admission records, medical conditions, length of stay, and billing amounts from healthcare data.

---

## 📌 Project Overview

This project cleans, processes, and analyzes hospital admission records to uncover insights into patient demographics, admission types, length of stay, and billing distributions across different medical conditions.

### Key Objectives
- Perform data cleaning and handling of missing values.
- Clean and standardize categorical variables (e.g., standardizing `Admission_Type`).
- Perform feature engineering to derive new metrics like `stay_days` (length of stay).
- Conduct exploratory data analysis (EDA) using statistical summaries and visual distributions.

---

## 📊 Dataset Overview

The dataset contains **1,000 patient records** across **10 primary features**:

| Feature Name | Type | Description |
| :--- | :--- | :--- |
| **Patient_ID** | String | Unique identifier for each patient |
| **Age** | Integer | Patient age (ranging from 18 to 85 years) |
| **Gender** | Categorical | Female, Male |
| **Blood_Type** | Categorical | Blood group classification |
| **Medical_Condition** | Categorical | Condition (Arthritis, Asthma, Diabetes, Heart Disease, Hypertension) |
| **Medical_Code** | Categorical | Corresponding medical ICD code |
| **Date_of_Admission** | DateTime | Date the patient was admitted |
| **Discharge_Date** | DateTime | Date the patient was discharged |
| **Admission_Type** | Categorical | Emergency, Elective, Urgent |
| **Billing_Amount** | Float | Total bill amount charged (in USD) |

---

## 🛠️ Data Preprocessing & Feature Engineering

1. **Missing Value Handling:** Missing codes in `Medical_Code` (30 missing entries) were imputed with `'unknown'`.
2. **Text Normalization:** Standardized `Admission_Type` strings using `.str.strip()` and `.str.title()` to merge inconsistencies.
3. **Datetime Conversion:** Converted `Date_of_Admission` and `Discharge_Date` to standard pandas `datetime64[ns]` types.
4. **Feature Engineering:** 
   - Created `stay_days` calculated as `(Discharge_Date - Date_of_Admission)` to measure hospital length of stay.

---

## 📈 Key Findings & Summary Statistics

- **Admission Types Distribution:**
  - **Emergency:** 381 admissions
  - **Elective:** 368 admissions
  - **Urgent:** 251 admissions

- **Billing Statistics:**
  - **Mean Billing:** ~$77,117.52
  - **Median (50%):** ~$77,293.90
  - **Billing Range:** $5,568.16 to $149,921.80

- **Average Age by Condition:**
  - Diabetes: **53.1** years
  - Arthritis: **52.7** years
  - Heart Disease: **52.2** years
  - Hypertension: **51.4** years
  - Asthma: **49.9** years

---

## 🚀 Getting Started

### Prerequisites
Make sure you have the following Python libraries installed:
```bash
pip install pandas numpy matplotlib seaborn
