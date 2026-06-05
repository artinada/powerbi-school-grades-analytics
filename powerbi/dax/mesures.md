## DAX Measures

Key DAX calculations:
- Global Grades Count = `CALCULATE(COUNTROWS(grades), ALL())`
- All Type Grades = `CALCULATE(COUNTROWS(grades), REMOVEFILTERS(grades[grade_type]))`
- Average Grade = `CALCULATE(AVERAGE(grades[grade_value]), REMOVEFILTERS(grades[grade_type]))`
- Exam Average Grade = `CALCULATE(
    AVERAGE(grades[grade_value]),
    REMOVEFILTERS(grades[grade_type]),
    grades[grade_type] = "exam"
) `
- Homework Average Grade = `CALCULATE(
    AVERAGE(grades[grade_value]),
    REMOVEFILTERS(grades[grade_type]),
    grades[grade_type] = "homework"
)`
- Test Average Grade = 
`CALCULATE(
    AVERAGE(grades[grade_value]),
    REMOVEFILTERS(grades[grade_type]),
    grades[grade_type] = "test"
  )`
- Project Average Grade = 
`CALCULATE(
    AVERAGE(grades[grade_value]),
    REMOVEFILTERS(grades[grade_type]),
    grades[grade_type] = "project"
)`
- Quiz Average Grade = 
`CALCULATE(
    AVERAGE(grades[grade_value]),
    REMOVEFILTERS(grades[grade_type]),
    grades[grade_type] = "quiz"
)`

- Neg Grades Count = `COUNTROWS(FILTER(grades, grades[grade_value]<=6))`
- Neg Grades Prop = `DIVIDE( _Measures[Neg Grades Count], _Measures[Total Grades])`

- Previous Grade = `CALCULATE(
AVERAGE(grades[grade_value]),
DATEADD('Calendar'[Date], -1, MONTH)
)`
- MoM_AG% =
```
VAR Result = DIVIDE(
_Measures[Average Grade]-_Measures[Previous Grade],
_Measures[Previous Grade]
)
RETURN
    IF(
        ISBLANK(_Measures[Previous Grade]) || _Measures[Previous Grade] = 0,
        BLANK(),
        Result
    )
```
- Average Grade MoM% = 
```
VAR __PREV_MONTH = CALCULATE([Average Grade], DATEADD('Calendar'[Date], -1, MONTH))
RETURN
	DIVIDE([Average Grade] - __PREV_MONTH, __PREV_MONTH)
```

- Average Grade YTD = `TOTALYTD([Average Grade], 'Calendar'[Date])`
