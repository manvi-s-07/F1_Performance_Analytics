# Formula 1 Performance, Reliability & Decision Analytics

An independent analytics and business intelligence extension of a prior University of Maryland data science project.

This project uses historical Formula 1 data from 1950–2024 to build a reusable reporting workflow for analyzing driver performance, constructor performance, reliability, and data quality.

The current implementation uses Excel and Power Query to clean, integrate, validate, and summarize multiple related datasets. The project is being extended into Power BI for interactive reporting and dashboard development.

## Project Goals

The goal of this project is to turn multiple historical Formula 1 datasets into a structured and reusable analytics workflow rather than relying on one-time analysis.

The project focuses on:

- Multi-source data integration
- Data cleaning and validation
- Data quality analysis
- Driver and constructor performance reporting
- Reliability analysis
- Interactive Excel reporting
- Repeatable Power Query workflows
- Power BI dashboard development

## Data

The project uses five related Formula 1 datasets:

- `results.csv`
- `drivers.csv`
- `constructors.csv`
- `races.csv`
- `status.csv`

The main results dataset contains approximately 26,759 race-result records spanning 1950–2024.

The datasets are connected through identifiers such as:

- `raceId`
- `driverId`
- `constructorId`
- `statusId`

## Current Workflow

### 1. Data Import and Cleaning

Power Query is used to create reusable connections for each source dataset:

- `qResults`
- `qDrivers`
- `qConstructors`
- `qRaces`
- `qStatus`

Cleaning steps include:

- Removing unnecessary fields
- Handling missing values
- Standardizing numeric, text, and date types
- Preserving valid historical records
- Validating identifier fields

### 2. Data Integration

A central reporting query, `qRacePerformance`, combines the five source datasets using key-based joins.

The reporting table includes readable driver, constructor, race, and race-status information alongside performance metrics.

### 3. Engineered Metrics

Additional fields were created to support analysis, including:

- Positions Gained
- Win Flag
- Podium Flag
- Points Flag
- Reliability Category

Reliability statuses are grouped into broader categories such as:

- Completed
- Classified / Lapped
- Mechanical
- Collision / Incident
- Other

## Data Quality Checks

A dedicated Excel data-quality report validates the transformed dataset.

Current checks include:

| Check | Result |
|---|---:|
| Total Rows | 26,759 |
| Missing Position | 10,953 |
| Missing Race Time | 19,079 |
| Missing Fastest Lap | 18,507 |
| Missing Fastest Lap Speed | 18,507 |
| Duplicate Result IDs | 0 |

These checks are important because historical Formula 1 data has uneven coverage across different metrics and eras.

## Excel Reporting

### Driver Summary

Driver-level reporting currently includes:

- Nationality
- Starts
- Wins
- Podiums
- Total Points
- Average Grid Position
- Average Finish
- Average Positions Gained
- Points-Scoring Rate

### Constructor Summary

Constructor-level reporting currently includes:

- Nationality
- Starts
- Wins
- Podiums
- Total Points
- Average Grid Position
- Average Finish
- Average Positions Gained
- Completion Rate
- Mechanical DNF Rate

Excel functions and features used include:

- XLOOKUP
- COUNTIF / COUNTIFS
- SUMIFS
- AVERAGEIFS
- SUMPRODUCT
- PivotTables
- PivotCharts
- Slicers
- Interactive year filtering

## Tools

- Microsoft Excel
- Power Query
- Python / pandas from the original analysis
- SQL concepts and relational data modeling
- Git / GitHub
- Power BI — currently being developed

## Project Structure

F1_Performance_Analytics/
│
├── data/
│   ├── documentation/
│   └── raw/
│       ├── constructors.csv
│       ├── drivers.csv
│       ├── races.csv
│       ├── results.csv
│       └── status.csv
│
├── docs/
├── excel/
│   └── F1_Performance_Analytics.xlsx
│
├── images/
├── powerbi/
├── .gitignore
└── README.md

## Current Status

### Completed

- Power Query source connections
- Data cleaning and type validation
- Multi-table integration
- Data quality checks
- Driver summary reporting
- Constructor summary reporting
- Initial PivotTable and PivotChart analysis
- Interactive year filtering

### In Progress

- Additional driver and reliability PivotTable analysis
- Power BI relational data model
- DAX measures
- Interactive Power BI dashboards
- Final documentation and dashboard screenshots

## Planned Power BI Analysis

The Power BI portion will include reporting for:

- Overall performance trends
- Driver performance
- Constructor performance
- Reliability and mechanical failures
- Historical trends
- Data quality and metric coverage

Planned measures include:

- Total Starts
- Wins
- Podiums
- Total Points
- Average Grid Position
- Average Finish
- Average Positions Gained
- Win Rate
- Podium Rate
- Completion Rate
- Mechanical DNF Rate
- Points per Start

## Project Background and Attribution

This project is an independent extension of a collaborative University of Maryland data science project completed in Summer 2025.

The original team project used Python, pandas, statistical analysis, visualization, and machine learning to study Formula 1 race performance.

My documented contributions to the original collaborative project included exploratory and statistical analysis, interpretation of results, final insights and conclusions, and coordination of the written analytical narrative.

The Excel, Power Query, reporting, data-quality, reliability, and upcoming Power BI work in this repository are part of my independent extension of that earlier project.

## Author

Manvi Sharma  
M.S. Data Science  
University of Maryland, College Park