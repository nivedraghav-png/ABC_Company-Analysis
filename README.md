# ABC Company Employee Data Analysis

## Project overview
This project analyses the ABC Company employee dataset supplied for the Python Module 1 end project. The original dataset contains **458 rows and 9 columns**. The work covers data inspection, the required height correction, employee distribution, age groups, salary expenditure, correlation, and visual storytelling.

## Tools and libraries
- Python
- Jupyter Notebook
- Pandas and NumPy
- Matplotlib and Seaborn

## Repository structure
```text
ABC_Company_Employee_Analysis/
├── data/
│   ├── ABC Company Dataset.csv
│   └── ABC_Employees_Cleaned.csv
├── notebooks/
│   └── Employee_Analysis.ipynb
├── visualizations/
│   ├── 01_team_distribution.png
│   ├── 02_position_distribution.png
│   ├── 03_age_groups.png
│   ├── 04_salary_expenditure.png
│   └── 05_age_salary_correlation.png
└── README.md
```

## How to run
1. Clone or download this repository.
2. Install the required packages:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Open the project folder in a terminal.
4. Start Jupyter:
   ```bash
   jupyter notebook
   ```
5. Open `notebooks/Employee_Analysis.ipynb` and run all cells.

## Data preprocessing
- Inspected dataset dimensions, data types, and missing values.
- Replaced all values in the `Height` column with random integers from **150 to 180 inclusive**, as required by the assignment.
- Used NumPy random seed `42` so the generated values are reproducible.
- Kept missing `College` and `Salary` values unchanged. Salary totals and age–salary correlation use available salary values only.

> **Note:** The replacement heights are synthetic values created solely to satisfy the assignment instruction. They do not represent actual employee heights.

## Analysis and findings

### 1. Employee distribution across teams
- The dataset includes **30 teams**.
- The largest team by headcount is **New Orleans Pelicans**, with **19 employees (4.15%)**.
- The notebook calculates each team's employee count and percentage of all 458 employees.

### 2. Employee distribution by position
- The most common position is **SG**, with **102 employees (22.27%)**.
- The notebook provides counts and percentage shares for every position.

### 3. Predominant age group
Age bands used: Under 20, 20–29, 30–39, and 40+.
- The predominant age group is **20–29**, with **334 employees (72.93%)**.

### 4. Salary expenditure
Salary expenditure is calculated as the **sum of recorded salaries**, not average salary.
- Highest-spending team: **Cleveland Cavaliers** – **106,988,689**.
- Highest-spending position: **C** – **466,377,332**.
- There are **447 non-missing salary records**; missing salaries are excluded from these totals.

### 5. Age and salary correlation
- Pearson correlation coefficient: **0.214**.
- This indicates a **weak positive linear association** in this dataset. It does not establish that age causes salary to increase.
- The scatter plot and regression line visualize the relationship.

## Visualizations
The `visualizations/` folder contains:
1. Employee count by team.
2. Employee distribution by position.
3. Employee age groups.
4. Salary expenditure by team and position.
5. Age versus salary correlation.

## Data story
The employee dataset spans 30 teams and five positions. The largest team and most common position can be identified from the distribution summaries, while the age-group analysis shows that employees are concentrated in the 20–29 band. Salary totals vary by team and position, with the Cleveland Cavaliers and Center (C) position having the largest aggregate recorded salary expenditure. Age and salary have a weak positive linear association, so age alone is not a strong predictor of salary in this dataset.

## Limitations
- Height values are randomized as instructed and are not valid real-world measurements.
- `College` and `Salary` contain missing values. The notebook reports missing values and does not fabricate replacements.
- Age-group boundaries are selected for this analysis because the assignment does not specify them.
- Aggregate salary expenditure is affected by team/position headcount as well as individual salary levels.

## Assignment coverage
This project addresses the preprocessing requirement, all five analysis tasks, graphical representations, and data-story requirement described in the assignment brief.
