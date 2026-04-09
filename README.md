# CSEC Data Science Bootcamp — Task 3 

A professional two-part data science notebook that covers:

- **Part 1:** Building a custom dataset in `pandas`
- **Part 2:** End-to-end Titanic dataset analysis (`train.csv`)

This Colab project is structured to demonstrate both fundamentals and practical analytics workflow.

---

## 🚀 Notebook Overview

### ✅ Part 1: Create Your Own Dataset (Foundation)

In Part 1, a custom student performance dataset is created with:

- **5 columns** (`Name`, `Age`, `Department`, `Score`, `Graduated`)
- **15 rows**
- **Custom index** from `S1` to `S15`

Learning outcomes:

- Creating a `DataFrame` from dictionaries/lists
- Applying custom row labels
- Verifying shape and structure

### ✅ Part 2: Titanic Dataset Analysis

In Part 2, a complete analysis workflow is applied to the Titanic training dataset:

1. **Data Exploration** (`head`, `info`, `describe`)
2. **Data Cleaning** (missing values + dropping high-missing column)
3. **Grouped Analysis** (`groupby` survival insights)
4. **Filtering** key passenger groups
5. **Insight Interpretation** from observed patterns

---

## 🧠 Core Analytical Logic

### Survival Rate Computation

For a selected group, survival rate is:

$$
	ext{Survival Rate} = \frac{\text{Survivors in Group}}{\text{Total Passengers in Group}}
$$

Since `Survived` is binary (`0`, `1`), the group mean directly gives survival probability:

- `df.groupby("Sex")["Survived"].mean()`
- `df.groupby("Pclass")["Survived"].mean()`
- `df.groupby("AgeGroup")["Survived"].mean()`

### Data Cleaning Strategy

- `Age` missing values → filled with **median**
- `Embarked` missing values → filled with **mode**
- `Cabin` column → dropped due to many missing values
- Duplicate rows → removed

### Age Group Engineering

Age bands are created with `pd.cut()`:

- Child: 0–12
- Teen: 13–18
- Adult: 19–60
- Senior: 61–100

This supports more interpretable survival comparisons.

---

## 📈 Key Insights (From Analysis)

1. **Females were much more likely to survive than males**
    - Typical result: female ≈ `0.74`, male ≈ `0.19`

2. **Passenger class strongly affected survival**
    - Typical result: Class 1 ≈ `0.63`, Class 2 ≈ `0.47`, Class 3 ≈ `0.24`

3. **Children had better survival rates than adults/seniors**
    - Consistent with historical evacuation priority patterns

4. **Highest survival profile**
    - Female + 1st Class + Child (often near complete survival in this dataset subset)

---



## ⚙️ Run in Google Colab

1. Open a new Colab notebook
2. Copy the Part 1 and Part 2 code blocks
3. Upload `train.csv` when running Part 2
4. Execute cells in order

If needed in Colab:

```python
import pandas as pd
```

---


## 🛠️ Troubleshooting

### `FileNotFoundError: train.csv`

Cause: The file is not in the current working directory.

Fix options:

- In Colab: upload `train.csv` to session files
- Locally: run from `Task3_Titanic` folder or use full file path

---

## ✅ Completion Checklist

- [x] Created a 15-row, 5-column custom dataset with custom index
- [x] Loaded Titanic training data
- [x] Performed `head`, `info`, and `describe` exploration
- [x] Cleaned missing values and removed unnecessary column
- [x] Computed survival metrics by gender, class, and age group
- [x] Filtered high-interest groups (female survivors, children survivors, 1st class survivors)
- [x] Documented clear, data-driven insights
