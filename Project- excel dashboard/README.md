# Data Jobs Salary Dashboard
![Dash Board](https://github.com/Jainamjain2601/Excel-projects/blob/main/Resources/Salary_Dashboard.png)

## Overview
Welcome to the Data Jobs Salary Dashboard!
This project is designed to help job seekers explore salaries across different data roles and make smarter career choices.

I built this dashboard using real-world 2023 data shared through my Excel course — the focus was not just on presenting numbers but on creating insights.
The dataset covers everything from job titles and salaries to locations and key skills.
## What's Inside

    📂 Final file: 1_Salary_Dashboard.xlsx

    🔥 **Built** entirely in Excel, showcasing dashboard design, data analysis, and interactivity.
    **Luke Barousse**


Key Excel Skills Applied

    📉 Creating dynamic Charts (Bar Charts, Map Charts)

    🧮 Using powerful Formulas and Functions (like MEDIAN(), FILTER())

    ❎ Setting up Data Validation to control user inputs

About the Dataset

The dataset comes from real-world data science jobs in 2023 and includes:

    👨‍💼 Job Titles

    💰 Salary figures

    📍 Locations around the world

    🛠️ Skills and requirements

This made it possible to analyze salary trends based on role, country, and schedule type.
How the Dashboard Was Built
Charts and Visuals

    Data Science Salaries (Bar Chart)
    → A horizontal bar chart ranks job titles by median salary.
    → Easy to spot that Senior and Engineering roles usually lead the pack.

    Country Median Salaries (Map Chart)
    → A world map shows how salaries vary by region.
    → Color-coded for quick comparisons — spot high and low-paying countries at a glance!

Formulas and Functions

    Median Salary Calculation

=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*(jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)

This formula dynamically calculates median salaries based on job title, country, and schedule type — all without hardcoding anything.

    Unique Job Schedule Types

=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))

A clever use of FILTER() to clean up and create a unique list of job types, leaving out messy entries.
Data Validation Setup

To make the dashboard user-friendly, I added data validation so users can only select from clean, validated options for job titles, countries, and schedule types.
It keeps the data neat and ensures consistency.
Final Thoughts

This project was all about turning raw data into real, useful insights.
Using just Excel, I built a dashboard that lets users instantly understand how location, role, and work type impact salaries.

It’s a small project — but it shows how much you can do with just smart Excel techniques and a focus on user experience!

Would you also like a third version — maybe something even more formal (like for a portfolio or resume link)? 🎯
Or do you want me to show you how it would look already formatted with some emojis, bold headers, and GitHub Markdown style? 🚀

