# Pricing & Sales Analytics Engine

An end-to-end **Pricing Intelligence & Demand Forecasting Pipeline** built with Python using:

* **Pandas** for data processing
* **Statsmodels** for elasticity modeling & ARIMA forecasting
* **OpenPyXL** for automated Excel reporting & formatting

This project analyzes product sales data, generates pricing insights, forecasts demand, segments products, simulates discount strategies, and exports everything into a professionally formatted Excel dashboard.

---

#  Features

## Data Processing

* Loads raw sales dataset
* Cleans and transforms data
* Creates engineered business features

## Profitability Analysis

* Calculates:

  * Product cost
  * Profit per unit
  * Total profit
  * Profit margins

## Price Elasticity Modeling

Uses **OLS Regression** to estimate:

* Demand sensitivity to discounts
* Impact of ratings & reviews on sales

## Demand Forecasting

Uses **ARIMA Time Series Forecasting** to:

* Predict future demand
* Generate next-period sales estimates

## Product Segmentation

Automatically classifies products into:

* Star
* Cash Cow
* Question Mark
* Dead Stock

## Discount Simulation Engine

Simulates:

* Revenue impact
* Profit impact
* Quantity demand changes
  for different discount percentages.

## Decision Recommendation Engine

Provides strategic business recommendations:

* Reduce discounting
* Increase marketing
* Remove underperforming products

## Automated Excel Report

Exports:

* Processed data
* Forecasts
* Simulations
* Recommendations
* Segmentation analysis

with:

* Auto formatting
* Color-coded decision indicators
* Dynamic column widths

---

# Project Structure

```bash
project/
│
├── amazon_sales_dataset.csv
├── pricing_engine.py
├── pricing_insights.xlsx
└── README.md
```

---

# Installation

## 1. Clone Repository

```bash
git clone https://github.com/yourusername/pricing-analytics-engine.git

cd pricing-analytics-engine
```

## 2. Install Dependencies

```bash
pip install pandas numpy statsmodels openpyxl
```

---

# Dataset Requirements

Your CSV file must contain the following columns:

| Column Name      | Description              |
| ---------------- | ------------------------ |
| order_date       | Date of order            |
| product_id       | Unique product ID        |
| price            | Original product price   |
| discounted_price | Discounted selling price |
| discount_percent | Discount percentage      |
| quantity_sold    | Units sold               |
| rating           | Product rating           |
| review_count     | Number of reviews        |
| total_revenue    | Revenue generated        |

---

# Run the Project

```bash
python pricing_engine.py
```

---

# Pipeline Workflow

## 1. Load Data

Reads CSV dataset into Pandas DataFrame.

## 2. Feature Engineering

Creates:

* Monthly periods
* Cost estimates
* Profit metrics
* Demand score

## 3. Elasticity Model

Uses regression to estimate:

[
Demand \sim Discount + Rating + Reviews
]

Outputs:

* Elasticity coefficient
* Statistical model summary

---

## 4. Forecasting Engine

Uses:

```python
ARIMA(1,1,1)
```

Forecasts:

* Future product demand
* Next 3 periods

---

## 5. Product Segmentation

### Star

High sales + positive growth

### Cash Cow

High sales + low growth

### Question Mark

Low sales + positive growth

### Dead Stock

Low sales + negative growth

---

## 6. Discount Simulation

Simulates:

* Demand increase/decrease
* Revenue changes
* Profitability changes

using estimated elasticity.

---

## 7. Recommendation Engine

Business rules include:

### Reduce Discounting

Triggered when:

* Profit margin is too low

### Increase Marketing

Triggered when:

* Product is a Star performer

### Consider Removing

Triggered when:

* Product is Dead Stock

---

# Excel Output

Generated file:

```bash
pricing_insights.xlsx
```

Includes sheets:

| Sheet            | Purpose                      |
| ---------------- | ---------------------------- |
| Processed_Data   | Cleaned & engineered dataset |
| Product_Segments | Product classification       |
| Profit_Analysis  | Margin & profitability       |
| Simulation       | Discount simulation          |
| Recommendations  | Business actions             |
| Forecast         | Demand forecasting           |
| README           | Embedded documentation       |

---

# Excel Formatting Features

* Green = Positive business action
* Red = Negative/No action
* Yellow = Product removal warning
* Auto-adjusted column widths

---

# Example Insights

The system can identify:

* Products that are overly discounted
* High-demand products worth marketing
* Dead inventory affecting profitability
* Future sales demand trends
* Price-sensitive customer behavior

---

# Technologies Used

| Technology  | Purpose                  |
| ----------- | ------------------------ |
| Python      | Core programming         |
| Pandas      | Data analysis            |
| NumPy       | Numerical operations     |
| Statsmodels | Regression & forecasting |
| OpenPyXL    | Excel automation         |

---


