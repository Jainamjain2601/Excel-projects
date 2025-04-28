# Data Jobs Salary Dashboard
![Dash Board](https://github.com/Jainamjain2601/Excel-projects/blob/main/Resources/Salary_Dashboard.png)

## Overview
Welcome to the Data Jobs Salary Dashboard!
This project is designed to help job seekers explore salaries across different data roles and make smarter career choices.

I built this dashboard using real-world 2023 data shared through my Excel course — the focus was not just on presenting numbers but on creating insights.
The dataset covers everything from job titles and salaries to locations and key skills.
## What's Inside

📂 Final file: 1_Salary_Dashboard.xlsx

🔥 Built entirely in Excel, showcasing dashboard design, data analysis, and interactivity.
    


Key Excel Skills Applied

📉 Creating dynamic Charts (Bar Charts, Map Charts)

🧮 Using powerful Formulas and Functions.

❎ Setting up Data Validation to control user inputs

About the Dataset

The dataset comes from real-world data science jobs  and includes:

👨‍💼 Job Titles

💰 Salary figures

📍 Locations around the world

🛠️ Skills and requirements

## Dashboard's

### 📉 Charts

📊 **Data Science Salaries - Bar Chart**

![Dash Board](https://github.com/Jainamjain2601/Excel-projects/blob/main/Resources/Job_title.png)


🛠️ **Excel Tools Used:** Built with Excel’s bar chart feature, adding salary formatting and a clean layout for easier understanding.

🎨 **Why This Design?:** I chose a horizontal bar chart to make comparing median salaries across job roles quick and intuitive.

📉 **How I Organized It:** Sorted job titles from highest to lowest salary to immediately show which positions pay more.

💡 **What I Learned:** It’s clear that Senior-level and Engineering roles generally offer higher salaries compared to Analyst positions.

 **🗺️ Country Median Salaries - Map Chart**

 ![Dash Board](https://github.com/Jainamjain2601/Excel-projects/blob/main/Resources/Country.png)

 🧮 **Formulas and Functions**

    Median Salary Calculation

     =MEDIAN(
          IF(
            (jobs[job_title_short]=A2)*
            (jobs[job_country]=country)*
            (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
            (jobs[salary_year_avg]<>0),
            jobs[salary_year_avg]
            ) 
        )

    
🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.

📊 **Array Formula:** Utilizes MEDIAN() function with nested IF() statement to analyze an array.

🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.

🔢 **Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.


📉 **Dashboard Implementation**

 ![Dash Board](https://github.com/Jainamjain2601/Excel-projects/blob/main/Resources/Job_title.png)

 ⏰ **Job Schedule Type Count**  

To create a clean and unique list of job schedule types, I used the following Excel formula:

        =FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))

🔍 **Unique List Generation:** This formula filters out any schedule types containing "and" or commas, and removes zero values, ensuring a clean dataset.

🔢 **Purpose:** It generates a list of distinct job schedule types, providing a better foundation for further dashboard features.

📉 **Dashboard Implementation**


 ![Dash Board](https://github.com/Jainamjain2601/Excel-projects/blob/main/Resources/Job_type.png)


❎ Data Validation

🔍 Filtered List Implementation

🔒 Enhanced Data Validation:
I applied the filtered list to the Data Validation settings for fields like Job Title, Country, and Job Type.

🎯 Key Benefits:

Ensures user input is restricted to only predefined, validated options.

🚫 Prevents incorrect or inconsistent data entries.

👥 Improves the overall usability and reliability of the dashboard.

## 🏁 Conclusion

This dashboard was created to uncover insights into salary trends across a range of data-related job titles.
Using real-world data from my Excel course, I built a tool that empowers users to make smarter career decisions by analyzing how location, job title, and work type affect salaries.


