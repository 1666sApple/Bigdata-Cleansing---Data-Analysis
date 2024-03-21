# Bigdata Cleansing & Data Analysis

## Work Flow

This document outlines the common stages of a big data analysis project, including the tools and techniques used at each step.

### 1. Loading the Data

* **Techniques:**
    * Utilize tools like Apache Sqoop or Flume to transfer data from various sources.
    * Leverage cloud storage solutions (e.g., AWS S3, Azure Blob Storage) for scalable data ingestion.
    * Employ Python libraries like Pandas or Spark for programmatic data loading.

### 2. Data Cleansing

* **Techniques:**
    * Address missing values through techniques like imputation or deletion.
    * Handle inconsistencies and errors using data validation and correction methods.
    * Standardize data formats to ensure consistency for analysis.
    * Utilize Python libraries like Pandas or Spark for data cleaning tasks.

### 3. Analysis

* **Techniques:**
    * Perform exploratory data analysis (EDA) to understand data characteristics.
    * Employ statistical analysis methods to identify patterns and relationships.
    * Implement machine learning algorithms to build predictive models.
    * Leverage Apache Spark for large-scale data processing and analytics.
    * Utilize SQL for querying relational databases.
    * Employ Python libraries like Scikit-learn, TensorFlow, or PyTorch for machine learning.

### 4. Visualization & Reporting

* **Techniques:**
    * Create charts and graphs to communicate insights effectively.
    * Utilize tools like Tableau, Power BI, or Matplotlib for data visualization.
    * Generate reports for clear presentation of findings.

### 5. Tools and Technologies

* **Programming Languages:** Python (widely used for data manipulation and analysis)
* **SQL:** Essential for querying relational databases
* **Linux Terminal Commands:** Provide granular control for data processing tasks

## Clinical Trials Analysis - Big Data Project

This project investigates clinical trial data using Apache Spark SQL and PySpark (RDD and DataFrame).

### Data Description

The project utilizes two CSV files:

1. `clinicaltrial_2023.csv`: Contains information on individual clinical trials with various columns (including dates in different formats) and a potentially mixed first column.
2. `pharma.csv`: Provides a list of pharmaceutical companies for reference.

**Data Location:**

- `/FileStore/tables/clinicaltrial_2023.csv`
- `/FileStore/tables/pharma.csv`

### Tasks

This project addresses five key questions about the clinical trial data:

1. **Number of Distinct Studies:** Analyzes the dataset to determine the exact count of unique studies.
2. **Study Type Distribution:** Lists all types of studies present and their frequencies (ordered by descending frequency).
3. **Top 5 Conditions:** Identifies the five most prevalent conditions within the data and their corresponding frequencies.
4. **Non-Pharmaceutical Sponsors:** Discovers the ten most frequent sponsors who are not listed as pharmaceutical companies, along with their sponsored trial count. (Assumes `Parent Company` in `pharma.csv` contains all pharmaceutical entities).
5. **Completed Studies by Month (2023):** Plots the number of completed studies for each month in 2023 alongside a table summarizing the plotted values.

### Implementation

Each task is implemented three times:

1. **Spark SQL**
2. **PySpark (RDD)**
3. **PySpark (DataFrame)**

### Visualization

Visualizations for the results can be created using any suitable tool, including:

- Python's Matplotlib
- Python's Seaborn
- Other free/open-source tools
