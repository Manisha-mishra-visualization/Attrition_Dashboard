# Attrition Exit Analysis Dashboard

A Power BI dashboard analyzing employee attrition through the lens of exit reasons, location, job level, and monthly trends — built to support retention strategy and exit-interview follow-up.

![Dashboard Overview](docs/screenshots/overview_dashboard.png)

## Overview

Attrition analytics dashboard breaking down exit reasons, voluntary vs. involuntary attrition, and monthly trends across departments, locations, and job levels. Covers 500 total employees with an 11.40% attrition rate (8.60% voluntary, 2.80% involuntary), filterable by job level, department, and location. Built in Power BI with DAX.

## Key Metrics

| Metric | Value |
|---|---|
| Total Employees | 500 |
| Attrition Rate | 11.40% |
| Voluntary Attrition Rate | 8.60% |
| Involuntary Attrition Rate | 2.80% |

## Dashboard Sections

- **Exit Reason by Department** — bar chart ranking exit reasons: Work-Life Balance (14), Career Growth (10), Compensation (9), Business Restructuring (6), Performance (6), Manager (5), Relocation (5), Policy Violation (2).
- **Voluntary Attrition Rate by Location** — bar chart across Delhi (90), Pune (80), Bangalore (78), Chennai (75), Hyderabad (60), and Mumbai (60).
- **Attrition Rate by Job Level** — pie chart showing L2 leading at 33.33% (19 employees), followed by L4 at 28.07% (16), L3 at 26.32% (15), and L1 at 10.53% (6).
- **Monthly Attrition by Department** — trend line tracking attrition month-by-month across Finance, HR, IT, Marketing, Operations, and Sales from 2024 through 2026.

## Filters

- **Job_Level** — filter all visuals by job level.
- **Department** — filter all visuals by department.
- **Location** — filter all visuals by location.

## Tech Stack

- **Power BI Desktop** — dashboard authoring
- **Power Query (M)** — data transformation
- **DAX** — calculated measures (see [docs/dax_measures.md](docs/dax_measures.md))

## Data

> **No real employee data is included in this repository.** Place your own dataset in `data/raw/` before opening the `.pbix` file, or point Power BI to your own data source. See [docs/data_dictionary.md](docs/data_dictionary.md) for expected columns.
>
> Exit reasons, location, and department-level attrition are moderately sensitive HR data — review before publishing real data publicly, and consider anonymizing or keeping the repo private.

## Repository Structure

```
Attrition-Exit-Analysis-Dashboard/
├── data/
│   ├── raw/            # original/source dataset (not committed if sensitive)
│   └── processed/      # cleaned data used by the model
├── pbix/
│   └── Attrition_Dashboard.pbix
├── docs/
│   ├── screenshots/    # dashboard images for this README
│   ├── data_dictionary.md
│   └── dax_measures.md
├── reports/
│   └── Attrition_Dashboard.pdf   # optional exported PDF view
├── .gitignore
├── .gitattributes
└── README.md
```

## Getting Started

1. Clone this repository.
   ```bash
   git clone https://github.com/<your-username>/Attrition-Exit-Analysis-Dashboard.git
   ```
2. Add your dataset to `data/raw/`.
3. Open `pbix/Attrition_Dashboard.pbix` in **Power BI Desktop**.
4. Update the data source path/connection if needed (Home → Transform Data → Data Source Settings).
5. Refresh the data and explore.

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

## Data Privacy

If your `.pbix` file is connected to real employee data, **do not commit that data** to a public repository. Use anonymized/synthetic data, or keep the repo private.
