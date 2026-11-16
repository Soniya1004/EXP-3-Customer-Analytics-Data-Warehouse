CUSTOMER ANALYTICS DATA WAREHOUSE
Experiment 3 - Exploratory Data Analysis and Visualization
Project Overview
This experiment performs Exploratory Data Analysis (EDA) and data visualization on customer demographic and account-related data. The analysis studies customer attributes and identifies patterns associated with customer churn.
Aim
To perform Exploratory Data Analysis (EDA) and data visualization on the Customer Analytics Data Warehouse dataset using Python.
Objectives
- Load and understand the dataset.
- Calculate measures of central tendency: mean, median and mode.
- Calculate measures of dispersion: standard deviation, variance, minimum, maximum, range and interquartile range (IQR).
- Examine relationships between numerical attributes using correlation analysis.
- Visualize distributions and relationships using a histogram, boxplot, heatmap and scatter plot.
- Interpret patterns related to customer churn.
Dataset
The supplied experiment uses a bank-customer dataset with fields such as CreditScore, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary and Exited.

The code expects a CSV file named Churn_Modelling.csv by default. The dataset itself is the customer-churn source data; Customer Analytics Data Warehouse is the project name used in the experiment. Make sure the CSV headers match the fields listed above.
Software and Libraries
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
Files
- Customer_Analytics_Data_Warehouse_Experiment_3.docx - editable experiment document
- Customer_Analytics_Data_Warehouse_Experiment_3.pdf - PDF version
- customer_analytics_eda.py - executable EDA program
- README.md - project documentation
Setup
Install Python 3, then install the required packages:
python -m pip install pandas numpy matplotlib seaborn
How to Run
1. Keep Churn_Modelling.csv in the same folder as customer_analytics_eda.py, or note its full path.
2. Open a terminal in the project folder.
3. Run:
python customer_analytics_eda.py --csv Churn_Modelling.csv
To save the charts without opening plot windows:
python customer_analytics_eda.py --csv Churn_Modelling.csv --no-show
To use a different CSV path and output folder:
python customer_analytics_eda.py --csv "data/Churn_Modelling.csv" --output-dir "eda_outputs"
Analysis Performed
1. Initial Exploration: displays dataset shape, column information, first five records and missing-value counts.
2. Central Tendency: calculates mean, median and mode for numerical attributes and mode for Geography and Gender when present.
3. Dispersion: calculates standard deviation, variance, minimum, maximum, range and IQR for available selected numerical attributes.
4. Correlation: calculates and displays the Pearson correlation matrix for the selected numerical attributes.
5. Visualization: creates an age histogram, balance-by-churn boxplot, correlation heatmap and age-versus-balance scatter plot.
6. Churn Summary: displays the counts and percentages for Exited (0 = stayed, 1 = left).
Generated Charts
The program creates the following PNG files in the output directory (default: eda_outputs):
- 01_customer_age_histogram.png
- 02_balance_by_churn_boxplot.png
- 03_customer_attribute_correlation_heatmap.png
- 04_customer_age_vs_balance_scatter.png
Notes
- The program requires the columns Age, Balance and Exited for the visualizations and churn summary.
- Other analysis columns are included when they are present in the CSV.
- The numerical inferences printed in the supplied experiment are based on its original example dataset/output. Actual values may differ if a different CSV version or modified data is used.
- Correlation indicates association, not causation.
Result
Exploratory Data Analysis is performed using descriptive statistics, correlation analysis and visualizations to understand the data distribution, variation and customer-churn patterns.
