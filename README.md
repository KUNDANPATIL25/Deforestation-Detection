🔥 Classification of Fire Types in India Using MODIS Satellite Data (2021–2023)
This project uses MODIS satellite data to classify different types of fires across India between 2021 and 2023. It involves data preprocessing, exploratory data analysis, and the use of machine learning models to classify fire types using confidence levels, satellite metadata, and spatial attributes.

📁 Dataset Description
We have used three datasets sourced from MODIS for the years:

modis_2021_India.csv

modis_2022_India.csv

modis_2023_India.csv

Each dataset includes fire incident records with attributes such as location (latitude, longitude), brightness, confidence level, date, time, and detection instrument.

⚙️ Libraries and Tools Used
pandas, numpy – Data handling and manipulation

matplotlib, seaborn – Data visualization

scikit-learn – Machine learning algorithms and preprocessing

xgboost – Gradient boosting classifier

folium – (Planned) map-based visualizations

📌 Project Steps
1. 📦 Installed and Imported Libraries
Essential libraries for data analysis, visualization, and machine learning were imported at the beginning.

2. 📂 Loaded and Merged Datasets
Loaded 3 datasets (2021–2023) individually into df1, df2, and df3.

Combined them using pd.concat() into a single DataFrame df.

3. 👁️‍🗨️ Viewed Sample Data
Used .head() and .tail() to verify data integrity.

Confirmed clean and structured format across files.

4. 🧮 Basic Data Checks
.shape, .info(), and .describe() were used to inspect structure and summary statistics.

Checked for:

Missing values

Duplicate entries

Data types and memory usage

5. 📊 Target Class Distribution
Used value_counts() on the type column to evaluate class imbalance.

Noted significant imbalance in fire type labels, indicating a need for resampling (e.g., SMOTE) later.

6. 🔤 Explored Categorical Variables
Printed unique values and counts for text-based columns like:

satellite (e.g., Terra, Aqua)

instrument (MODIS)

daynight (Day/Night)

7. 📈 Visual Analysis
a. Fire Type Count Plot
Used seaborn.countplot() to show the skew toward one dominant fire type.

b. Confidence Histogram
Visualized the distribution of confidence scores.

Found bimodal pattern with peaks in high and low confidence, few medium scores.

📌 Key Observations
The dataset is clean and comprehensive with no null or duplicate values.

A major class imbalance was observed in fire type distribution.

High and low confidence scores dominate, indicating stronger reliability at extremes.

📍 Future Work (Optional)
Incorporate folium for interactive fire mapping.

Apply SMOTE for class balancing.

Evaluate different ML classifiers (Logistic Regression, Random Forest, etc.).

Add model persistence using joblib.



✍️ Author
Kundan Sunil Patil
B.Tech Final Year Engineering Student.
MIT
