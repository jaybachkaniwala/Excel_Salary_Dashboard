# Excel_Salary_Dashboard

![Salary_Dashboard](https://github.com/user-attachments/assets/6bc66056-79d1-4d5a-b1b9-993c1185512d)

## Introduction
💡 This data science jobs salary dashboard was created to help potential job seekers to investigate salaries for their desired job titles, and how salaries can differ according to job title, location, and job type.

## Data
Data from: https://www.lukebarousse.com/excel

The dataset used for this project contains real-world data science job information from 2023. The dataset is available via the link above. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

### Dashboard File
📂 My final dashboard can be found here: [Salary_Dashboard.xlsx](https://github.com/user-attachments/files/18353342/Salary_Dashboard.xlsx)

## Excel Skills Used
The following Excel skills were utilized for analysis:

1. **🔣 Formulas & Functions**
- Logical Functions
- Array Formulas
- XLOOKUP
- Text Functions
  
2. **✅🚫 Data Validation**

3. **📊 Charts**
- Bar Charts
- Map Chart

## Dashboard Build

### 📈 Charts

#### 💰 Job Salaries Bar Chart

![Job_Title_Median_Salary_Chart](https://github.com/user-attachments/assets/d3dc50e4-ebcd-45e5-bf13-753a95442e06)

- 🛠️ **Type/Features:** Utilized bar chart feature with an optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries for different job titles. Chosen job title is also highlighted on the chart itself for visual purposes.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends by job title, notably that Senior roles and Engineers are higher-paying than Analyst roles.

### 🔣 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles based on different regions, and schedule types.
- 🔢 **Formula Purpose:** This formula populates the table created below, returning the median salary based on job title, country, and the job type specified.

#️⃣ Data Table

![Job_Title_Median_Salary_Data](https://github.com/user-attachments/assets/9234932d-a401-4801-ae86-ca8baa7ae070)

📋 Dashboard Implementation  

![Job_Title_Dashboard_Implementation](https://github.com/user-attachments/assets/59ac03f9-1e65-4f89-9ea6-d36fa50db506)

#### #️⃣ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below utilizes the `FILTER()` function to exclude entries containing "and" or commas, and also omits zero values. This cleans the data for analysis purposes.
  
- **🔢 Formula Purpose:** This formula populates the table created below, which gives us a list of unique job schedule types.

#️⃣ Data Table

![Job_Schedule_Type_Data](https://github.com/user-attachments/assets/323911c2-b6dc-49ac-9f5e-2170fee5b60f)

📋 Dashboard Implementation  

![Job_Schedule_Type_Dashboard_Implementation](https://github.com/user-attachments/assets/a83fcd8a-5fed-45a6-962e-f483a9720061)

### ✅🚫 Data Validation

#### 🔍 Filtered List

- 🔒🔑 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
- 🎯 User input is restricted to predefined, validated schedule types via a dropdown list for the user to choose from.
- 🚫 Incorrect or inconsistent entries are prevented ensuring data integrity.
- 👥 Overall usability of the dashboard is enhanced.


![Data_Validation_Example](https://github.com/user-attachments/assets/6a6f6772-ab93-47c6-bafc-d4541f32828e)

## Conclusion

- This dashboard was created to showcase insights into salary trends across various data-related job titles.
- This dashboard allows users to make informed decisions about their career paths.
- It also allows the jobs seekerto explore and understand how location and job type influence salaries.

## ✅ What I learned from this project 
During this project, I gained practical experience in advanced Excel tools and techniques, which enhanced my ability to work with a complex dataset, and then create an interactive and user-friendly dashboard to allow meaningful insights to be derived from it. 

This project has re-iterated the importance and value of data visualization for various stakeholders.







