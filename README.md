## Project Overview
### School Performance Analytics in Power BI

End-to-end analytical project built in Power BI using a simulated electronic school grading system.

The project simulates a real-world scenario where management wants to monitor student performance trends over time and receive actionable analytical insights.

The objective of the project is to analyze academic performance trends, evaluate grade distributions, implement time intelligence calculations, and build a unified analytical product with consistent navigation and design.

The dashboard combines:

- analytical visuals,
- built-in Power BI Analytics tools,
- quick measures,
- time intelligence calculations,
- drill-through navigation,
- tooltip pages,
- standardized dashboard UX/UI design.

This project demonstrates the development of a comprehensive analytical dashboard in Power BI for an educational institution:

- data ingestion from CSV sources
- data cleaning and transformation in Power Query
- star schema data modeling
- DAX calculations
- calendar dimension creation
- interactive dashboard development
- KPI tracking and performance analysis

The solution was designed following BI and analytics best practices commonly used in production reporting environments.

## Business Problem

The dashboard answers the following business questions:

- How does the average grade change over time?
- Are there visible positive or negative trends?
- What values are considered typical (median and percentiles)?
- What performance can be expected in the next months?
- How are grades distributed across subjects?
- How does the cumulative average grade behave during the academic year?
- How does academic performance change Month-over-Month?

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

## Project Architecture
### Data Layer
- Prepared in Power Query
- Cleaned and transformed datasets
### Model Layer
- Star schema
- Calendar dimension
- Dedicated measure table
### Visualization Layer
- Interactive dashboards
- Drill-through pages
- Tooltips
- Time intelligence visuals

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
```

## Dashboard Pages
### 1. Academic Performance Overview

Main KPI overview of academic performance metrics.

Features:
- KPI cards
- Average Grade trends
- Subject analysis
- Interactive slicers
- Navigation menu

### 2. Class Performance

Detailed analysis of class-level performance.

Features:
- Comparative analysis
- Filtering by class and department
- Performance breakdowns
- Drill-through integration

### 3. Analytics & Time Intelligence

Core analytical page focused on advanced Power BI analytics.

Features:
- Percentiles (25th / Median / 75th)
- Trend line
- Constant reference line
- Forecasting with confidence interval
- YTD calculations
- Month-over-Month analysis
- Quick Measures
- “Show value as” calculations

### 4. Class Details

Detailed drill-through page for class-level inspection.

Features:
- Student-level details
- Dynamic context preservation
- Drill-through navigation

### 5. MoM%_AG_details

Tooltip page for detailed Month-over-Month explanations.

Features:
- Dynamic tooltip analytics
- Context-sensitive calculations
- Compact analytical insights

## Dashboard Design Principles
The report follows enterprise dashboard design principles:

- unified color palette,
- standardized KPI zones,
- reusable layout structure,
- consistent spacing,
- aligned slicers,
- predictable navigation,
- filter context preservation.

The dashboard is designed as a complete analytical product rather than isolated report pages.

## Business Recommendations
- Investigate the causes of lower performance in Computer Science courses.
- Review project assessment criteria and student support mechanisms, as projects exhibit the highest failure rate.
- Monitor testing practices, since tests account for the largest number of failing grades.
- Pay particular attention to periods preceding semester-end assessments, where seasonal declines in performance are observed.
- Continue monitoring long-term trends, although current forecasting indicates stable academic outcomes.

## Skills Demonstrated
### Power Query
- Data Cleaning
- Data Validation
### Power BI Analytics Features
- Analytics pane
- Percentiles
- Median lines
- Trend lines
- Forecasting
- Confidence intervals
### Time Intelligence
- Year-to-Date (YTD)
- Month-over-Month (MoM)
- Previous period comparison
- Cumulative calculations
### DAX
- TOTALYTD()
- CALCULATE()
- DATEADD()
- DIVIDE()
- Filter Context management
### Dashboard Engineering
- KPI Development
- Unified dashboard styling
- Navigation buttons
- Consistent UX/UI
- Layout standardization
- Filter context preservation
### Data Modeling
- Star schema
- Calendar table
- Measure tables
- Relationship management

## Tools Used
- Power BI
- DAX
- Power Query
- GitHub

## Author

Nadia Kamenski

Aspiring Data Analyst focused on Power BI, SQL, analytics engineering, and business intelligence solutions.

