# U.S. Grocery and Gas Price Analysis (2015–2026)

A collaborative data analytics project completed as part of the **NPower Canada Data Analytics Training Program**. This project explores how grocery and energy prices in the United States have changed over time, identifies the categories experiencing the largest price increases, and compares consumer price trends with general inflation.

## Project Overview

How have U.S. grocery and energy prices changed between January 2015 and July 2026, and which categories have experienced the greatest increases?

This project analyzes monthly average U.S. retail prices for 55 grocery and energy products. Using Python, Pandas, data cleaning techniques, exploratory data analysis, and interactive visualizations, we investigate long-term price trends, category-level changes, and differences between individual products.

An interactive dashboard was also developed using Dash to explore price movements and compare them with the Consumer Price Index (CPI).

## Dataset

**Dataset Name:** US Grocery and Gas Prices (2015–2026)

**Dataset Source:** Kaggle

**Original Data Source:** U.S. Bureau of Labor Statistics (BLS), Average Price Data Program.

**Kaggle Dataset:**  
https://www.kaggle.com/datasets/harshitsama/us-grocery-and-gas-prices-2015-2026

**Original Dataset File:** `us_average_prices_wide.csv`

**Data Period:** January 2015 – July 2026

**Original Dataset Dimensions:** 139 rows × 75 columns (including the date column).

The dataset contains monthly average retail prices for products purchased by U.S. households, including:

- Meat and poultry
- Dairy products and eggs
- Bakery products and grains
- Fruits and vegetables
- Coffee and other grocery products
- Gasoline and utility gas

The original data comes from the BLS Average Price Data program, which collects and reports average prices for selected consumer goods in U.S. urban areas.

### Additional Data Source

For the interactive dashboard, the project also uses the U.S. Consumer Price Index (CPI-U) series `CPIAUCSL`, retrieved from FRED (Federal Reserve Economic Data).

FRED: https://fred.stlouisfed.org/series/CPIAUCSL

CPI is used as a general inflation benchmark to help compare grocery and energy price changes with broader consumer price movements.

## Project Workflow

### 1. Data Loading

- Downloaded the dataset directly from Kaggle using the KaggleHub library.
- Loaded the CSV file into a Pandas DataFrame.
- Examined the dataset structure, dimensions, data types, and missing values.

### 2. Data Cleaning and Preparation

- Converted the date column into a datetime format.
- Checked for duplicate rows, columns, dates, and column names.
- Identified and visualized missing values.
- Removed 19 product columns containing 40 or more missing values.
- Applied two methods to estimate remaining missing prices:
  - Linear interpolation.
  - Historical average month-to-month percentage change.
- Selected the historical percentage-change method for most applicable columns, using linear interpolation for romaine lettuce.

### 3. Feature Engineering

The remaining 55 products were manually grouped into broader categories to support meaningful comparisons and consistent visualization.

The categories include:

- Meat
- Poultry
- Dairy and fats
- Eggs
- Bakery and grains
- Fruits and vegetables
- Other grocery products
- Energy

### 4. Exploratory Data Analysis (EDA)

The analysis explores several questions:

- By what percentage did the price of each category increase between January 2015 and July 2026?
- Which categories experienced the fastest price increases?
- How did average category prices change over time?
- Which years experienced the largest year-over-year price increases or decreases?
- How many individual products became more expensive, and by how much?
- Were price increases consistent across products within each category, or driven by a few products?

### 5. Data Visualization

The project includes:

- **Bar Charts:** Percentage price increases by category.
- **Line Charts:** Monthly price trends using category-level statistics, including mean, median, minimum, and maximum.
- **Heatmaps:** Year-over-year percentage changes in average category prices.
- **Pie Charts:** Distribution of individual products by percentage price increase or decrease.
- **Box Plots:** Comparison of individual product price changes across categories.

### 6. Interactive Dashboard

An interactive dashboard titled **U.S. Consumer Price Trends** was developed using Python Dash and Plotly.

Dashboard features include:

- Category Overview and Item Detail views.
- Interactive year-range selection.
- Category and product filters.
- KPI cards showing the number of products compared, median price change, latest year-over-year change, and the proportion of products rising faster than inflation.
- Price trend comparisons against general inflation (CPI).
- Bargain Finder identifying products that became cheaper or more expensive relative to inflation.
- Interactive charts that can be dragged and resized.
- CSV export for filtered data.
- Dashboard layout reset functionality.

## Technologies and Tools

- **Python** – Data analysis and programming.
- **Pandas** – Data manipulation and cleaning.
- **NumPy** – Numerical calculations.
- **Matplotlib** – Data visualization.
- **Seaborn** – Statistical visualization.
- **Plotly** – Interactive charts.
- **Dash** – Interactive dashboard development.
- **KaggleHub** – Dataset retrieval.
- **Pandas DataReader** – Retrieving CPI data from FRED.
- **Jupyter Notebook / Google Colab** – Project development and analysis.


## How to Run the Project

### Option 1: Google Colab

1. Download or clone this repository.
2. Open [Google Colab](https://colab.research.google.com/).
3. Upload `NPW_Data_Analytics_Project_Group_1.ipynb`.
4. Run the notebook cells in order.
5. Ensure internet access is available for downloading the Kaggle dataset and retrieving CPI data from FRED.

The notebook uses KaggleHub to download the original dataset. If Kaggle requires authentication, configure your Kaggle credentials in the Colab environment.

The interactive dashboard section uses Google Colab-specific functionality to display the Dash application.

### Option 2: Local Python Environment

1. Clone the repository:

   `git clone https://github.com/YOUR-USERNAME/us-grocery-gas-price-analysis.git`

2. Navigate to the project directory:

   `cd us-grocery-gas-price-analysis`

3. Install dependencies:

   `pip install -r requirements.txt`

4. Open the notebook using Jupyter Notebook or JupyterLab.

5. Configure Kaggle access and run the notebook cells.

**Note:** The interactive dashboard code uses Google Colab's `google.colab.output` functionality. Running the dashboard outside Colab may require adapting the application launch code.

## Key Project Outcomes

This project demonstrates practical data analytics skills, including:

- Retrieving and exploring real-world datasets.
- Identifying and handling missing data.
- Applying different data imputation techniques.
- Transforming and categorizing raw data.
- Performing exploratory and comparative data analysis.
- Calculating percentage changes and year-over-year trends.
- Creating informative static and interactive visualizations.
- Developing an interactive dashboard for data exploration.
- Comparing product price movements against general inflation.

## Team Members

**NPower Canada – Data Analytics Project, Group 1**

- Mohamed Ali Abidi
- Venkata Prasanna Dama
- XinXin (Nate) Huang
- Lamia Jarid
- Emma Ma
- Million Meshesha
- Upadya Ratnayake
- Naznin Sharmin Shishir

## Acknowledgments

This project was completed collaboratively as part of the NPower Canada Data Analytics Training Program.

We acknowledge Kaggle and the U.S. Bureau of Labor Statistics for providing the grocery and energy price data, and the Federal Reserve Bank of St. Louis for providing CPI data through FRED.

---

**Project Category:** Data Analytics | Exploratory Data Analysis | Data Visualization | Interactive Dashboard

**Developed using:** Python, Pandas, Plotly, and Dash.
