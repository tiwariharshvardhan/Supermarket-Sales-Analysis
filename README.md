# Supermarket Sales Analysis

## 1. Project Overview

This project involves the analysis of sales data from a supermarket chain in Tamil Nadu, covering the period from 2015 to 2018. The primary objective is to perform Exploratory Data Analysis (EDA) to identify sales patterns, track profit metrics, and uncover key insights.

The analysis focuses on determining the most profitable regions, product categories, and time periods, and observing sales trends over the four-year span. The main analysis is conducted in a Jupyter Notebook, with the final results and key metrics visualized in a Power BI dashboard.

---

## 2. Datasets Used

* **`supermart Grocery Sales Dataset.csv`**: The original, raw dataset containing 9,994 transaction records before cleaning.
* **`supermarket_dataset_cleaned.csv`**: The cleaned dataset, generated from the Jupyter Notebook, used for the analysis and visualizations.

---

## 3. Tools and Libraries

* **Python 3**
    * **Pandas**: For data loading, manipulation, and cleaning.
    * **NumPy**: For numerical operations.
    * **Matplotlib & Seaborn**: For data visualization within the notebook.
* **Microsoft Power BI**: For creating the final interactive dashboard.

---

## 4. Methodology

The analysis was performed in the `Supermarket Sales Analysis.ipynb` notebook and followed these steps:

### 4.1. Data Cleaning and Preparation

1.  **Loading Data**: The raw `supermart Grocery Sales Dataset.csv` was loaded into a Pandas DataFrame.
2.  **Handling Missing Data**: The dataset was checked for null values; none were found.
3.  **Handling Duplicates**: The dataset was checked for duplicate rows; none were found.
4.  **Dropping Irrelevant Columns**:
    * `Order ID` was dropped as it is a unique identifier not needed for analysis.
    * `State` was dropped as it contained only one unique value ("Tamil Nadu") and provided no analytical value.
5.  **Correcting Data Types**: The `Order Date` column was converted from an object to a datetime format to enable time-series analysis.
6.  **Filtering Outliers**: The 'North' region was removed from the dataset as it contained only one entry, allowing the analysis to focus on the four main regions (West, East, Central, and South).

### 4.2. Feature Engineering

* **Time-based Features**: `Order Month` and `Order Year` were extracted from the `Order Date` column to analyze sales and profit based on seasonality and annual trends.

### 4.3. Exploratory Data Analysis (EDA)

Visualizations were created to analyze the relationships between sales, profit, and various categories:
* Profit by Region
* Profit by Product Category and Sub Category
* Profit by Month
* Sales by Year

---

## 5. Key Findings

The analysis of the data from 2015-2018 revealed several key insights:

* **Annual Growth**: The supermarket has demonstrated consistent growth, with **total sales increasing every year** from 2015 to 2018.
* **Top Region**: The **West** region is the most profitable and generates the highest sales volume, accounting for 4.80M (32.09%) of total sales.
* **Profitable Categories**: The top 3 most profitable product categories are **Snacks**, **Eggs, Meat & Fish**, and **Beverages**.
* **Profitable Sub-Categories**: The most significant drivers of profit are **Health Drinks**, **Cookies**, and **Edible Oil & Ghee**.
* **Seasonal Trends**: Profitability peaks during the festive months of **September, November, and December**.

---

## 6. Project Files

* **`Supermarket Sales Analysis.ipynb`**: The main Jupyter Notebook detailing all data cleaning, analysis, and visualization steps.
    * **Note**: *The raw `.ipynb` file contains saved cell outputs, including plots that are stored as long base64-encoded text strings. This is normal for notebooks but can make the file difficult to read in a standard text editor. It is best viewed using Jupyter, VS Code, or another notebook-compatible application.*
* **`Supermarket Sales Analysis.pbix`**: The Microsoft Power BI workbook containing the final interactive dashboard.
* **`Supermarket Sales Analysis.pdf`**: A PDF export of the final Power BI dashboard, showcasing key metrics and visuals.
* **`supermart Grocery Sales Dataset.csv`**: The original, raw data.
* **`supermarket_dataset_cleaned.csv`**: The final, cleaned data used for the analysis.
