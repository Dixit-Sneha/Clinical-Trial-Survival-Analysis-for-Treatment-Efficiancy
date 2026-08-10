# Clinical Trial Survival Analysis

A Python-based clinical trial survival analysis project that investigates patient survival outcomes and treatment effects using statistical survival modeling techniques. The project analyzes clinical trial data and applies Kaplan–Meier estimation, Log-Rank testing, and Cox regression models to understand survival patterns and the influence of patient and treatment characteristics.

## Project Overview

This project uses the **Veteran lung cancer clinical trial dataset**, containing 274 observations and variables such as treatment group, cell type, Karnofsky performance score, diagnosis time, age, and prior therapy status.

The analysis focuses on comparing survival outcomes between **standard and test treatment groups** and evaluating how clinical characteristics affect survival time.

## Key Analysis

* **Kaplan–Meier Survival Analysis**

  * Estimated overall survival probability over time.
  * Compared survival curves between standard and test treatment groups.
  * Calculated median survival for each treatment group.

* **Log-Rank Test**

  * Statistically compared survival distributions between the treatment groups.
  * Obtained a test statistic of **0.0116** with a p-value of **0.91423**.

* **Cox Proportional Hazards Model**

  * Evaluated the relationship between survival time and clinical covariates.
  * Included treatment, age, Karnofsky score, diagnosis time, cell type, and prior therapy.
  * Model concordance was **0.74**.

* **Time-Varying Cox Model**

  * Transformed the data into start–stop survival intervals.
  * Applied `CoxTimeVaryingFitter` to model survival with time-dependent observations.
  * The fitted model contained 128 subjects, 128 periods, and 128 observed events.

## Technologies Used

* **Python**
* **Pandas** – Data loading and manipulation
* **NumPy** – Numerical operations and data validation
* **Matplotlib** – Survival curve and coefficient visualization
* **Lifelines** – Kaplan–Meier estimation, Log-Rank testing, and Cox regression

## Workflow

```text
Clinical Trial Dataset
        ↓
Data Loading & Inspection
        ↓
Survival/Event Data Preparation
        ↓
Kaplan–Meier Analysis
        ↓
Treatment Group Comparison
        ↓
Log-Rank Test
        ↓
Cox Proportional Hazards Model
        ↓
Time-Varying Cox Model
        ↓
Statistical Interpretation & Visualization
```

## Key Findings

The Kaplan–Meier analysis produced median survival estimates of **95 days for the standard treatment group** and **52 days for the test treatment group**. However, the Log-Rank test produced a p-value of **0.91423**, indicating that the observed difference between the treatment survival distributions was not statistically significant in this analysis.

The Cox model showed a concordance index of **0.74**, with Karnofsky performance score and large-cell cancer type emerging as notable covariates in the fitted model.

## Project Structure

```text
Clinical-Trial-Survival-Analysis/
│
├── Sneha_Dixit_Clinical_Trial.ipynb
└── README.md
```

## How to Run

1. Clone the repository.
2. Open `Sneha_Dixit_Clinical_Trial.ipynb` in Jupyter Notebook or Google Colab.
3. Install the required dependency:

```bash
pip install lifelines pandas numpy matplotlib
```

4. Run the notebook cells sequentially.

## Purpose

This project demonstrates the practical application of **survival analysis and statistical modeling in clinical trial data**, with an emphasis on treatment comparison, survival estimation, and identifying clinical factors associated with patient survival.
