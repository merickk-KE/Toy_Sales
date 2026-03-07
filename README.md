# Toy_Sales
This dataset is obtained from Kaggle.

## 1. Overview


Before conducting any analysis, the data requires cleaning and preprocessing to ensure accuracy, consistency, and usability. This focuses on handling missing values, correcting inconsistent categorical values, removing duplicates, and ensuring appropriate data types.


## 2. Initial Data Quality Assessment

An initial exploration is performed to understand the structure and quality of the dataset. This included:
Inspecting the shape of the dataset and column data types


Reviewing summary statistics using descriptive methods


Checking for missing values and duplicate records


Identifying inconsistent representations in categorical variables (e.g., “Yes”, “yes”, “TRUE”, “Y”)


Key issues identified:

Presence of missing values in several columns


Inconsistent labeling in boolean/categorical fields


Duplicate records across key identifiers


Some columns stored as incorrect data types.


## 3. Handling Missing Values

Missing values are assessed both in terms of frequency and potential impact on the analysis. Depending on the column and its relevance:
Columns with a small number of missing values were imputed using appropriate strategies.

For categorical indicators, missing values were preserved as NaN to avoid introducing bias.

This is to ensure that the dataset remained as informative as possible without distorting the underlying distributions.


## 4. Standardizing Categorical Values

Several categorical columns contained inconsistent labels representing the same concept (e.g., “Yes”, “yes”, “Y”, “TRUE”). These values were standardized into consistent categories to improve interpretability and enable accurate grouping and aggregation.
For example:
All affirmative responses were mapped to "Yes"

All negative responses were mapped to "No"

This step significantly reduced noise in categorical features and improved downstream analysis.


## 5. Data Type Corrections

Several columns were cast to appropriate data types to ensure correct analytical behavior:
The ‘transaction_date’ columns were converted to datetime format.

Categorical columns were cast to category/object types where appropriate


## 6. Outlier & Consistency Checks

Basic outlier detection and consistency checks were performed on numerical variables to identify unrealistic or invalid values (e.g., negative quantities, extreme transaction values).

Outliers were reviewed and retained or removed based on relevance to avoid discarding valid but extreme observations.


## 7. Final Cleaned Dataset

After cleaning:
The dataset had consistent categorical labels

No duplicate records remained

Missing values were handled appropriately

All columns had correct data types.
