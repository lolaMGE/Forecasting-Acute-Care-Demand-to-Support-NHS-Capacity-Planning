# Forecasting-Acute-Care-Demand-to-Support-NHS-Capacity-Planning
This project is designed to forecast the healthcare demand of citizens to support operational planning and decision-making
### Project Overview

The NHS continuously faces intense pressure on acute care services driven by seasonal illness, demographic change, workforce constraints, and system shocks (e.g. winter surges). Inaccurate demand forecasting contributes to bed shortages, prolonged A&E waiting times, elective care backlogs, and inefficient use of clinical staff.

This project aims to develop robust, interpretable forecasting models to predict short- and medium-term acute care demand across NHS hospitals. The outputs are designed to support capacity planning, decisions-making  including bed allocation, staffing levels, escalation planning, and winter preparedness.

Using historical NHS activity data combined with calendar, weather, and population health indicators, the project delivers actionable insights for forecasts at daily and weekly horizons, with clear uncertainty bounds to support operational and strategic decision-making.

### Objectives

The key objectives of the project are to:

a. Forecast acute care demand (e.g. emergency admissions, bed occupancy, A&E attendances) at hospital or Trust level.

b. Capture seasonal and structural patterns, including winter pressures, bank holidays, and long-term trends.

c. Quantify uncertainty to help planners understand best- and worst-case scenarios.

d. Evaluate model performance using appropriate time-series validation methods.

e. Translate forecasts into operational insights that can inform NHS capacity planning and policy decisions.

### Data Sources

The project uses publicly available and simulated NHS-style datasets to reflect realistic operational conditions, including:

Hospital Episode Statistics (HES) – emergency admissions and length of stay

A&E Attendances and Emergency Admissions (NHS England)

Bed Availability and Occupancy Returns (KH03)

Calendar features – day of week, bank holidays, school holidays

Weather indicators – temperature, cold snaps (proxy for respiratory illness)

Demographic trends – population age structure (optional extension)

All data are aggregated to daily or weekly frequency to align with operational planning cycles.Data Sources

The project uses publicly available and simulated NHS-style datasets to reflect realistic operational conditions, including:

Hospital Episode Statistics (HES) – emergency admissions and length of stay

A&E Attendances and Emergency Admissions (NHS England)

Bed Availability and Occupancy Returns (KH03)

Calendar features – day of week, bank holidays, school holidays

Weather indicators – temperature, cold snaps (proxy for respiratory illness)

Demographic trends – population age structure (optional extension)

### Methodology
1. Exploratory Data Analysis (EDA)

Identified strong weekly and annual seasonality, with pronounced winter peaks

Detected structural breaks linked to policy changes and pandemic effects

Assessed missing data patterns and reporting artefacts

2. Feature Engineering

Lagged demand variables (e.g. 7-day, 14-day, 28-day lags)

Rolling averages and volatility measures

Holiday and extreme weather indicators

Trend and seasonality decomposition features

3. Modelling Approaches

A comparative modelling strategy was adopted:

Baseline statistical models

Seasonal Naïve

SARIMA / SARIMAX

Machine learning models

Gradient Boosting (XGBoost / LightGBM)

Random Forests for non-linear effects

Time-series ML hybrids

ML models with explicit lag and seasonality features

Models were evaluated using rolling-origin cross-validation to reflect real-world forecasting conditions.


