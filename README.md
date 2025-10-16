# Employee Attrition Analysis Using Python

## Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Dataset Information](#dataset-information)
- [Tools and Libraries Used](#tools-and-libraries-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Data Analysis](#data-analysis)
- [Key Insights](#key-insights)
- [Conclusion](#conclusion)
- [Author](#author)

---

## Project Overview
The purpose of this project is to analyze employee attrition data and understand factors that contribute to employees leaving an organization.  
Using Python, the dataset was cleaned, structured, and analyzed to identify employee trends, reasons for attrition, and key demographic patterns.

---

## Objectives
- Clean and preprocess employee data to ensure accuracy and consistency.  
- Identify duplicate, missing, and invalid records.  
- Analyze employee distribution by department, city, experience, and job title.  
- Explore attrition reasons and categories.  
- Derive meaningful insights from the analysis.

---

## Dataset Information
The dataset (`Attrition_dataset.csv`) contains details of employees such as:
- Employee ID  
- Gender  
- Date of Birth  
- Hire and Termination Dates  
- Job Title  
- Department  
- City  
- Experience (Length of Service)  
- Termination Type and Reason  
- Employment Status and Year  

Each row represents one employee record, and each column provides attributes related to employment history.

---

## Tools and Libraries Used
- **Python**
- **Pandas** – data manipulation and cleaning  
- **NumPy** – numerical operations  
- **Matplotlib / Seaborn** – data visualization  

---

## Data Cleaning and Preparation
The following steps were performed to clean and prepare the data:

1. **Removed duplicate entries** using the `drop_duplicates()` method.  
2. **Handled missing values** by dropping rows with null entries using `dropna()`.  
3. **Renamed columns** for better readability (e.g., `birthdate_key` → `DOB`, `orighiredate_key` → `hire_date`, `terminationdate_key` → `term_date`).  
4. **Converted date columns** (`recorddate_key`, `birthdate_key`, `orighiredate_key`, `terminationdate_key`) to datetime format.  
5. **Standardized column names** and string formats (e.g., converted “Active” or “Terminated” to title case).  
6. **Removed unnecessary columns** like `store_name` and `gender_short`.  
7. **Added new columns** such as:
   - `exp_level`: Categorized employees as *Junior*, *Mid-Senior*, or *Senior* based on years of experience.  

---

## Data Analysis

After cleaning, several analyses were performed:

- **Employee Count:**  
  Total number of employees using `df['ID'].count()`  

- **Unique Values:**  
  Found the count of unique departments, jobs, genders, cities, and business units.  

- **Termination Reasons:**  
  Listed all unique termination reasons and counted their occurrences.  

- **Experience Categorization:**  
  Classified employees into experience levels using `pd.cut()`.  

- **Sorting Operations:**  
  Sorted specific employee job titles in ascending and descending order using `sort_values()` and `sort_index()`.  

- **Attrition Details:**  
  Queried specific employees based on indexes (e.g., 0, 25, 700, 500) and retrieved their job, experience, and termination information.  

---

## Key Insights

- The dataset included employees from multiple departments and cities with varying experience levels.  
- Many employees had an “Active” status, while others were terminated for specific reasons such as *Retirement* or *Resignation*.  
- The experience-based grouping revealed that a significant number of employees fall under the *Mid-Senior* category.  
- Data cleaning showed several duplicates and missing records that were handled to ensure analysis accuracy.  

---

## Conclusion
This project helped understand how employee data can be processed, structured, and analyzed effectively using Python.  
The analysis provides a foundation for deeper studies such as attrition prediction or workforce trend modeling.

---

## Author
**Uppara Mahesh**  
Data Analyst | Python | Pandas | Matplotlib | Seaborn | Excel | Power BI
