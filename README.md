**Traffic Fines Comparative Analysis**

### Introduction

This project aims to conduct a comparative study between traffic fines data from the most recent full year and available records from 2020. The analysis includes the visualization of top locations with the highest fines, identification of common traffic violations, analysis of speed-related data, and comparison of monthly fines between the two years.

### Combining Data

The data from twelve separate CSV files covering the months of two specified years (2020 and 2022) is combined into a single DataFrame using the `combine_csv_files` function. The resulting DataFrame is explored to understand its dimensions.

### Data Cleaning

To ensure consistency and ease of analysis, unnecessary geographic columns (`COORDENADA-X` and `COORDENADA-Y`) are dropped using the `drop_coors` function. Additionally, the `ANIO` (year) and `DESCUENTO` (discount) columns are identified as constants and removed.

### Exploring Unique Values

The unique values of each variable are examined, revealing that `ANIO` and `DESCUENTO` have only one unique value throughout the dataset. Further investigation into the `DESCUENTO` column in 2022 shows an outlier.

### Handling Anomalies

Anomalies in the `VEL_LIMITE` and `VEL_CIRCULA` columns are addressed by replacing empty values with None using regular expressions. The columns are then converted to numeric type, and null values are filled with 0.

### Speed Limits Analysis

The most common speed limit (excluding zero) is identified and visualized. A new column, `DIFFERENCE_KMH`, is created to calculate the difference between the driver's speed and the speed limit. The top 10 drivers who exceeded speed limits by the highest margins are identified.

### Points Deduction Analysis

The DataFrame is filtered for complaints resulting in point deductions (excluding zero points), and the public agent with the highest average points deduction is identified.

### Infractions by Hour

The decimal part of the hours column is removed, and the number of infractions for each hour is graphically represented. Peak hours with the most infractions are identified.

### Comparative Study

The fines issued during the months of the most recent full year (2022) are graphically displayed and compared with 2020. The percentage change in fines issued is calculated, providing insights into potential impacts of Spain's COVID-19 confinement on traffic infractions.

### Top Fines Visualization

The top 20 locations with the highest traffic fines for 2020, 2021, and 2022 are visualized in three separate subplots. Common locations across all three years are identified.

### Additional Analysis: Common Violations

A deeper analysis is conducted to identify and visualize the most common types of traffic violations in prominent locations. This includes data from the top fines locations for each year (2020, 2021, 2022).

### Conclusion

 Provides an overview of the steps taken in the comparative analysis of traffic fines data. The visualizations and analyses conducted offer valuable insights into patterns, anomalies, and trends in traffic violations over the specified years. The code is organized, documented, and can be easily extended for further exploration or adapted for similar analyses.