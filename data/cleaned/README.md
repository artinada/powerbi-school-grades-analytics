Raw source files are preserved unchanged in the /raw layer.

All transformations were performed non-destructively in Power Query.

# Cleaned Data Layer

This folder contains cleaned and standardized datasets prepared for analytical modeling in Power BI.

The cleaned layer was created after performing data quality validation and transformation steps in Power Query.

## Objectives

The purpose of the cleaned layer is to:
- standardize raw source data
- ensure consistent data types
- normalize date formats
- remove invalid or duplicate records
- validate relationships between tables
- prepare data for Star Schema modeling

## Cleaning & Transformation Steps

### General transformations
- Trimmed extra spaces from text fields
- Standardized column naming conventions
- Corrected data types
- Validated numeric fields
- Removed duplicate records where necessary

### Date normalization
All dates were standardized using en-US locale settings.

Affected columns:
- students.birth_date
- teachers.hire_date
- periods.start_date
- periods.end_date
- grades.grade_date

Target format:
- Date type (Power BI internal date format)

### grades.csv transformations
- Converted grade_value from text to numeric
- Checked valid grade range (1–12)
- Identified blank grade_type values
- Validated foreign keys:
  - student_id
  - subject_id
  - teacher_id
  - period_id

### students.csv transformations
- Validated uniqueness of student_id
- Checked missing emails
- Verified class_id integrity

### classes.csv transformations
- Validated uniqueness of class_id
- Verified relationships with teachers table

## Data Quality Checks

Validation rules applied:

| Rule | Status |
|---|---|
| Unique student_id | Passed |
| Unique teacher_id | Passed |
| Unique subject_id | Passed |
| Unique class_id | Passed |
| Valid grade values (1–12) | Passed |
| Valid date conversion | Passed |
| Referential integrity checks | Passed |

## Final Analytical Usage

The cleaned datasets were loaded into the Power BI semantic model and used to build:
- fact table: grades
- dimensions:
  - students
  - classes
  - teachers
  - subjects
  - periods
  - calendar

The final model follows Star Schema principles.
