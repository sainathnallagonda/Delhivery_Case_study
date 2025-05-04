# Delhivery - Feature Engineering

## Project Overview
This project focuses on **feature engineering** for logistics data to optimize **route scheduling** and **trip time predictions**. The dataset contains trip details, including timestamps, distances, and scan times.

## Objectives
- **Clean and preprocess** logistics data.
- **Create meaningful features** for route optimization.
- **Analyze trip segments** to enhance predictive modeling.
- **Remove outliers** using visual analysis.

## Dataset
The dataset includes:
- **Trip UUID** (Unique trip identifiers)
- **Source and Destination Centers**
- **Trip Creation Time**
- **Distance and Time Metrics**
- **OSRM-based estimated time and distance**
- **Segment-wise journey details**

## Tools & Libraries Used
- **Python** (`pandas`, `numpy`, `matplotlib`, `seaborn`)
- **Feature Engineering** (`groupby`, `cumsum`, `datetime processing`)
- **Data Cleaning** (`dropna`, `reset_index`, `StandardScaler`)
- **Outlier Detection** (`IQR filtering`, `Box plots`)

## Methodology
1. **Data Cleaning**:
   - Removed null values.
   - Converted timestamps to `datetime` format for analysis.
2. **Feature Engineering**:
   - Created trip segments using `trip_uuid + source_center + destination_center`.
   - Computed cumulative segment time and distance.
   - Extracted **hour, month, day, weekday** features from trip timestamps.
   - Created **State, City, and Place mappings** for better regional analysis.
3. **Outlier Detection & Removal**:
   - Applied **Interquartile Range (IQR) filtering** to remove extreme trip values.
   - Used **Box plots** to visualize and refine filtered datasets.

## Key Findings
- **High variance in trip durations**, influenced by destination and route type.
- **Carting trips are more common** than Full Truck Load (FTL) trips.
- **Major delays occur due to specific regional factors**, requiring additional investigation.
- **Feature engineering significantly improves trip segmentation and route analysis**.

## Repository Contents
- `delhivery_feature_engineering.ipynb` – Jupyter notebook with full analysis.
- `delhivery_data.csv` – Dataset file.
- `README.md` – This file.

## Conclusion
Feature engineering enhances logistics data **interpretability** and **decision-making**. The project provides **valuable insights** for optimizing **route scheduling and trip efficiency**.
