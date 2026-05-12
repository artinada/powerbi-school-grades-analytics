## Project Overview
### School Performance Analytics in Power BI

End-to-end analytical project built in Power BI using a simulated electronic school grading system.

The project demonstrates:
- data ingestion from CSV sources
- data cleaning and transformation in Power Query
- star schema data modeling
- DAX calculations
- calendar dimension creation
- interactive dashboard development
- KPI tracking and performance analysis

The solution was designed following BI and analytics best practices commonly used in production reporting environments.

## Business Problem

School management needs a centralized analytical system to monitor:
- student academic performance
- subject-level trends
- class performance
- grading distribution
- regional differences
- performance dynamics over time

The goal was to transform raw operational CSV files into a clean analytical model suitable for reporting and decision-making.

## Dataset Description

| File | Description |
| --- | --- |
| students.csv |	Student master data |
|grades.csv |	Fact table with grade records |
| teachers.csv |	Teacher dimension |
| subjects.csv |	Subject dimension |
| periods.csv |	Academic periods |
| classes.csv |	Class dimension |


## Project Structure
```
school-performance-analytics-powerbi/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── data/
│   ├── raw/
│   │   ├── students.csv
│   │   ├── classes.csv
│   │   ├── teachers.csv
│   │   ├── subjects.csv
│   │   ├── periods.csv
│   │   └── grades.csv
│   │
│   └── cleaned/
│       └── README.md
│
├── powerbi/
│   ├── School_Analytics.pbix
│   ├── screenshots/
│   │   ├── dashboard-overview.png
│   │   ├── data-model.png
│   │   ├── power-query.png
│   │   └── kpi-section.png
│   │
│   └── dax/
│       ├── measures.md
│       └── calendar-table.md
│
├── docs/
│   ├── business-case.md
│   ├── data-modeling.md
│   ├── data-cleaning.md
│   ├── data-validation.md
│   ├── dashboard-design.md
│   └── insights.md
│
└── assets/
    ├── star-schema.png
    └── dashboard-layout.png
```

## 9. Key Insights

<example>
  
- Mathematics and Science showed the highest average grades.
- Grade distribution varied significantly between regions.
- Semester 2 performance improved for most classes.
- Homework grades were consistently higher than exam grades.

## 10. Skills Demonstrated

- Power BI
- Power Query
- DAX
- Data Modeling
- Star Schema
- Data Cleaning
- Data Validation
- Dashboard Design
- KPI Development
- Data Visualization
- Analytical Thinking
