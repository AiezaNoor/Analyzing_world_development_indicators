# Analyzing_world_development_indicators
**World Development Indicators Analysis: Policy Impact Detection and Forecasting**

**Project Overview**

This project analyzes the relationship between policy changes and development indicators using World Bank data from 1960-2024. We employ advanced time series models to detect policy impacts and predict future trends in key economic and social indicators across 31 countries.

**Key Features**

- Dataset: Uses World Development Indicators dataset with:

31 countries (developed and developing)

20 key indicators (GDP growth, population metrics, life expectancy, etc.)

Annual data from 1960-2024

**Methodology:**

- Change-point detection to identify significant policy impacts

- LSTM and TCN models for time series forecasting

- Comprehensive data preprocessing pipeline

**Visualizations:**

- Interactive trend analysis

- Change-point detection plots

- Model performance comparisons
**Key Results**
**Change-Point Detection:**

- Identified significant policy impacts across countries
- Zimbabwe showed most frequent changes (10 change points)
- Common change years: 1971, 2001, 2021

**Model Performance:**
- LSTM (India GDP per capita):
- R²: 0.93
- MSE: 8586.20
- Forecasted 2025 GDP: $2619.46
**TCN (US GDP growth):**
- Initial R²: -0.044 (needs improvement)
- Training time: ~5 seconds
  
**Methodology**
  
**Data Collection & Preprocessing:**

- Handled missing values (dropped indicators with >60% missing)
- Standardized formats across 60+ years
- Reshaped for time series analysis

**Change-Point Detection:**
- Used PELT algorithm with RBF cost function
- Identified structural breaks in economic trends
- Created binary labels for model training

**Model Development:**
- LSTM: For capturing long-term dependencies
- TCN: For parallel processing of long sequences
- Train/Test split: 1960-2010 / 2011-2024

**Challenges Addressed**
- Handling sparse historical data (1960s-1980s)
-Accounting for delayed policy impacts (5-10 year lags)
- Developing proxy variables for policy changes
- Model tuning for small dataset sizes

**Dependencies**
- Python 3.8+
- Libraries: pandas, numpy, matplotlib, ruptures, tensorflow, keras-tcn
- Visualization: seaborn, plotly

**Future Work**
- Incorporate external policy databases
- Develop multi-country forecasting models
- Create policy impact simulation dashboard
- Expand indicator coverage (education, health outcomes)

Team
- Kashaf Sajjad (124-8032)
- Aieza Noor (124-8021)
- Aqdas Bibi (124-8048)
- Muhammad Shahbaz (124-8029)

**Acknowledgments**

- Dr. Muhammad Ishtiaq (Course Instructor)
- World Bank Open Data
- Ruptures and Keras-TCN library maintainers
