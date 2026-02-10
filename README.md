# Urban Transportation Ridership Analysis Documentation

## 1. Introduction

### 1.1 Project Overview
This project aims to analyze the urban transportation ridership data for the cities of Chicago and Philadelphia. As a Data Analyst for the urban transportation agency, the goal is to create an interactive Power BI dashboard that allows stakeholders to monitor the evolution of ridership, compare performance by line and type of day, and detect anomalies. The analysis will also provide strategic recommendations to optimize transportation services.

### 1.2 User Story
As a Data Analyst, I must produce an interactive Power BI dashboard to monitor the evolution of ridership, compare performance by line and type of day, and detect anomalies, in order to propose strategic recommendations for optimizing services.

## 2. Project Structure

### 2.1 GitHub Repository Structure
The project is organized into the following directories:

- **Data**: Contains the raw data files.
  - *Chicago (RDF)*
  - *Philadelphia (CSV)*
  - *Real-time APIs*: CTA Bus Tracker (Chicago), SEPTA TransitView (Philadelphia)
- **Notebooks**: Python code used for ETL processes and statistical analysis.
- **Power BI**: Power BI file containing the data model, DAX measures, and interactive dashboard.
- **Docs**: Documentation files (if applicable).
- **README.md**: Overview of the project, instructions for setup and execution.
  
### 2.2 Files in GitHub
- **README.md**: Explains the project context, objectives, setup instructions, and technical details.
- **Python Notebooks**: Contains scripts used for ETL, statistical analysis, and any machine learning models.
- **Power BI Report**: The main Power BI report file (`Urban_transport_Performance.pbix`) with all visualizations, DAX measures, and KPIs.
- **Jira/Confluence**: Documentation and tracking for the project.

## 3. Data Collection and Preparation

### 3.1 Data Sources
- **Chicago**: RDF data files containing monthly ridership by line and type of day.
- **Philadelphia**: CSV files containing the same structure as Chicago’s data.
- **Real-time APIs**: Real-time data provided by CTA Bus Tracker (Chicago) and SEPTA TransitView (Philadelphia).

### 3.2 Data Transformation
1. **Chicago RDF to CSV**: RDF data is transformed to CSV format using a Python script.
2. **Philadelphia CSV**: Data is imported directly and standardized.
3. **Real-time APIs**: Data is fetched via REST APIs for real-time ridership and punctuality data.

## 4. ETL Process & Python Notebook

### 4.1 ETL Process
- **Data Cleaning**: Missing values and duplicates are handled.
- **Transformation**: Data is cleaned and transformed using pandas and numpy libraries in Python.
- **Libraries Used**: pandas, numpy, scipy, statsmodels.

### 4.2 Python Code
The Python notebook includes scripts for:
- **RDF to CSV transformation**: This process is done using Python’s `rdflib` and `pandas` libraries.
- **Statistical Analysis**: Hypothesis tests, correlation tests, and other analyses are done using `scipy` and `statsmodels`.

## 5. Power BI Modeling and DAX

### 5.1 Data Modeling
The data model follows a **star schema** structure:
- **Fact Table**: `FactRidership` - Contains ridership data.
- **Dimension Tables**:
  - `DimDate`: Date-related dimensions.
  - `DimRoute`: Route-related dimensions.
  - `DimMode`: Transportation mode-related dimensions.

### 5.2 DAX Measures
The following KPIs and DAX measures have been created:
- **Monthly Ridership Growth (MoM)**: Measures the month-over-month ridership growth.
- **Percentage of Days Above Goals**: Percentage of days that meet or exceed performance goals.
- **Frequency-Weighted Performance Index**: A weighted measure of frequency and performance.
- **Standard Deviation of Ridership**: Measures the volatility in ridership by week.
- **Direct Benchmarking**: Comparison of ridership between Chicago and Philadelphia.

## 6. Statistical Analysis with Python

### 6.1 Hypothesis Testing
- **Normality Test (Shapiro-Wilk)**: Checks whether the ridership data follows a normal distribution.
- **t-test (Student’s Test)**: Compares the average ridership between different routes or cities.
- **ANOVA**: Analyzes the significant differences in ridership based on day type (Week, Saturday, Sunday).
- **Correlation (Pearson/Spearman)**: Measures the correlation between actual frequency and ridership volume.

## 7. Dashboard Design

### 7.1 Overview
- **Page 1**: Displays global KPIs, temporal trends, and filters (slicers) for interactivity.
- **Page 2**: Focuses on quality of service, analyzing the performance and correlation between API data and ridership.
- **Page 3**: Presents the statistical results, including visualizations of the Python-based hypothesis tests and comparative analysis.

## 8. Evaluation and Final Presentation

### 8.1 Presentation Breakdown
The final presentation is structured as follows:
1. **Introduction** (5 minutes)
   - Brief overview of the project context.
   - Problem and solution description.
2. **Solution and Project Presentation** (10 minutes)
   - Overview of the technologies and concepts used (Python, Power BI).
   - Demonstration of the Power BI dashboard.
3. **Technical Explanation** (10 minutes)
   - Explanation of DAX measures, Python integration, and the ETL process.
4. **Business Case and Use Case** (10 minutes)
   - Comparison between Chicago and Philadelphia.
   - Proposed recommendations for service optimization.
5. **Q&A** (5 minutes)
   - Exchange with the jury.

## 9. Conclusion
- **Key Findings**: Insights on ridership patterns, performance analysis, and areas for optimization.
- **Strategic Recommendations**: Suggestions to improve service efficiency based on the analysis.
