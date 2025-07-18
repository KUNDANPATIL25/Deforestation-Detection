1. Installed and Imported Libraries
I started by installing and importing the necessary Python libraries. These included:

numpy and pandas for handling and analyzing data

matplotlib and seaborn for creating visualizations

scikit-learn for machine learning models and preprocessing

xgboost for using the XGBoost classifier

folium was listed for map-based visualizations (though not yet used)

These libraries provided the basic tools needed for data analysis, visualization, and building classification models.

2. Loaded Datasets
I loaded three CSV files:

modis_2021_India.csv

modis_2022_India.csv

modis_2023_India.csv

Each file was loaded into its own dataframe (df1, df2, df3). These files contain fire detection data from different years.

3. Displayed Sample Data
After loading the files, I printed the first few rows of each dataframe using head(), and also viewed the last few rows of df1 using tail(). This helped me check that the files were loaded correctly and that the data looked clean.

4. Combined All Years into One Dataset
I merged the three dataframes (df1, df2, and df3) into one single dataframe called df using the concat() function. This allowed me to work with all three years of data together.

I then printed the first few rows of the combined dataset to confirm that the merge was successful.

5. Checked Dataset Size and Structure
I used:

shape to see the number of rows and columns

info() to check data types and memory usage

isnull().sum() to check for missing values

duplicated().sum() to check for duplicate rows

columns to see all column names

describe().T to view summary statistics like mean, min, max, etc.

These steps helped me understand what kind of data I was dealing with and whether there were any issues to fix.

6. Checked Class Distribution of Target Column
I used value_counts() on the type column to see how many records belong to each fire type. I noticed that:

Most of the data was labeled as "MODIS"

Fewer records were labeled as "VIIRS"

This showed that the target classes were imbalanced, which is something I may need to address during model training.

7. Explored Categorical Data
For every column that had text (categorical data), I printed:

The name of the column

All unique values in that column

The number of unique values

This helped me understand how many categories each feature had, and whether any columns needed encoding.

8. Created Visualizations
a. Count Plot for Fire Type
I created a bar chart showing the number of occurrences of each fire type using Seaborn's countplot(). This confirmed that:

"MODIS" was much more common than "VIIRS"

The dataset is imbalanced

b. Histogram for Confidence Values
I created a histogram showing how confidence scores are distributed in the data. From this, I observed that:

There are two main groups: low confidence and high confidence

Very few records have medium confidence values

This helped me understand how reliable the fire detection data is.