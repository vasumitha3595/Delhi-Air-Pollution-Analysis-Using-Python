# Delhi Air Pollution Analysis Using Python

**A Data-Driven Study of Pollution Trends, Monitoring Stations, and Weather Associations**

| | |
|---|---|
| **Project Type** | Data Analytics Final Project |
| **Domain** | Environmental Data Analytics |
| **Tools** | Python, Pandas, NumPy, Matplotlib, Seaborn |
| **Dataset** | Delhi Air Quality Monitoring Data (2024–25) |
| **Environment** | Google Colab |

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-EDA-150458)
![NumPy](https://img.shields.io/badge/NumPy-Numerical-013243)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4c72b0)

---

## 📌 1. Project Overview

This project analyzes **hourly air-quality and weather data from 39 monitoring stations across Delhi (2024–2025)** using Python. It covers data cleaning, exploratory data analysis (EDA), statistical analysis and visualization to understand how pollution changes by **hour, day, month, season, station and weather condition**.

The goal is to turn raw sensor readings into useful information that supports air-quality monitoring and better decision-making.

## 📂 2. Data Source

| Item | Details |
|---|---|
| Dataset Name | Combined Delhi Air Quality Dataset (39 stations, hourly) |
| Source | [OpenCity – Delhi Hourly Air Quality Reports](https://data.opencity.in/dataset/delhi-hourly-air-quality-reports) (combined file hosted in this repository) |
| File | `delhi_39_stations_hourly_2024_2025.csv` |
| File Type | CSV |
| Location / Timeline | Delhi, India / 2024–2025 |
| Domain | Environmental Data Analytics |
| Records | 683,803 |
| Attributes | 30 |

The dataset contains hourly readings of pollutants (particulate matter, gases and volatile organic compounds) and weather variables (temperature, humidity, wind, rainfall, solar radiation and pressure) for each station.

## ❓ 3. Problem Statement

Delhi's air quality is monitored continuously, but the raw data has many stations, many pollutants and many gaps, which makes the patterns that matter hard to see. Without proper analysis it is difficult to tell **when, where and under what weather conditions** pollution becomes dangerous.

This project identifies the key factors (time, season, location and weather) that influence air pollution in Delhi and compares observed levels with health guidelines.

## 🎯 4. Objectives

**Data objectives**
- Understand the dataset structure
- Clean and prepare the data for analysis
- Handle missing values and duplicates
- Perform Exploratory Data Analysis
- Create meaningful visualizations
- Generate actionable insights

**Analytical objectives**
- Analyze hourly, daily, monthly and yearly pollution trends
- Compare PM2.5 and PM10 across monitoring stations
- Examine pollution distributions, variability and outliers
- Investigate correlations between different pollutants
- Study relationships between pollution and weather variables
- Compare weekday and weekend pollution levels
- Develop data-driven insights to support air-quality monitoring

**Project requirements at a glance**

| Requirement | Delivered |
|---|---|
| Combine data from multiple monitoring stations | ✅ 39 stations combined into one hourly dataset (683,803 records) |
| Clean missing values, duplicates, timestamps and data types | ✅ Section 7 |
| Trends across months, days and hours | ✅ Charts 5, 6, 7, 13 |
| Compare PM2.5 and PM10 across stations | ✅ Chart 4 |
| Relationships among pollutants | ✅ Chart 12 |
| Pollution vs weather variables | ✅ Charts 10, 11, 12, 14 |
| At least 10 meaningful visualizations | ✅ 15 charts |
| At least 5 evidence-based insights | ✅ 7 key findings (Section 11) |

## 🗂️ 5. Attribute Details

### Original columns (30)

| Attribute | Type | Description |
|---|---|---|
| Station ID | Text | Unique identifier of the monitoring station (39 stations) |
| State | Text | State of the station (Delhi) |
| City | Text | City of the station (Delhi) |
| Station Name | Text | Name of the monitoring station |
| Timestamp | Datetime | Date and hour of the record |
| readings_in_hour | Integer | Number of readings combined into the hourly record (typically 4) |
| PM2.5 (µg/m³) | Float | Fine particulate matter (diameter up to 2.5 µm) |
| PM10 (µg/m³) | Float | Coarse particulate matter (diameter up to 10 µm) |
| NO (µg/m³) | Float | Nitric oxide |
| NO2 (µg/m³) | Float | Nitrogen dioxide |
| NOx (ppb) | Float | Total oxides of nitrogen |
| NH3 (µg/m³) | Float | Ammonia |
| SO2 (µg/m³) | Float | Sulphur dioxide |
| CO (mg/m³) | Float | Carbon monoxide |
| Ozone (µg/m³) | Float | Ground-level ozone |
| Benzene (µg/m³) | Float | Benzene (volatile organic compound) |
| Toluene (µg/m³) | Float | Toluene (volatile organic compound) |
| Xylene (µg/m³) | Float | Xylene (about 90% missing) |
| O Xylene (µg/m³) | Float | O-Xylene (completely empty, dropped) |
| Eth-Benzene (µg/m³) | Float | Ethylbenzene (about 85% missing) |
| MP-Xylene (µg/m³) | Float | M,P-Xylene (about 85% missing) |
| AT (°C) | Float | Air temperature |
| RH (%) | Float | Relative humidity |
| WS (m/s) | Float | Wind speed |
| WD (deg) | Float | Wind direction (0–360) |
| RF (mm) | Float | Rainfall |
| TOT-RF (mm) | Float | Total rainfall |
| SR (W/mt2) | Float | Solar radiation |
| BP (mmHg) | Float | Barometric pressure |
| VWS (m/s) | Float | Vertical wind speed (about 86% missing) |

### Engineered features

| Feature | Description |
|---|---|
| hour, day, month, year | Time parts extracted from `Timestamp` |
| day_of_week | 0 = Monday … 6 = Sunday |
| is_weekend | 1 for Saturday and Sunday, otherwise 0 |
| Season | Winter (Dec–Feb), Summer (Mar–May), Monsoon (Jun–Sep), Post-Monsoon (Oct–Nov) |

## 🛠️ 6. Tools & Technologies

- **Python**
- **Pandas** – data handling and cleaning
- **NumPy** – numerical operations
- **Matplotlib** – plotting
- **Seaborn** – statistical visualization
- **Google Colab** – development environment

## 🧹 7. Data Pre-Processing & Feature Engineering

**Data cleaning steps**
- Checked data types of all columns
- Identified missing values
- Removed duplicate records (none found)
- Converted blank strings to missing values
- Converted `Timestamp` to datetime

**Missing-value strategy**
- Pollutant columns were filled with the **median of the same station**.
- Columns with less than 30% missing values were filled with the overall median.
- Air temperature and pressure were **interpolated within each station** (up to 8 hours), then filled with the station median.
- `O Xylene` (100% empty) was dropped. `Xylene`, `Eth-Benzene`, `MP-Xylene` and `VWS` (more than 85% missing) were left unfilled rather than inventing values.

**Feature engineering**
- Time features (hour, day, day of week, month, year, weekend flag) from `Timestamp`
- `Season` based on the Delhi climate calendar
- Chart-specific features: CPCB air-quality category from daily mean PM2.5, PM2.5/PM10 ratio per station, rain-level groups, 16 wind-direction sectors and weather bins

> Wind direction, rainfall and weather bins are analyzed on the **original (unfilled) data** so that median imputation does not distort the results.

## 🔎 8. Exploratory Data Analysis (EDA)

- **Structure:** 683,803 rows × 30 columns (24 float, 1 integer, 5 text)
- **Statistical summary:** `describe()` of all numerical columns
- **Missing values:** PM2.5 ~6% and PM10 ~5% missing; Toluene ~33%; Xylene, Eth-Benzene, MP-Xylene and VWS above 85%
- **Duplicates:** 0 duplicate rows
- **Coverage:** 39 unique monitoring stations

## 📐 9. Statistical Analysis

Measures used: mean, median, mode, minimum, maximum, variance, standard deviation, skewness and kurtosis.

| Variable | Mean | Median | Std. dev. | Skewness |
|---|---|---|---|---|
| PM2.5 (µg/m³) | 99.48 | 68.77 | 93.73 | 2.36 |
| PM10 (µg/m³) | 204.04 | 171.00 | 140.63 | 1.50 |
| NO2 (µg/m³) | 44.38 | 36.47 | 34.93 | 2.47 |
| CO (mg/m³) | 1.27 | 1.03 | 1.02 | 5.29 |
| Ozone (µg/m³) | 34.06 | 20.42 | 37.75 | 2.38 |
| AT (°C) | 26.35 | 27.70 | 6.51 | -0.79 |
| RH (%) | 64.06 | 65.25 | 17.80 | -0.40 |
| WS (m/s) | 0.97 | 0.77 | 0.90 | 7.15 |

**Interpretation:** The mean sits above the median for PM2.5 and PM10 because of extreme winter hours. Both are right-skewed, so the **median is used as the typical value** and the mean as a measure of overall exposure.

## 📊 10. Data Visualization

The project contains **15 visualizations**: 3 univariate, 8 bivariate and 4 multivariate, each followed by a short interpretation.

### Univariate analysis
| Chart | Description |
|---|---|
| 1 | Distribution of PM2.5 |
| 2 | Outliers and variability of PM2.5, PM10 and NO |
| 3 | Average pollutant concentration vs WHO guidelines |

### Bivariate analysis
| Chart | Description |
|---|---|
| 4 | Station-wise PM2.5 and PM10 |
| 5 | Monthly PM2.5 and PM10 trends by year |
| 6 | Daily trend of PM2.5 and PM10 |
| 7 | Air-quality category (CPCB) mix by month |
| 8 | Seasonal variation of pollutants |
| 9 | Weekday vs weekend PM2.5 |
| 10 | PM2.5 by wind direction (polar chart) |
| 11 | PM2.5 across wind speed, humidity, solar radiation and pressure bins |

### Multivariate analysis
| Chart | Description |
|---|---|
| 12 | Spearman correlation: weather variables vs pollutants |
| 13 | Hourly PM2.5 heatmap by month and year |
| 14 | Rain effect on particulate matter (scavenging) |
| 15 | Daily rhythm of six gaseous pollutants |

## 💡 11. Key Findings

- **Particulate matter far exceeds safe limits.** Average PM2.5 (99.48 µg/m³) and PM10 (204.04 µg/m³) are about **6.6× and 4.5×** the WHO 24-hour guidelines (15 and 45 µg/m³). NO2 (44.38 µg/m³) also exceeds its limit, while SO2 and CO stay within theirs.
- **Winter is the worst season.** November peaks at 226.15 µg/m³ PM2.5, **6.8× the August low** (33.30). In Nov-24 and Nov-25 nearly every day was Very Poor or Severe, while the monsoon months were the cleanest.
- **Hotspot stations.** Jahangirpuri, Anand Vihar and Wazirpur have the highest PM2.5 (~125–128 µg/m³); Mundka has the highest PM10 (~274 µg/m³).
- **Time of day matters.** PM2.5 is highest at night and early morning and lowest in the afternoon. Traffic-related gases peak in the evening and night (NO2 at 20:00, CO at 21:00).
- **Weather drives pollution.** Colder, calmer air traps pollutants (AT vs PM2.5 correlation −0.44; PM2.5 falls from 106 to 47 µg/m³ as wind speed rises). Rain lowers PM2.5 by about 15–20% and PM10 by about 22–29%.
- **Wind direction.** North-east winds carry the most polluted air (~123 µg/m³ PM2.5), about 1.6× the cleanest direction.
- **No weekday–weekend effect.** Daily mean PM2.5 stays between 95 and 102 µg/m³, so pollution is regional and weather-driven rather than tied to the working week.

## 🧠 12. Types of Analysis

| Type | What was done |
|---|---|
| **Descriptive** | Averages vs WHO guidelines; monthly, seasonal and station-wise levels; distributions and outliers |
| **Diagnostic** | Low wind, low temperature and stagnant air explain winter peaks; rain washes out coarse PM10 more than PM2.5; traffic gases peak in evening/night |
| **Predictive** | Repeating seasonal and hourly patterns give a baseline for anticipating winter spikes (no forecasting model built yet) |
| **Prescriptive** | Target chronic hotspot stations; focus alerts on 19:00–09:00 and winter months; fix data gaps in trace-gas monitoring |

## 🚀 13. Future Enhancements

- Add more years of data and station coordinates for spatial (map) analysis
- Apply machine learning (PM2.5 time-series forecasting or AQI category classification)
- Build interactive dashboards (Power BI, Tableau or Streamlit)
- Automate reporting so the analysis refreshes with new data
- Add external factors such as traffic, crop-residue burning and industrial emissions

## ✅ 14. Conclusion

Average PM2.5 and PM10 in Delhi are far above WHO health guidelines, making particulate matter the region's most acute air-quality problem. Pollution peaks in post-monsoon and winter (especially November), at night and early morning, and under cold, low-wind conditions, while monsoon rain cleans the air. There is no weekday–weekend difference.

These results can help authorities and monitoring agencies make better decisions by **targeting chronic hotspot stations and high-risk hours**, and by closing the data gaps in trace-gas measurements.

## ▶️ 15. How to Run

**Option A: Google Colab (recommended)**
1. Open `Delhi_Air_Quality_Updated.ipynb` in Google Colab (upload it or use *File → Open notebook → GitHub*).
2. Run all cells. The notebook loads the dataset directly from this repository.

**Option B: Locally**
```bash
git clone https://github.com/vasumitha3595/Delhi-Air-Pollution-Analysis-Using-Python.git
cd Delhi-Air-Pollution-Analysis-Using-Python
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Delhi_Air_Quality_Updated.ipynb
```

> The CSV is stored with Git LFS. If you clone locally, install [Git LFS](https://git-lfs.com) first (`git lfs install`) so the data file downloads correctly.

## 📁 16. Repository Structure

```
Delhi-Air-Pollution-Analysis-Using-Python/
├── Delhi_Air_Quality_Updated.ipynb          # Main analysis notebook
├── delhi_39_stations_hourly_2024_2025.csv   # Dataset (39 stations, hourly)
├── Delhi_Air_Quality_project.pdf            # Project report
└── README.md
```

---

⭐ If you found this project useful, consider giving it a star.
