
# 🌫️ Delhi Air Pollution Analysis Using Python
### A Data-Driven Study of Pollution Trends, Monitoring Stations, and Weather Associations

> **Project Type:** Data Analytics Final Project  
> **Domain:** Environmental Data Analytics  
> **Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn  
> **Dataset:** Delhi Air Quality Monitoring Data (2024–25)

---

## 📌 1. Project Overview

Delhi experiences varying levels of air pollution throughout the year. Understanding how pollution changes over time, differs across monitoring stations, and relates to weather conditions can help reveal important environmental patterns.

This project will use Python to analyze air-quality measurements from multiple monitoring stations across Delhi. The analysis will focus on data cleaning, exploratory data analysis (EDA), visualization, and the identification of meaningful, data-supported insights.

## 🎯 2. Project Objectives

- Collect and combine air-quality data from multiple monitoring stations.
- Clean missing values, duplicates, timestamps, and inconsistent data types.
- Analyze pollution trends across months, days, and hours.
- Compare PM2.5 and PM10 concentrations across monitoring stations.
- Investigate relationships among different pollutants.
- Explore associations between pollution and weather variables.
- Create at least **10 meaningful visualizations**.
- Identify at least **5 evidence-based insights**.

## 📂 3. Dataset Description

**Source:** [OpenCity — Delhi Air Quality Reports](https://data.opencity.in/dataset/delhi-hourly-air-quality-reports)

The dataset collection contains station-level CSV files labelled as 15-minute AQI data for 2024–25.

**Potential variables include:**

| Category | Variables |
|---|---|
| Particulate pollutants | PM2.5, PM10 |
| Gaseous pollutants | NO, NO2, NOx, CO, SO2, Ozone |
| Weather measurements | Temperature, humidity, wind speed, wind direction, rainfall |
| Identification and time | Station name, station ID, timestamp |

> The actual date range, measurement units, data types, and completeness will be verified before analysis.

## 🛠️ 4. Tools and Technologies

- **Python:** Main programming language
- **Pandas:** Data manipulation and cleaning
- **NumPy:** Numerical calculations
- **Matplotlib:** Data visualization
- **Seaborn:** Statistical charts and visualizations
- **Jupyter Notebook / Google Colab:** Analysis environment

## 🔍 5. Project Methodology

### Phase 1: Data Collection
Download the original CSV files for selected monitoring stations and document their sources.

### Phase 2: Data Understanding
Inspect dataset dimensions, columns, data types, timestamp ranges, missing values, and duplicates.

### Phase 3: Data Cleaning
Standardize column names, convert numeric measurements, parse timestamps consistently, and address missing or invalid records.

### Phase 4: Data Integration
Combine compatible station datasets while retaining station identifiers for comparison.

### Phase 5: Exploratory Data Analysis
Calculate summary statistics and investigate temporal trends, pollutant distributions, station differences, and correlations.

### Phase 6: Visualization
Create charts to communicate the main patterns and answer the research questions.

### Phase 7: Insights and Reporting
Summarize the findings using statistical evidence, visualizations, and clearly stated limitations.

## 📊 6. Planned Visualizations

1. **Monthly PM2.5 and PM10 Trends** — Line chart
2. **Top 10 Stations by Average PM2.5** — Horizontal bar chart
3. **Day-of-Week vs. Hour-of-Day Pollution** — Heatmap
4. **PM2.5 Distribution Across Stations** — Box plot
5. **Pollutant Correlation Analysis** — Correlation heatmap
6. **Temperature vs. PM2.5** — Scatter plot
7. **Rainfall and PM2.5 Comparison** — Grouped chart
8. **Hourly Pollutant Patterns** — Line chart
9. **Monthly Pollution-Category Distribution** — Stacked bar chart, if a documented categorization method is available
10. **Monthly PM2.5 Trends Across Stations** — Multi-line chart

## 💡 7. Key Research Questions

### Research Question 1: Seasonal Pollution
Which months record the highest and lowest average PM2.5 and PM10 concentrations?

### Research Question 2: Station-Level Differences
Which monitoring stations record comparatively high or low particulate pollution?

### Research Question 3: Daily and Weekly Patterns
How does pollution vary by hour of the day and day of the week?

### Research Question 4: Pollutant Relationships
Which pollutants show the strongest positive or negative correlations?

### Research Question 5: Weather Associations
How are temperature, relative humidity, wind speed, and rainfall associated with pollution concentrations?

> These are research questions to investigate. Final conclusions will be based on the actual analysis rather than assumptions.

## 📦 8. Expected Deliverables

- Original source CSV files
- Cleaned and integrated dataset
- Jupyter Notebook or Google Colab notebook
- At least 10 visualizations
- At least 5 evidence-based insights
- Final project report with methodology, findings, and limitations

## 🏁 9. Expected Outcome

> The project will deliver a reproducible Python-based analysis of Delhi's air-quality data, highlighting pollution trends over time, differences between monitoring stations, relationships among pollutants, and potential associations between air quality and weather conditions.

---

### 📚 Dataset Reference

OpenCity. *Delhi Air Quality Reports.*  
https://data.opencity.in/dataset/delhi-hourly-air-quality-reports
