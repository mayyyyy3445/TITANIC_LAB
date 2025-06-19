# TITANIC_LAB

Question 1: Loading and Handling Data
Purpose: You loaded the Titanic dataset (titanic.csv) into a DataFrame using pandas to explore its structure.
Key actions:
Used .head() to preview the first few rows of the dataset.
Used .info() to understand the data types and which columns have missing values.
Used .describe() to get summary statistics (mean, std, min, max, etc.) for numerical columns.
Used .isnull().sum() to count how many missing values each column has.

Question 2: Identifying Missing Data
You used df.isnull().sum() to identify which columns have missing data.
Insight: Now that you know where the missing values are, you can choose to:
Drop those rows (e.g., if too few)
Fill them using a method (like the mean, median, or a constant)
For Cabin, since most of the values are missing, you might drop this column entirely.

Question 3: Determining Survival Rate
Calculation:
df["Survived"].mean() gives the proportion of survivors (because Survived is 1 for survived, 0 for not).
Output: 0.3838 → 38.38% of the passengers survived.
Visualization:
You plotted a bar chart showing:
Number of survivors (green)
Number of non-survivors (red)

Question 4: Analyzing Survival by Age
Result: The average age of survivors was about 28.34 years.

Activity 2:

1. Loading the Dataset
You started by importing necessary libraries and loading titanic.csv:

import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("titanic.csv")
Then, you previewed the dataset using .head() and explored structure with .info() and .describe().

2. Understanding the Dataset
What you discovered:

891 rows, 12 columns
Data types: Mix of numerical (Age, Fare, etc.) and categorical (Sex, Embarked)
Missing values:
Age: 177 missing
Cabin: 687 missing (most of it)
Embarked: 2 missing

3. Handling Missing Data
You applied standard data-cleaning practices:

Column	Action Taken
Age	Filled missing values with median
Cabin	Dropped (too many missing values)
Embarked	Filled with most common value (mode)

4. No duplicates were found, which means your dataset was already clean in that aspect.


5. Renamed all columns to lowercase for consistency.
Saved the cleaned dataset as titanic_cleaned.csv.

6. Most passengers were aged 20–40 years, helping understand the ship’s demographics.



