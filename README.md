# HR Analytics - Employee Attrition Dashboard

A Power BI dashboard to analyze employee attrition patterns and find what factors are driving people to leave the company.

## What this project does

HR teams spend a lot of time figuring out why employees leave. This dashboard looks at 1,470 employee records across different departments and breaks down attrition by education, age group, salary, job role, and years at the company. The goal was to find where attrition is highest so the HR team can take action.

## Dataset

- Total employees: 1,470
- Employees who left (attrition): 237
- Attrition rate: 16.12%
- Average age: 37 years
- Average salary: 6.5K per month
- Average tenure: 7 years

## Dashboard features

**Overview page**
- Total employees, attrition count, attrition rate
- Average age, salary, and tenure of employees
- KPI cards for quick summary

**Attrition by Education**
- Which education background has the highest attrition
- Life Sciences and Medical fields show highest exit numbers

**Attrition by Age Group**
- Bar chart showing attrition count per age group
- 26-35 age group has the highest attrition

**Attrition by Salary Slab**
- Employees earning up to 5K per month leave the most
- Higher salary bands have significantly lower attrition

**Attrition by Job Role**
- Laboratory Technician and Sales Executive roles have highest attrition
- Research Director has lowest attrition

**Attrition by Years at Company**
- Employees in their first year and those around 5 years mark show spikes in attrition

**Department filter**
- All charts can be filtered by department: Human Resources, Research & Development, Sales

## Key findings

1. Most attrition happens in the 26-35 age group
2. Employees earning below 5K per month leave more than others
3. Laboratory Technicians and Sales Executives have the highest exit rate by role
4. First year of joining is the most critical - highest attrition happens here
5. Life Sciences education background has more attrition than others

## DAX measures used

```dax
Attrition Rate = 
DIVIDE(
    COUNTROWS(FILTER('HR Analytics', 'HR Analytics'[Attrition] = "Yes")),
    COUNTROWS('HR Analytics'),
    0
)

Avg Age = AVERAGE('HR Analytics'[Age])

Avg Salary = AVERAGE('HR Analytics'[MonthlyIncome])

Avg Tenure = AVERAGE('HR Analytics'[YearsAtCompany])
```

## Tech Stack

- Power BI Desktop
- Power Query (for data cleaning)
- DAX (for calculated measures)

## Files in this repo

```
HR-Analytics-Employee-Attrition-Dashboard/
│
├── Screenshot 2025-03-21 043142.png    # Dashboard screenshot
├── README.md                           # Project documentation
```

> Note: The .pbix Power BI file is not uploaded here as it contains the full data model. The screenshot above shows the complete dashboard.
