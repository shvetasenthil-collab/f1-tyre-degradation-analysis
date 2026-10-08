# Formula 1 Tyre Degradation Analysis 

A Python data analysis project investigating tyre degradation using real
Formula 1 race data from the FastF1 library.

The main analysis focuses on Max Verstappen's performance during the
2025 Japanese Grand Prix and investigates how tyre age affects lap time.

## Project Overview

Tyre degradation is an important factor in Formula 1 race strategy. However,
lap times are influenced by several factors beyond tyre age, including fuel
load, tyre compound and changing track conditions.

This project explores these effects using Formula 1 lap data and regression
analysis.

The analysis:
- Explores lap and tyre data using FastF1
- Cleans race data and removes pit-in and pit-out laps
- Visualises lap times across different tyre compounds
- Uses simple linear regression to investigate tyre degradation
- Identifies the effect of confounding variables on the initial model
- Uses multiple regression to account for race progression and tyre compound

## Key Findings

The initial simple regression produced a tyre-age coefficient of
-0.0284 seconds per lap, suggesting lap times became faster as the tyres
aged.

This counterintuitive result highlighted the effect of race progression,
particularly decreasing fuel load.

After including race lap number and tyre compound in a multiple regression
model, the tyre-age coefficient became **+0.0271 seconds per lap**.

This suggests that, after accounting for the variables included in the model,
increasing tyre age was associated with slower lap times.

## Technologies Used

- Python
- FastF1
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

## Limitations

The analysis considers one driver and one race, so the estimated coefficients
should not be interpreted as universal tyre-degradation rates.

Factors such as traffic, fuel load, track evolution and driver behaviour may
also influence lap times.
