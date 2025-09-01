# UK E-Commerce Dashboard (Power BI + Python Preprocessing)

##  Project Overview
This project features a **Power BI dashboard** built using a UK-based e-commerce dataset, visualizing key business metrics like revenue trends, top-performing products, customer segments, and geographic distribution.

##  Dataset
- **Source**: [Kaggle – E-Commerce Data (UK Retail Online)](https://www.kaggle.com/datasets/carrie1/ecommerce-data)  
- **Contents**: Transaction-level data (Dec 2010–Dec 2011) including:
  - InvoiceNo, StockCode, Description
  - Quantity, InvoiceDate, UnitPrice
  - CustomerID, Country
- **Usage**: Original dataset not included due to licensing. Download from Kaggle and place in the repository root as `raw_data.csv`.

##  Project Structure
├── cleaned_data.pbix ← Power BI dashboard file
├── datasets/
│ └── raw_data.csv ← Place Kaggle CSV file here
├── notebooks/
│ └── data_cleaning.ipynb ← (Optional) Python notebook for preprocessing
├── images/
│ └── dashboard.png ← Screenshot of the dashboard
└── README.md

##  Preprocessing (Optional – Python + Pandas)

- Loaded `raw_data.csv` using Pandas.
- Removed rows with missing `CustomerID` or `Description`.
- Filtered out negative `Quantity` values and zero-priced items.
- Created `TotalAmount = Quantity × UnitPrice`.
- Extracted Year-Month, Month, Day, Hour from `InvoiceDate`.
- Saved final clean dataset as `cleaned_data.csv`.

##  Tools & Technologies
- **Power BI Desktop** – Dashboard creation and visualization.
- **Python (Pandas, NumPy)** – Data cleaning.
- **Kaggle** – Source of the dataset.

##  Dashboard Features
- **KPIs**: Total Revenue, Quantity Sold, Number of Unique Customers, Average Order Value.
- **Visuals**:
  - Monthly revenue trends line chart.
  - Best sellers by revenue and quantity sold.
  - Revenue by country shown on a map.
  - Customer segment breakdown via donut chart.
- **Filters/Slicers**: Country, Invoice Date and Customer Segments.


## 📊 Dashboard Preview
![Dashboard Screenshot](images/ecommerce%20dashboard%20screenshot.png)



##  Getting Started
1. Download the dataset from Kaggle and place it at `datasets/raw_data.csv`.
2. If preprocessing:
   - Navigate to `notebooks/data_cleaning.ipynb`, run cells to generate cleaned data.
3. Open `cleaned_data.pbix` via Power BI Desktop.
4. Interact with the dashboard using slicers and visuals.

##  Future Enhancements
- Introduce profit/margin calculations (if cost data becomes available).
- Add customer retention or repeat-purchase metrics.
- Implement drill-through pages for deeper product or segment analysis.
- Polish visual consistency and theme across dashboard.

##  Licensing
- **Dataset License**: Please refer to Kaggle’s terms for the dataset.

---
