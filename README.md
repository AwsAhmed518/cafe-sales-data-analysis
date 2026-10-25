# Cafe Sales Data Analysis | Python & Power BI

An end-to-end data analytics project combining Python-based data cleaning with an interactive Power BI dashboard to explore cafe sales transactions and purchasing patterns.

## Project Overview

This project transforms raw cafe sales data into a cleaned dataset ready for analysis and visualization. Python and Pandas are used to inspect, clean, and prepare the data, while Microsoft Power BI is used to present sales information through an interactive dashboard.

The project demonstrates key data analyst skills, including data exploration, missing-value handling, data type conversion, data preparation, and dashboard development.

## Project Objectives

- Explore and understand the structure and quality of raw sales data.
- Clean inconsistent values and handle missing information.
- Prepare reliable data for analysis and visualization.
- Build an interactive Power BI dashboard to investigate cafe sales performance.
- Demonstrate an end-to-end data analytics workflow.

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Python | Data cleaning and preparation |
| Pandas | Data manipulation and analysis |
| NumPy | Missing-value handling and data preparation |
| Jupyter Notebook | Documenting and executing the cleaning workflow |
| Microsoft Power BI | Interactive dashboards and data visualization |
| CSV | Input and output data storage |

## Dataset Overview

The dataset contains cafe sales transactions with the following fields:

- `Transaction ID` — Transaction identifier.
- `Item` — Cafe product purchased.
- `Quantity` — Number of items purchased.
- `Price Per Unit` — Price of one item.
- `Total Spent` — Total transaction amount.
- `Payment Method` — Method used for payment.
- `Location` — Purchasing location or service type.
- `Transaction Date` — Date of the transaction.

### Dataset Files

| File | Description | Records |
|---|---|---:|
| `dirty_cafe_sales.csv` | Original dataset before cleaning | 10,000 |
| `cleaned_cafe-dataset.csv` | Prepared dataset after cleaning | 9,064 |

The cleaned dataset contains 936 fewer records than the original. These records were removed during the cleaning workflow, including rows with missing transaction dates and rows with missing product information that could not be resolved. The cleaned file retains the same eight columns as the original.

## Data Cleaning & Preparation

The cleaning workflow is documented in `notebooks/Cafe Cleaning.ipynb`.

The process includes:

1. **Data exploration:** Inspecting the dataset structure, dimensions, descriptive statistics, and missing values.
2. **Text standardization:** Cleaning product names and standardizing categorical values.
3. **Invalid-value handling:** Converting invalid numeric entries into missing values for further processing.
4. **Product data cleaning:** Resolving some missing product names using available price information and removing unresolved product records.
5. **Numeric data preparation:** Converting quantity, unit price, and total spending fields into appropriate numeric types.
6. **Missing-value treatment:** Filling missing unit prices using available product-level information and handling missing values in selected numeric and categorical columns.
7. **Date processing:** Converting transaction dates to datetime format and removing records with invalid or missing dates.
8. **Exporting:** Saving the prepared dataset as a CSV file for use in Power BI.

## Power BI Dashboard

The Power BI report is available in `powerbi/gdc_project_pro.pbix`.

The dashboard is intended to make cafe sales data easier to explore through visualizations and interactive filtering.

Areas of analysis include:

- **Sales performance:** Exploring sales metrics and transaction trends.
- **Product analysis:** Comparing performance across cafe products.
- **Transaction and payment analysis:** Exploring payment methods and purchasing locations.

The exact metrics, charts, and available filters can be reviewed by opening the Power BI report.

## Key Questions

This project provides a foundation for exploring questions such as:

- How does sales performance vary over time?
- Which products contribute most to sales?
- How do transaction patterns differ across products?
- Which payment methods are most frequently used?
- How do purchasing locations compare?

Specific findings and recommendations should be added after validating the results in the completed dashboard.


## Dashboard Preview

### 1. Sales Overview

![Sales Overview Dashboard](images/sales-overview.png)

### 2. Product Analysis

![Product Analysis Dashboard](images/product-analysis.png)

### 3. Transaction & Payment Analysis

![Transaction and Payment Analysis Dashboard](images/transaction-payment-analysis.png)


## Repository Structure

```text
cafe-sales-data-analysis/
├── README.md
├── data/
│   ├── dirty_cafe_sales.csv
│   └── cleaned_cafe-dataset.csv
├── notebooks/
│   └── Cafe Cleaning.ipynb
├── powerbi/
│   └── gdc_project_pro.pbix
└── images/
    ├── sales-overview.png
    ├── product-analysis.png
    └── transaction-payment-analysis.png
```

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/cafe-sales-data-analysis.git
cd cafe-sales-data-analysis
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Install the Python Dependencies

```bash
pip install pandas numpy jupyter
```

### 3. Run the Cleaning Notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Open `notebooks/Cafe Cleaning.ipynb` and execute the cells in order. The notebook uses relative paths to access the dataset in the `data` directory.

### 4. Open the Power BI Report

Open `powerbi/gdc_project_pro.pbix` in Microsoft Power BI Desktop.

If necessary, update the data source path to point to `data/cleaned_cafe-dataset.csv`, then refresh the report.

## Skills Demonstrated

- Data exploration and quality assessment
- Data cleaning and transformation
- Missing-value handling
- Data type conversion
- Python and Pandas
- Jupyter Notebook
- Power BI dashboard development
- Data visualization and analytical thinking


## Author
**Aws Ahmed**

**Data Analytics Portfolio Project**

Developed to demonstrate practical data preparation and business intelligence skills using Python and Microsoft Power BI.

---

*This project is intended for educational and portfolio purposes. Interpretations and business recommendations should be based on verified findings from the dashboard.*
