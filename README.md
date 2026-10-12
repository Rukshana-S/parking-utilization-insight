
# 🅿️ Parking Utilization Insight
### Data-Driven Parking Analysis for ParkSmart City Services

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=black)
![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Analysis_Completed-success?style=for-the-badge)

**Parking Utilization Insight** is a Data Science assessment project that analyzes parking session records to identify zone-wise parking activity, peak entry hours, parking duration patterns, and differences in recorded sessions across event and weather categories.

The project uses Python in Google Colab for data preprocessing and exploratory data analysis, followed by Microsoft Excel for PivotTables, visualizations, KPI summaries, and dashboard creation.

> **Note:** The datasets used in this assessment are synthetic sample data. Findings represent the supplied sample and should not be interpreted as verified real-world parking conditions.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Problem Statement](#-problem-statement)
- [Objectives](#-objectives)
- [Datasets](#-datasets)
- [Technology Stack](#-technology-stack)
- [Project Workflow](#-project-workflow)
- [Data Preprocessing](#-data-preprocessing)
- [Feature Engineering](#-feature-engineering)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Key Findings](#-key-findings)
- [Excel Dashboard](#-excel-dashboard)
- [Business Recommendations](#-business-recommendations)
- [Limitations](#-limitations)
- [Future Enhancements](#-future-enhancements)
- [Repository Structure](#-repository-structure)
- [How to Run](#-how-to-run)
- [Author](#-author)

---

## 📖 Project Overview

Parking facilities need to be managed efficiently to reduce congestion, improve space availability, and support better planning.

This project explores parking session data from multiple sources to understand how parking activity varies across zones and entry times. It also investigates parking duration by zone type and compares the distribution of recorded sessions across event and weather categories.

The analysis produces a cleaned dataset, descriptive summaries, visualizations, and an Excel dashboard to communicate findings clearly.

### Project Highlights

- Data cleaning and quality validation
- Integration of five CSV datasets
- Time-based feature engineering
- Zone-wise parking analysis
- Peak entry-hour identification
- Parking duration analysis
- Event and weather comparisons
- Excel PivotTables and charts
- KPI summary and dashboard
- Future scope for occupancy prediction

---

## 🎯 Problem Statement

Parking management requires an understanding of where and when parking facilities are used.

Without analyzing historical parking records, it can be difficult to identify frequently used zones, busy entry periods, differences in parking duration, or possible relationships between parking activity and contextual factors.

The objective of this project is to analyze the available parking data and generate preliminary insights that can support better parking management decisions.

---

## 🎯 Objectives

1. Understand the structure and quality of parking-related datasets.
2. Identify missing, duplicate, inconsistent, and invalid records.
3. Clean and combine data from multiple sources.
4. Engineer useful time-based and contextual features.
5. Analyze parking sessions across different zones.
6. Identify the busiest recorded entry hours.
7. Compare average parking duration across zone types.
8. Explore session distributions across event and weather categories.
9. Develop an Excel dashboard for presenting analytical findings.
10. Propose future enhancements for reliable parking occupancy prediction.

---

## 📂 Datasets

The project uses five CSV datasets supplied for the assessment.

| Dataset | Original Records | Attributes | Description |
|---|---:|---:|---|
| `parking_sessions.csv` | 500 | 6 | Parking sessions, timestamps, duration, and fee |
| `zones.csv` | 500 | 5 | Parking zones, locations, capacity, and zone type |
| `payments.csv` | 500 | 4 | Payment records, payment mode, and amount |
| `calendar.csv` | 500 | 4 | Dates, weekdays, holidays, and events |
| `weather.csv` | 500 | 3 | Rainfall indicator and temperature |

**Important:** These record counts refer to the original supplied files. The cleaned parking analysis contains 492 session records.

The datasets are synthetic and are used for demonstrating the data science workflow.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data processing and analysis |
| Google Colab | Cloud-based notebook environment |
| Pandas | Data cleaning, transformation, and aggregation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Microsoft Excel | PivotTables, charts, KPI summaries, and dashboard |
| GitHub | Source code and project documentation |

---

## 🔄 Project Workflow

The project follows this workflow:

1. **Data Collection** — Load the five CSV datasets.
2. **Data Understanding** — Inspect records, columns, types, and data quality.
3. **Data Cleaning** — Standardize labels and handle missing or invalid values.
4. **Data Integration** — Combine datasets using relevant identifiers and dates.
5. **Feature Engineering** — Create time-based and contextual features.
6. **Exploratory Data Analysis** — Analyze zone counts, entry hours, durations, events, and weather.
7. **Excel Visualization** — Create PivotTables, charts, and KPI summaries.
8. **Dashboard Development** — Consolidate five charts into one dashboard.
9. **Insight Generation** — Summarize findings and preliminary recommendations.

---

## 🧹 Data Preprocessing

The following data quality issues were investigated during preprocessing:

### Missing Values
- Missing parking exit timestamps
- Missing parking durations
- Missing payment amounts
- Other incomplete fields relevant to analysis

### Duplicate Records
Duplicate records were checked and removed according to the cleaning rules applied to session identifiers and session details.

### Inconsistent Labels
Parking zone labels were standardized to support consistent grouping and analysis.

### Invalid Values
- Negative parking durations were treated as invalid.
- Invalid timestamps and incomplete records were handled according to the cleaning logic.
- Invalid fee and capacity values were reviewed.

### Data Integration

The datasets were combined using relevant keys:

- Parking sessions and zone information
- Parking sessions and payment records
- Parking dates and calendar information
- Parking dates and weather information

After cleaning, the merged analytical dataset contained **492 parking session records**.

---

## ⚙️ Feature Engineering

The following features were used or created during analysis:

| Feature | Description |
|---|---|
| `zone` | Parking zone identifier |
| `zone_type` | Type of parking zone |
| `capacity` | Recorded parking capacity |
| `entry_hour` | Hour extracted from entry timestamp |
| `date` | Date associated with the parking session |
| `day_of_week` | Weekday of the session |
| `is_weekend` | Weekend indicator |
| `time_period` | Categorized entry period |
| `duration` | Parking duration in hours |
| `fee` | Recorded parking fee |
| `is_event_day` | Event-day indicator |
| `rain` | Rainfall indicator |
| `temperature` | Recorded temperature |

These features support grouping, descriptive analysis, and comparisons across time, zones, and contextual categories.

---

## 📊 Exploratory Data Analysis

### 1. Parking Sessions by Zone

The number of recorded sessions was grouped by parking zone to identify differences in recorded activity.

### 2. Peak Entry-Hour Analysis

Session counts were grouped by entry hour to identify the busiest recorded entry period.

### 3. Parking Duration by Zone Type

Average parking duration was compared across Commercial, Hospital, Recreational, and Transit zones.

### 4. Event Comparison

Recorded sessions were grouped by event-day indicator to compare event-associated and non-event-associated records.

### 5. Weather Comparison

Recorded sessions were grouped by rainfall indicator to compare rainy and non-rainy records.

### 6. Descriptive and Correlation Analysis

Descriptive statistics and numerical correlations were used to explore the distributions and relationships among selected numerical variables.

---

## 📈 Key Findings

### Overall KPI Summary

| Metric | Result |
|---|---:|
| Cleaned parking sessions | 492 |
| Average parking duration | 2.19 hours |
| Total recorded parking fees | 17,632.83 |
| Average recorded parking fee | 35.84 |

The currency of the fee field was not confirmed in the supplied information; therefore, monetary values are shown without a currency symbol.

### Parking Sessions by Zone

| Zone | Sessions |
|---|---:|
| Zone A | 104 |
| Zone B | 93 |
| Zone C | 89 |
| Zone D | 105 |
| Zone E | 101 |

**Finding:** Zone D has the highest recorded session count, with 105 sessions. Zone C has the lowest, with 89 sessions.

### Peak Entry Hour

| Entry Hour | Sessions |
|---|---:|
| 06:00 | 27 |
| 07:00 | 17 |
| 08:00 | 34 |
| 09:00 | 25 |
| 10:00 | 25 |
| 11:00 | 31 |
| 12:00 | 27 |
| 13:00 | 26 |
| 14:00 | 35 |
| 15:00 | 22 |
| 16:00 | 26 |
| 17:00 | 32 |
| 18:00 | 36 |
| 19:00 | 34 |
| 20:00 | 32 |
| 21:00 | 32 |
| 22:00 | 31 |

**Finding:** 18:00 (6 PM) is the busiest recorded entry hour, with 36 sessions.

### Average Parking Duration by Zone Type

| Zone Type | Average Duration |
|---|---:|
| Commercial | 2.18 hours |
| Hospital | 2.02 hours |
| Recreational | 2.33 hours |
| Transit | 2.24 hours |

**Finding:** Recreational zones have the longest average recorded parking duration, while Hospital zones have the shortest.

### Event Comparison

| Category | Recorded Sessions |
|---|---:|
| Non-event-associated records | 464 |
| Event-associated records | 28 |

### Weather Comparison

| Category | Recorded Sessions |
|---|---:|
| No-rain records | 363 |
| Rain-associated records | 129 |

**Interpretation note:** Event and weather values represent record counts. They are not normalized daily demand rates and do not demonstrate causal effects.

---

## 📊 Excel Dashboard

An Excel dashboard was created to consolidate the main analysis results into a single worksheet.

### Dashboard Components

1. **Parking Sessions by Zone** — Compares recorded sessions across Zone A to Zone E.
2. **Parking Demand by Entry Hour** — Displays session counts for each recorded entry hour.
3. **Average Parking Duration by Zone Type** — Compares duration across four zone types.
4. **Event vs Non-event Days** — Shows the distribution of records by event indicator.
5. **Rain vs No Rain** — Shows the distribution of records by rainfall indicator.

### KPI Summary

The KPI sheet displays:

- Total sessions
- Average duration
- Total parking fees
- Average parking fee

The dashboard provides a consolidated view of the descriptive analysis and supports presentation of the findings.

---

## 💡 Business Recommendations

Based on the preliminary sample analysis:

1. **Review Evening Activity**  
   Investigate recorded evening entry patterns to understand whether additional staffing or space availability measures are needed.

2. **Evaluate Zone Differences**  
   Examine the reasons for differences in session counts across zones before changing parking allocations.

3. **Review Parking Duration**  
   Investigate duration differences across zone types to inform future parking policies.

4. **Improve Data Quality**  
   Capture complete entry and exit timestamps and validate session durations, fees, and capacity records.

5. **Collect More Detailed Data**  
   Record parking activity at finer time intervals to enable reliable daily-demand and occupancy analysis.

6. **Develop Predictive Capabilities**  
   Build a reliable concurrent-occupancy dataset before implementing predictive models.

These recommendations are preliminary and should be validated with representative operational data.

---

## ⚠️ Limitations

- The datasets are synthetic sample data, not real-world operational records.
- The sample contains approximately one session per date, limiting interpretation of daily parking demand.
- Session counts do not represent simultaneous vehicle occupancy.
- The sessions-per-capacity measure is only a comparative indicator, not true occupancy.
- Event and weather comparisons use record counts and do not establish causal relationships.
- The supplied data does not yet support a reliable, validated occupancy prediction model.
- Model performance metrics have not been generated because a predictive model has not yet been trained and evaluated.

These limitations should be considered when interpreting the findings.

---

## 🚀 Future Enhancements

### 1. Concurrent Occupancy Calculation
Use valid entry and exit timestamps to calculate how many vehicles are parked in each zone at specific times.

### 2. Improved Data Collection
Collect real-world parking sessions with multiple records per day and reliable capacity information.

### 3. Machine Learning
Develop a **Random Forest Regressor** to predict the number of vehicles occupying a zone at a specified time, once reliable target labels are available.

Potential input features include zone, capacity, hour, day of week, historical occupancy, event indicators, rainfall, and temperature.

### 4. Model Evaluation
Evaluate the trained model using:

- R² Score
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)

No model performance values are reported at this stage because the model has not yet been trained.

### 5. Interactive Dashboard
Extend the current Excel dashboard into an interactive application with reliable data refresh, filters, and time-based occupancy visualization.

---

## 📁 Repository Structure

The repository may be organized as follows:

```text
parking-utilization-insight/
│
├── README.md
├── Parking_Utilization_Analysis.xlsx
├── Parking_Utilization_Insight_DS_Presentation.pptx
│
├── notebooks/
│   └── parking_utilization_analysis.ipynb
│
├── data/
│   ├── parking_sessions.csv
│   ├── zones.csv
│   ├── payments.csv
│   ├── calendar.csv
│   └── weather.csv
│
└── outputs/
    ├── cleaned_parking_analysis.csv
    └── analysis_summaries/
```

*Note: This is a suggested structure. Only files that are actually present in the repository should be listed as available project artifacts.*

---

## ▶️ How to Run

### Option 1: Google Colab

1. Open the project's `.ipynb` notebook in Google Colab.
2. Upload the five CSV datasets or place them in Google Drive.
3. Update the dataset directory path in the notebook.
4. Run the cells in order, from data loading through analysis and export.
5. Review the generated tables, charts, and output files.

### Option 2: Local Python Environment

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open the analysis notebook and ensure that the CSV files are available at the configured paths.

---

## 👩‍💻 Author

**Rukshana S**  
B.E. Computer Science and Engineering  
Sri Eshwar College of Engineering

GitHub: [rukshana-s](https://github.com/rukshana-s)

---

## 🏁 Conclusion

Parking Utilization Insight demonstrates an end-to-end introductory data science workflow, from data understanding and preprocessing to feature engineering, exploratory analysis, visualization, and business recommendations.

The analysis identifies differences in recorded parking sessions across zones, highlights the busiest recorded entry hour, and compares average parking duration by zone type. An Excel dashboard brings these findings together in a single view.

Future work will focus on reliable concurrent occupancy calculations, richer data collection, and a validated machine-learning model to support smarter parking management.

---

**Project:** Parking Utilization Insight  
**Organization / Case Study:** ParkSmart City Services  
**Domain:** Data Science and Smart-City Analytics
