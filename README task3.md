# Task 3: Energy Consumption Time Series Forecasting

## Objective
Forecast short-term household energy usage using historical time-based patterns and compare multiple forecasting models.

## Dataset Information
- **Source**: Household Power Consumption Dataset (simulated)
- **Time Range**: January 1, 2022 - December 31, 2023 (2 years)
- **Frequency**: Daily data
- **Features**: Global active power, reactive power, voltage, sub-metering, temperature
- **Target**: Global_active_power (energy consumption in kW)

## My Approach

### 1. Data Preprocessing & Feature Engineering

**Time-based features created:**
- Year, Month, Day, DayOfWeek, Quarter, WeekOfYear
- IsWeekend (binary flag for weekend days)

**Lag features (previous days):**
- Lag_1, Lag_2, Lag_3, Lag_7, Lag_14

**Rolling window features:**
- Rolling mean (3, 7, 14 days)
- Rolling standard deviation (3, 7, 14 days)

### 2. Exploratory