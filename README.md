# Employee Workforce Analytics Dashboard

An interactive **Power BI** dashboard exploring workforce composition, hiring trends, attrition, employee satisfaction, income, experience, and demographics.

> **Dataset note:** The dataset contains 3,000 synthetic employee records for learning and portfolio demonstration. It is not real company data.

## Project Objectives
- Summarize the workforce using key performance indicators (KPIs).
- Compare employee counts across departments and locations.
- Explore hiring patterns by month and day.
- Analyze attrition by employment type and job role.
- Compare job satisfaction and average monthly income across departments.
- Explore education and gender distribution.
- Enable interactive analysis using Year and Location slicers.

## Tools and Skills
- Microsoft Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Excel
- Data cleaning and transformation
- Data modeling concepts
- Data visualization and dashboard design
- Interactive reporting and data storytelling

## Dashboard Features
- **KPI cards:** Total Employees, Average Monthly Income, Average Experience, and Total Attrition.
- **Department analysis:** Employee count by department.
- **Hiring trends:** Hiring patterns by month.
- **Location analysis:** Employee distribution by location.
- **Attrition analysis:** Attrition by employment type and job role.
- **Satisfaction analysis:** Average job satisfaction by department.
- **Demographic analysis:** Education and gender distribution.
- **Year-wise matrix:** Employee counts by year and department.
- **Interactive slicers:** Year and Location.

## Data Preparation
1. Imported the Excel dataset into Power BI Desktop.
2. Checked column names and data types.
3. Set `Hire Date` to the Date data type.
4. Validated numeric and categorical fields.
5. Sorted `Month Name` by `Month Sort` and `Day` by `Day Sort`.
6. Created measures and visuals for analysis.

## Example DAX Measures
Replace `'Employee Data'` if your Power BI table has a different name.

```DAX
Total Employees =
DISTINCTCOUNT('Employee Data'[Employee ID])
```

```DAX
Total Attrition =
CALCULATE(
    DISTINCTCOUNT('Employee Data'[Employee ID]),
    'Employee Data'[Attrition] = "Yes"
)
```

```DAX
Attrition Rate =
DIVIDE([Total Attrition], [Total Employees], 0)
```

```DAX
Average Monthly Income =
AVERAGE('Employee Data'[Monthly Income])
```

```DAX
Average Experience =
AVERAGE('Employee Data'[Total Experience (Years)])
```

## Key Observations
- The dataset contains **3,000 employee records**.
- It includes **365 attrition cases**, equivalent to an overall attrition rate of approximately **12.2%** (365 / 3,000).
- In the current report, IT has the highest employee count and HR has the lowest among the departments shown.

These observations describe this synthetic dataset only. Results may change when slicers are applied.

## How to Use
1. Open the `.pbix` file in Power BI Desktop.
2. If prompted, update the source path to the dataset.
3. Use the Year and Location slicers to filter the dashboard.
4. Select chart categories to cross-filter other visuals where enabled.
5. Clear slicers to return to the overall view.

## Suggested Repository Structure
```text
employee-workforce-analytics/
├── README.md
├── Employee_Workforce_Analytics_Project_Report.pdf
├── Employee_Workforce_Analytics_Dashboard.pbix
├── Employee_Workforce_Analytics_Dataset.xlsx
└── screenshots/
    └── dashboard-overview.png
```

Upload only files you have permission to share. Remove confidential information before publishing.

## Limitations
- The dataset is synthetic and may not reflect real workforce behavior.
- The dashboard is descriptive and does not prove the causes of attrition.
- Findings depend on data quality, measure definitions, and slicer selections.

## Future Enhancements
- Add attrition trends by year and month.
- Add attrition-rate breakdowns by department and job role.
- Create drill-through pages for department-level details.
- Add KPI definitions and tooltips.
- Document data refresh and validation steps.

## Conclusion
This project demonstrates a practical Power BI workflow covering data preparation, DAX-based measures, interactive visualizations, and dashboard storytelling.

**Project:** Employee Workforce Analytics Dashboard  
**Primary tool:** Microsoft Power BI
