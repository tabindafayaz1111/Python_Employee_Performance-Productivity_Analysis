# Employee Performance & Productivity Analysis

Exploratory data analysis of an HR dataset (300 employees) to understand the drivers of
**employee performance** and **productivity**, using Python (pandas, matplotlib, seaborn, plotly).

## Project overview

The project answers questions such as:

- Which departments, job roles, and age groups have the highest performance ratings?
- How do gender, remote-work percentage, and job satisfaction relate to performance?
- What factors most strongly correlate with a composite **Productivity Score**?
- Who are the top and bottom performers, and how is productivity distributed?

A custom **Productivity Score** is engineered from performance rating, job satisfaction,
and (normalized) training hours:

```
Productivity_Score = 0.5 * Performance Rating
                   + 0.3 * Job Satisfaction Score
                   + 0.2 * Training_norm
```

## Dataset

`data/HR_Employee_Performance_Dataset.xlsx` — 300 rows, 18 columns including department,
job role, experience, age, gender, salary, bonus, training hours, job satisfaction,
remote-work %, and promotion status.

## How to run

```bash
# 1. (optional) create a virtual environment
python -m venv .venv
.venv\Scripts\activate        # Windows
# source .venv/bin/activate   # macOS / Linux

# 2. install dependencies
pip install -r requirements.txt

# 3. launch the notebook
jupyter notebook Performance_Productivity_Analysis_project.ipynb
```

## Project structure

```
employee_performanceAndProductivity_analysis/
├── Performance_Productivity_Analysis_project.ipynb   # main analysis notebook
├── data/
│   └── HR_Employee_Performance_Dataset.xlsx          # source dataset
├── requirements.txt
├── .gitignore
└── README.md
```

## Key steps in the notebook

1. **Data loading & inspection** — shape, dtypes, summary stats, missing-value check.
2. **Feature engineering** — age groups, remote-work groups, satisfaction categories,
   experience groups, normalized training hours, and the composite Productivity Score.
3. **KPIs** — employee count, average experience, average performance rating,
   average salary, total training hours.
4. **Performance analysis** — charts by department, job role, age, gender, satisfaction,
   and remote work, plus a correlation heatmap.
5. **Productivity analysis** — productivity by department/age/gender, correlation with key
   factors, top/bottom performers, and productivity-level distribution.

## Tools

Python · pandas · NumPy · matplotlib · seaborn · plotly · Jupyter
