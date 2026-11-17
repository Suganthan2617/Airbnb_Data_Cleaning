
# Real-World Dataset Cleaning and Preprocessing

## Project Overview

This project focuses on cleaning and preprocessing a real-world Airbnb listings dataset from Seattle, Washington.

The objective was to improve data quality by handling missing values, detecting outliers, checking duplicates, and encoding categorical variables using Python.

## Dataset Information

- Dataset: Inside Airbnb - Seattle Listings
- Original Rows: 7,657
- Original Columns: 19
- Cleaned Rows: 7,657
- Cleaned Columns: 41

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Data Cleaning Operations

### 1. Missing Value Handling
- Filled missing prices using the median.
- Filled missing minimum nights using the median.
- Replaced missing monthly review counts with 0.
- Replaced missing license values with "Not Provided".
- Retained missing review dates for listings with zero reviews.

### 2. Duplicate Detection
- Checked duplicate rows.
- Checked duplicate listing IDs.
- No duplicates were found.

### 3. Outlier Detection and Treatment
Used the Interquartile Range (IQR) method to detect and cap outliers in:
- Price
- Minimum Nights
- Reviews Per Month

### 4. Categorical Encoding
Applied One-Hot Encoding to:
- Room Type
- Neighbourhood Group

A total of 21 encoded columns were created.

### 5. Date Conversion
Converted the `last_review` column into a datetime data type.

## Before and After Comparison

| Metric | Before | After |
|---|---:|---:|
| Rows | 7,657 | 7,657 |
| Columns | 19 | 41 |
| Missing Values | 4,296 | 915 |
| Duplicate Rows | 0 | 0 |

## Project Files

- `Data_Cleaning.ipynb` - Complete data cleaning process and explanations.
- `raw_dataset.csv` - Original dataset (download separately from Inside Airbnb).
- `cleaned_dataset.csv` - Final cleaned dataset.

## How to Run

1. Clone this repository.
2. Install the required Python libraries:

   `pip install pandas numpy matplotlib seaborn jupyter`

3. Open `Data_Cleaning.ipynb` using Jupyter Notebook or VS Code.
4. Download the original Seattle listings dataset from Inside Airbnb and place it in the project folder as `raw_dataset.csv`.
5. Run all notebook cells.

## Conclusion

This project provided practical experience in real-world data cleaning and preprocessing. The final dataset is better prepared for further exploratory data analysis and machine learning applications.
