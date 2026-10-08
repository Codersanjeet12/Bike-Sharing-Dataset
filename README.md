# Bike-Sharing-Dataset
# Bike Sharing Dataset Analysis  This repository contains an hourly bike rental dataset with features such as: - Date, season, year, month, hour - Weather situation, temperature, humidity, windspeed - User counts (casual, registered, total)  📊 Purpose: The dataset can be used for: - Data cleaning and preprocessing.
# 🚲 Bike Sharing Dataset Analysis

## 📌 Overview
This repository contains an **hourly bike rental dataset** with features such as:
- Date, season, year, month, hour
- Weather situation, temperature, humidity, windspeed
- User counts (casual, registered, total)

The dataset is ideal for **data cleaning, exploratory data analysis (EDA), visualization, and predictive modeling**.

---

## 🎯 Objectives
- Analyze rental trends across seasons, weekdays, and hours.
- Study the impact of weather conditions on bike demand.
- Build forecasting models to predict future rentals.

---

## 📊 Dataset Features
| Column       | Description |
|--------------|-------------|
| dteday       | Date of record |
| season       | Season (1: Spring, 2: Summer, 3: Fall, 4: Winter) |
| yr           | Year (0: 2011, 1: 2012) |
| mnth         | Month (1–12) |
| hr           | Hour of the day (0–23) |
| holiday      | Holiday indicator |
| weekday      | Day of the week |
| weathersit   | Weather situation (1: Clear, 2: Mist, 3: Light Snow/Rain, 4: Heavy Rain) |
| temp         | Normalized temperature |
| atemp        | Normalized feeling temperature |
| hum          | Humidity |
| windspeed    | Wind speed |
| casual       | Count of casual users |
| registered   | Count of registered users |
| cnt          | Total rentals (casual + registered) |

---

## ⚡ Example Usage

### Python (Pandas + Matplotlib)
```python
import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
df = pd.read_csv("dataset_3.csv")

# Rentals by hour
hourly = df.groupby("hr")["cnt"].mean()
plt.plot(hourly.index, hourly.values)
plt.title("Average Rentals by Hour")
plt.xlabel("Hour of Day")
plt.ylabel("Average Rentals")
plt.show()
