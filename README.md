# Weather Dataset Analysis Project

This project demonstrates the analysis of a weather dataset using Python's pandas library. The dataset is a time-series record of per-hour weather conditions, including Temperature, Dew Point Temperature, Relative Humidity, Wind Speed, Visibility, Pressure, and Weather Conditions.

## Table of Contents
- [Dataset Description](#dataset-description)
- [Requirements](#requirements)
- [Usage](#usage)
- [Features](#features)
- [Analysis Steps](#analysis-steps)
- [Results](#results)
- [Author](#author)

## Dataset Description
The dataset contains hourly weather observations at a specific location. Key columns include:
- `Temperature`
- `Dew Point Temperature`
- `Relative Humidity`
- `Wind Speed_km/h`
- `Visibility_km`
- `Pressure`
- `Weather`

## Requirements
To run the analysis, you need:
- Python 3.7+
- Required libraries:
  - pandas
  - numpy (optional for further calculations)
  - matplotlib (optional for visualizations)

Install dependencies with:
```bash
pip install pandas matplotlib
```

## Usage
1. Load the dataset from the provided CSV file:
   ```python
   import pandas as pd
   data = pd.read_csv("path/to/your/dataset.csv")
   ```
2. Perform exploratory data analysis (EDA) using the provided code snippets.

## Features
The script includes the following analyses:

1. **Basic Data Exploration**:
   - View the first few rows: `data.head()`
   - Get dataset dimensions: `data.shape`
   - Check column names: `data.columns`
   - Identify data types: `data.dtypes`

2. **Unique Value Analysis**:
   - Identify unique values in columns: `data['Column'].unique()`
   - Count unique values: `data.nunique()`

3. **Data Cleaning**:
   - Check for null values: `data.isnull().sum()`
   - Replace or rename columns: `data.rename(columns={'Old Name': 'New Name'}, inplace=True)`

4. **Statistical Analysis**:
   - Mean: `data['Column'].mean()`
   - Standard deviation: `data['Column'].std()`
   - Variance: `data['Column'].var()`

5. **Filtering Data**:
   - Filter rows based on conditions:
     ```python
     data[data['Column'] == 'Value']
     ```
   - Combine conditions:
     ```python
     data[(data['Column1'] > value) & (data['Column2'] == value)]
     ```

6. **Grouping and Aggregation**:
   - Group data by column: `data.groupby('Column').mean()`
   - Find min/max values: `data.groupby('Column').min()` / `data.groupby('Column').max()`

7. **Special Queries**:
   - Find all instances when Weather is "Clear":
     ```python
     data[data['Weather'] == 'Clear']
     ```
   - Find instances with multiple conditions:
     ```python
     data[(data['Weather'] == 'Clear') | (data['Visibility_km'] > 40)]
     ```

## Analysis Steps
The following questions are answered in the analysis:
1. Find all unique `Wind Speed` values.
2. Count the number of times the `Weather` is "Clear".
3. Identify instances where `Wind Speed` is exactly 4 km/h.
4. Locate null values in the dataset.
5. Rename the `Weather` column to `Weather Condition`.
6. Calculate the mean visibility.
7. Determine the standard deviation of `Pressure`.
8. Compute the variance of `Relative Humidity`.
9. Find all records with "Snow" conditions.
10. Identify instances where `Wind Speed` > 24 km/h and `Visibility` = 25 km.
11. Calculate mean values for each column grouped by `Weather Condition`.
12. Determine minimum and maximum values for each column grouped by `Weather Condition`.
13. Display all records with `Weather Condition` as "Fog".
14. Find records where `Weather` is "Clear" or `Visibility` > 40 km.
15. Combine complex conditions for filtering.

## Results
The analysis provides insights such as:
- Unique weather conditions.
- Statistical summaries (mean, standard deviation, variance) for numerical columns.
- Filtering and grouping of data based on weather conditions and other metrics.

## Author
**Shreyash Sule**

For any queries or feedback, please contact: shreyashsule22@gmail.com

