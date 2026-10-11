# Titanic Survival Analysis: An End-to-End Data Visualization Workflow

## Authors
- Frank Lin ([@frankaus1224](https://github.com/frankaus1224))

## Project Description
This project is an end-to-end analysis of the Titanic passenger dataset, which has 891 passengers and 12 variables. I want to find out which factors, such as sex, passenger class, and age, are linked to survival. I will clean the data, run statistical tests, and build static charts that tell a clear story. I will also build an interactive Plotly dashboard so that users can explore the data by themselves. The project does not use machine learning, and it focuses on responsible and reproducible data work.

## Project Outline/Plan
- **Milestone 0: Dataset selection and quality audit**
  - Choose the Titanic dataset and write a data dictionary
  - Check rows, columns, data types, missing values, duplicates, and outliers
- **Milestone 1: Cleaned data and statistics**
  - Clean missing values and document every cleaning decision
  - Compute descriptive statistics
  - Run statistical tests (t-test and chi-square)
- **Milestone 2: Static visualization story**
  - Create at least 5 static charts (PNG/PDF)
  - Write a design rationale, an accessibility check, and a bias critique
- **Milestone 3: Interactive dashboard prototype**
  - Build a Plotly dashboard (HTML file) with filters and hover details
  - Collect peer feedback and write a revision plan
- **Final project: Report and presentation**
  - Write a 5-10 page report and give an 8-minute presentation

## Interface Plan
- **Development:** Jupyter notebooks and Python scripts, with the whole project stored in this GitHub repository
- **Static charts:** Saved as PNG/PDF files made with matplotlib and seaborn
- **Interactive dashboard:** A Plotly HTML file that opens in any web browser
- **Interactions:** Hover to see passenger details, dropdown filters for passenger class and sex, and zoom/pan
- **Deployment:** None. I will provide the HTML file and the code

## Data Collection and Storage Plan (written by Author: Frank Lin)
- **Source:** Titanic passenger data from Data Science Dojo: https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv
- **Collection:** Load the CSV directly with `pandas.read_csv()` from the URL above
- **Raw data:** Saved in `data/raw/titanic.csv` and never edited by hand
- **Cleaned data:** Saved in `data/processed/titanic_clean.csv`, created by a cleaning script
- **Storage rule:** The `data/` folder is listed in `.gitignore`, because GitHub is for code, not data. Anyone can recreate the data by running the scripts
- **Initial quality audit:** 891 rows and 12 columns, with missing values in Age (about 20%), Cabin (about 77%), and Embarked (2 rows)

## Data Analysis and Visualization Plan (written by Author: Frank Lin)
- **Cleaning:** Drop Cabin (too many missing values), fill Age with the median by passenger class, fill Embarked with the mode, and keep the high fare values as real data. Every decision will be explained
- **Descriptive statistics:** Mean, median, min, max, and standard deviation for Age, Fare, SibSp, and Parch
- **Statistical tests:** Welch's t-test (and Mann-Whitney U test) for age of survivors vs non-survivors, and chi-square tests for sex vs survival and class vs survival
- **Static charts (at least 5):** Survival rate by class (bar), age distribution by survival (histogram), fare by class (box plot), survival by sex and class (grouped bar), and a correlation heatmap
- **Accessibility:** Use a colorblind-friendly palette, clear labels, and high contrast
- **Bias critique:** Discuss misleading bin sizes, missing data, hidden points in box plots, and the limits of 1912 data
- **Dashboard:** An interactive Plotly scatter plot with filters, plus an explanation of what interaction adds to the analysis
