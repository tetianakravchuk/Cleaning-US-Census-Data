Cleaning US Census Data

Introduction

As a Data Analyst at the Census Bureau, my task is to clean, analyze, and visualize census data efficiently. This project demonstrates the power of Python and pandas in automating tedious tasks like handling CSV files, cleaning messy data, and creating insightful visualizations.

The dataset consists of multiple CSV files containing state-level demographic data. My goal is to clean the data, create scatterplots, histograms, and other visualizations.

Project Steps

1. Inspect the Data

	•	Combine all the CSV files using glob and load them into a single pandas DataFrame called us_census.
	•	Inspect the data types and columns using .head(), .columns, and .dtypes.
	•	Plan to clean the data for numerical manipulation.

2. Data Cleaning

Cleaning Steps:

	1.	Handle Income Column:
	•	Remove $ signs and convert the column to numeric.
	2.	Split GenderPop Column:
	•	Separate Men and Women into two columns and convert them to numeric by removing M and F.
	3.	Handle Missing Values:
	•	Fill NaN values in Women using TotalPop - Men.
	4.	Remove Duplicates:
	•	Use .duplicated() and .drop_duplicates() to ensure data integrity.
	5.	Clean Race Data:
	•	Remove % signs from race-related columns and convert them to numeric.
	•	Fill missing values with zeros or an appropriate default.

3. Visualizations

Scatterplots

	1.	Women vs Income:
	•	Visualize the relationship between the women population and average income in each state.

plt.scatter(df['Women'], df['Income'])
plt.title('Scatter Plot: Women vs Income')
plt.xlabel('Women Population')
plt.ylabel('Income')
plt.show()



Histograms

	•	Generate histograms for race-related data (e.g., White, Black, Asian, Hispanic) to visualize distributions.

Advanced Visualizations

	1.	Bar Plot:
	•	Show the top 10 states by total population.
	2.	Pie Chart:
	•	Display racial demographics for a specific state.
	3.	Line Chart:
	•	Plot trends in income vs women population.
	4.	Stacked Bar Plot:
	•	Compare racial distributions across the top 5 most populous states.
	5.	Heatmap:
	•	Highlight correlations between numerical columns using seaborn.

Key Learnings

	1.	Data Cleaning:
	•	Remove non-numeric characters (e.g., $, %).
	•	Handle missing values with logical assumptions.
	•	Ensure consistent data types for numerical analysis.
	2.	Visualization:
	•	Create meaningful plots to convey insights clearly.
	•	Use advanced visualizations (e.g., stacked bar plots, heatmaps) for deeper analysis.
	3.	Efficiency:
	•	Automate repetitive tasks (e.g., cleaning and merging data) using Python.
	•	Eliminate the manual effort of working with CSV files and Excel.

Tools Used

	•	Python: Core programming language.
	•	pandas: For data manipulation and cleaning.
	•	matplotlib: For visualizations.
	•	seaborn: For advanced plots (e.g., heatmaps).
	•	glob: To handle multiple CSV files.

Run the Project

	1.	Clone the repository and place your CSV files in the project directory.
	2.	Install the necessary libraries:

pip install pandas matplotlib seaborn


	3.	Run the script:

python us_census_analysis.py

Results

This project showcases:
	•	Cleaned and organized census data.
	•	Scatterplots, histograms, and advanced visualizations.
	•	The scalability and repeatability of Python over manual methods.