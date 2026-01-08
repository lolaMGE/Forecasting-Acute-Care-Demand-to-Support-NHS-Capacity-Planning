# Forecasting Emergency Admissions to Support Winter Staffing Decisions in an NHS Trust
This project is designed to forecast the healthcare demand of citizens to support operational planning and decision-making
### Project Overview

The NHS continually faces intense seasonal pressure in emergency admissions, especially during the winter season. This is driven by seasonal illnesses, demographic changes, workforce constraints,and system shocks. This surge places constraints on staffing levels, availability of beds and patient flow, which could lead to the risk of delays, overcrowding and compromised patient care. Accurate and explainable demand forecasting plays a critical role in supporting operational planning, enabling NHS managers and analysts to anticipate pressure points, plan staffing rotas, and support escalation discussions. Operational teams often need early, data-driven insight to inform rota planning and escalation decisions. However, forecasts must be simple, transparent, and explainable to be trusted and acted upon, because poor anticipation of demand can lead to understaffing, increased expenses spent on agency staff, staff burnout, and poorer patient outcomes.

### Objectives
This project aims to develop robust, interpretable forecasting of emergency admission to support short -term capacity and staffing planning during a period of increased demand.

This analysis is designed to support:

1. Operational managers

2. Workforce planners

3. Performance and information teams


The key objectives of the project are to:

a. Forecast acute care demand (e.g. emergency admissions, bed occupancy, A&E attendances) at hospital or Trust level.

b. Capture seasonal and structural patterns, including winter pressures, bank holidays, and long-term trends.

c. Quantify uncertainty to help planners understand best- and worst-case scenarios.

d. Evaluate model performance using appropriate time-series validation methods.

e. Translate forecasts into operational insights that can inform NHS capacity planning and policy decisions.


Using historical NHS activity data combined with calendar, weather, and population health indicators, the project delivers actionable insights for forecasts at daily and weekly horizons, with clear uncertainty bounds to support operational and strategic decision-making.




### Data Sources

The project uses publicly available and simulated NHS-style datasets to reflect realistic operational conditions, including:

1. Hospital Episode Statistics (HES) – emergency admissions and length of stay

2. A&E Attendances and Emergency Admissions (NHS England)

3. Bed Availability and Occupancy Returns (KH03)

4. Calendar features – day of week, bank holidays, school holidays

5. Weather indicators – temperature, cold snaps (proxy for respiratory illness)

Demographic trends – population age structure 

All data are aggregated to daily or weekly frequency to align with operational planning cycles.

### Methodology Overview

The analytical approach follows standard NHS analytics practice:

1. Exploratory analysis to understand trends, seasonality, and structural patterns

2. Feature engineering to capture calendar effects such as winter periods and bank holidays

3. Development of baseline and enhanced time-series forecasting models

4. Rolling or walk-forward validation to reflect real-world forecasting conditions

5. Evaluation using appropriate accuracy metrics and error analysis

Modelling choices are explicitly justified, with emphasis placed on robustness, interpretability, and suitability for operational use rather than model complexity.


### Methodology
##### Exploratory Data Analysis (EDA)

Identified strong weekly and annual seasonality, with pronounced winter peaks

Detected structural breaks linked to policy changes and pandemic effects

Assessed missing data patterns and reporting artefacts

##### Feature Engineering

Lagged demand variables (e.g. 7-day, 14-day, 28-day lags)

Rolling averages and volatility measures

Holiday and extreme weather indicators

Trend and seasonality decomposition features

##### Modelling Approaches

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

Uncertainty and Risk Considerations

Recognising the inherent uncertainty in healthcare demand, forecasts are accompanied by uncertainty estimates. These are intended to support:

Scenario planning

Risk-aware decision-making

Better understanding of forecast limitations

This reflects NHS best practice, where forecasts inform decisions but do not replace professional judgement.

##### Operational Interpretation

Rather than presenting forecasts in isolation, results are translated into operationally meaningful insights, such as:

Anticipated pressure periods

Relative changes compared to recent baselines

Implications for staffing, beds, and escalation planning

The focus is on supporting conversations and planning, not prescribing actions.

### Limitations

Key limitations of this project include:

Reliance on aggregated public data

Absence of real-time operational constraints

Simplified assumptions compared to live Trust systems

These limitations are discussed transparently, alongside suggestions for how the analysis could be extended using internal NHS data.




