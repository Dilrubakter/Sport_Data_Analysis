# Sport_Data_Analysis

**Project Overview**
This project involves analyzing the FIFA 2017 player dataset (FullData.csv) to gain insights into player attributes, focusing on physical performance metrics like speed and strength. The analysis is performed using Python in a Jupyter Notebook environment (assignment (2).ipynb). The notebook includes data loading, exploratory data analysis (EDA), and preprocessing steps suitable for machine learning tasks.

**Dataset**

**Source**: The dataset is sourced from Kaggle (/kaggle/input/complete-fifa-2017-player-dataset-global/FullData.csv).
**Description**: Contains detailed attributes of FIFA 2017 players, including nationality, club, physical stats (e.g., Speed, Strength), and skill metrics (e.g., Ball Control, Dribbling).
**Key Columns**:
Name, Nationality, Club, Club_Position, Club_Kit, Contract_Expiry, Rating, Age
Physical attributes: Speed, Strength
Skill attributes: Ball_Control, Dribbling, Marking, etc.
Goalkeeper attributes: GK_Positioning, GK_Diving, etc.



**Notebook Structure**
The Jupyter Notebook (assignment (2).ipynb) is organized as follows:

Importing Libraries:

Libraries used: pandas, numpy, matplotlib, seaborn, plotly, sklearn.
Purpose: Data manipulation, visualization, and preprocessing.


Reading the File:

Loads the dataset into a pandas DataFrame for analysis.


Exploratory Data Analysis (EDA):

Checks for null values to assess data quality.
Creates a Physical_Score metric, calculated as:Physical_Score = Speed * 0.6 + Strength * 0.4


Sorts players by Physical_Score to identify top physical performers.
Drops Speed and Strength columns after creating Physical_Score.


**Data Preprocessing**:

Handles missing values in National_Kit by filling with the mode.
Separates features into categorical and numerical types.
Applies StandardScaler to numerical features for normalization.
Uses LabelEncoder to encode categorical features (e.g., Nationality, Club) as numerical values.
Combines scaled numerical and encoded categorical data into a final DataFrame, ensuring all values are floats for machine learning compatibility.



**Requirements**
To run the notebook, ensure you have the following Python packages installed:
pip install pandas numpy matplotlib seaborn plotly scikit-learn

**Output**

The notebook produces a preprocessed DataFrame (final_df) with scaled numerical features and encoded categorical features, ready for machine learning tasks.
The top 15 rows of the preprocessed data are displayed for inspection.

**Notes**

The dataset contains missing values, particularly in National_Position and National_Kit (16,513 missing entries each). The preprocessing step currently fills National_Kit with the mode, but further handling of other missing values may be needed depending on the analysis.
The Physical_Score metric prioritizes speed (60%) over strength (40%), which can be adjusted based on analysis needs.
The notebook assumes the dataset is accessible at the specified Kaggle path. Update the path if running locally.

**Author**
This project was created by Dilruba Akter.
