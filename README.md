# DA---Project-
Exploratory Data Analysis on Adult Income Dataset

Project Overview

This project is a beginner-friendly Exploratory Data Analysis (EDA) project using Python and Pandas.

The main purpose of this project is to understand the Adult Income dataset, clean the data, perform basic statistical analysis, identify outliers, and create different visualizations.

I worked with the dataset step by step, starting from loading and understanding the data and then moving towards data cleaning, analysis, and visualization.

Dataset

The project uses an adult.csv dataset containing information about people such as:

Age

Workclass

Final Weight

Education

Education Number

Marital Status

Occupation

Relationship

Race

Gender

Capital Gain

Capital Loss

Hours per Week

Native Country

Income

The dataset contains 32,561 rows and 15 columns.

Objectives

The main objectives of this project are:

Understand the structure of the dataset

Select and filter required columns and rows

Calculate basic statistical measures

Understand income and education categories

Identify missing/null values

Handle missing values

Find and remove duplicate records

Clean inconsistent text values

Detect and handle outliers

Understand relationships between numerical columns

Create different charts for better data understanding

Use AutoViz for automated exploratory visualization

Tools and Technologies

Python

Pandas

NumPy

Matplotlib

SciPy

AutoViz

Jupyter Notebook / Google Colab

EDA Process

1. Loading the Dataset

The dataset is loaded using Pandas:

import pandas as pd

df = pd.read_csv("adult.csv")

After loading the data, the first and last records were checked using head() and tail().

2. Data Selection and Filtering

Different Pandas techniques were used to work with the required data:

Selecting individual columns

Selecting multiple columns

Selecting rows using indexing

Filtering people based on age

Filtering based on income

Combining multiple conditions

Using isin() for multiple category filtering

Examples include filtering people with age greater than 50 and selecting people whose education is Bachelors or Masters.

3. Statistical Analysis

Basic statistical analysis was performed on the dataset.

The project calculates:

Mean

Median

Minimum

Maximum

Standard deviation

Count

Correlation

Mode

The describe()/aggregation approach was also used to understand numerical columns.

Some specific analysis questions covered in the notebook include:

Average, minimum, and maximum age

Standard deviation of age and hours per week

Number and frequency of education categories

Number of people in each income category

Percentage of people in each income category

Average working hours for a selected income category

Average age of people with Bachelors education

Most common education and occupation

Data Cleaning

Data cleaning was an important part of this project.

Missing Values

The dataset was checked for missing values and placeholder ? values.

Missing values were handled using approaches such as:

Filling missing values with a constant value

Dropping rows with missing values

Backward filling for selected columns

For example:

df = df.replace(" ?", None)
df = df.fillna("unknown")

The notebook also checks the number of null values before and after cleaning.

Duplicate Records

Duplicate rows were identified using:

df.duplicated()

The number of duplicate records was also checked and duplicate rows were removed using:

df.drop_duplicates(inplace=True)

Data Consistency

Text columns were cleaned using strip() and title() to make category values more consistent.

Columns cleaned include:

Workclass

Education

Marital Status

Occupation

Relationship

Race

Gender

Outlier Detection

Outliers were explored using different methods.

IQR Method

The Interquartile Range (IQR) method was applied to columns such as Age and EducationNum.

For Age, the notebook calculated:

Q1 = 28

Q3 = 48

IQR = 20

Lower Bound = -2

Upper Bound = 78

The notebook identified 142 IQR outliers for Age.

Z-Score Method

The Z-score method was also used to identify unusual values.

For Age, the notebook identified 120 observations using the absolute Z-score > 3 condition.

Trimming and Winsorization

The project also demonstrates:

Z-score trimming

Winsorization

These techniques were used to show different ways of handling outliers.

A similar outlier analysis was performed on EducationNum.

Data Visualization

Different visualization techniques were explored using Matplotlib.

Box Plot

Box plots were created to examine:

Education Number

Age

Hours per Week

Bar Plot

A bar plot was created using marital status and age.

Scatter Plot

Scatter plots were created to explore:

Age vs Hours per Week

Education Number vs Hours per Week

AutoViz

AutoViz was also used to automatically generate visualizations from the dataset.

The notebook used Income as the dependent variable for automated visualization.

Project Workflow

Load Dataset
     ↓
Understand Dataset
     ↓
Select & Filter Data
     ↓
Perform Statistical Analysis
     ↓
Identify Missing Values
     ↓
Clean Missing Values
     ↓
Remove Duplicates
     ↓
Clean Inconsistent Values
     ↓
Detect Outliers
     ↓
Handle Outliers
     ↓
Create Visualizations
     ↓
Understand the Data

Files in this Project

EDA-Project/
│
├── EDA_project1.ipynb
├── adult.csv
└── README.md

How to Run the Project

1. Clone or download this repository

2. Keep the files in the same folder

Make sure adult.csv and EDA_project1.ipynb are available in the project folder.

3. Open the notebook

You can open EDA_project1.ipynb using:

Jupyter Notebook

JupyterLab

Google Colab

VS Code with Jupyter support

4. Run the cells

Run the notebook cells from top to bottom to reproduce the analysis.

What I Learned

Through this project, I practiced:

Working with Pandas DataFrames

Selecting and filtering data

Using statistical functions

Handling missing values

Removing duplicate records

Cleaning inconsistent categorical data

Detecting outliers using IQR and Z-score

Applying trimming and winsorization

Creating charts using Matplotlib

Using AutoViz for automated visualization

Understanding the basic workflow of an EDA project

Conclusion

This project helped me understand the complete basic workflow of Exploratory Data Analysis. Instead of directly creating charts, I first worked on understanding the dataset, cleaning the data, checking statistical information, identifying unusual values, and then visualizing different aspects of the data.

The project gave me practical experience with Python, Pandas, data cleaning, statistical analysis, outlier detection, and data visualization.

Author

Harshavardhini

This project was created as part of my practice in Python and Data Analytics.
