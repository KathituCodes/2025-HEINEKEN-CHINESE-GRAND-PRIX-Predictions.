# 2025 Heineken Chinese Grand Prix – Prediction Model

## Project Overview

This project aims to **predict the finishing order** of the 2025 Heineken Chinese Grand Prix using historical race data, qualifying results, and machine learning.

By leveraging **FastF1** for race data and **Gradient Boosting Regression** for predictions, the model attempts to estimate race lap times and standings based on driver performance trends from previous seasons.

---

## Objectives

The primary goals of this project were to:

1. **Collect and process historical Formula 1 data** – Load 2024 Chinese Grand Prix results, lap times, and tire data.
2. **Integrate 2025 qualifying results** – Map driver qualifying performance into a structured dataset.
3. **Engineer predictive features** – Convert lap times to seconds, align driver codes, and merge qualifying + historical race datasets.
4. **Train a machine learning model** – Use Gradient Boosting Regressor to predict lap times and derive expected finishing positions.
5. **Evaluate model accuracy** – Assess the prediction using **Mean Absolute Error (MAE)**.
6. **Generate 2025 race predictions** – Produce an estimated race order for the Chinese GP.

---

## Data Sources

* **FastF1 API** – Historical race telemetry, lap times, and session results.
* **2025 Qualifying Data** – Manually compiled grid positions and qualifying times.
* **Past Race Performance** – 2024 Chinese Grand Prix race results.

---

## Methodology

1. **Load Historical Race Data**
   Extracted lap-by-lap data from the 2024 Chinese GP, including tire compounds and grid positions.

2. **Prepare 2025 Qualifying Data**
   Created a dataframe for drivers, lap times, and starting grid, mapping names to 3-letter driver codes.

3. **Merge & Preprocess Data**
   Combined 2025 qualifying with 2024 race data for model training.

4. **Train the Model**

   * Features: Qualifying time, grid position
   * Target: Average lap time
   * Algorithm: `GradientBoostingRegressor`
   * Train/test split to validate predictions.

5. **Predict 2025 Results**
   Generated expected lap times and ranked drivers accordingly.

---

## Model Performance

The model’s predictive accuracy was measured using **Mean Absolute Error (MAE)** to ensure reasonable lap time estimations.

---

## Future Improvements

* Incorporating **weather data** for race day conditions.
* Adding **pit stop strategies** and tire degradation modeling.
* Using **multi-season data** for stronger driver performance trends.

---

## Requirements

```bash
pip install fastf1 pandas numpy scikit-learn
```

---

## Disclaimer

This model is a **fun, data-driven prediction tool** and not an official forecast. Race outcomes can vary due to unpredictable factors like crashes, mechanical issues, or strategy changes.

