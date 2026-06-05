# Overview

The purpose of this analysis is to examine the effect of internet voting on voter turnout in the canton of St. Gallen, Switzerland. This study aims to determine whether the introduction of internet voting significantly increases voter turnout in referendums. 

### Methodology:

1. **Methodological Framework**:
   - The study employs a difference-in-difference approach to exploit the quasi-random variation in the availability of internet voting across different municipalities in St. Gallen.
   - The analysis compares turnout changes before and after the introduction of internet voting between municipalities that adopted the technology and those that did not.

2. **Staggered Treatment and Heterogeneous Effects**:
   - Not all municipalities adopted internet voting simultaneously, creating a staggered treatment design.
   - To address potential biases from heterogenous treatment effects, the study utilizes a robust estimator to ensure clean comparisons between treated and not-yet-treated units.

3. **Data**:
   - The dataset includes turnout data from 75 municipalities over 69 referendums, with 18 municipalities introducing internet voting at some point in 2023 or 2024.
   - Summary statistics and control variables (demographic data and political sentiment) are used to support the analysis and ensure robustness.

4. **Empirical Models**:
   - A two-way fixed effects (TWFE) model is used as the baseline specification.
   - Additional specifications incorporate municipality-level linear time trends and demographic controls.
   - The final model specification tests for heterogeneous treatment effects by examining whether the impact of internet voting varies across different municipalities, particularly those with initially lower/higher turnout rates.

### Findings:
The main finding is that internet voting does not significantly increase turnout in the canton of St. Gallen. 


## Setup Instructions
   1. Clone the repository
   2. Create and activate virtual environment
         python -m venv env
         source env/bin/activate  (On Windows, use `env\Scripts\activate`)
   3. Install required packages
         pip install -r requirements.txt

## Running the Analysis
   Data cleaning: Run the data cleaning notebook to preprocess the raw data.
      jupyter notebook notebooks/data_cleaning.ipynb
   Summary Statistics: Generate summary statistics.
      jupyter notebook notebooks/summary_stats.ipynb
   Pre-trends Analysis: Check for pre-trends.
      jupyter notebook notebooks/pretrends.ipynb
   Difference-in-Differences Analysis: Run the difference-in-differences analysis.
      jupyter notebook notebooks/diff_in_diff.ipynb
   
