# 👗 Fashion Retail Analytics

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)
![XGBoost](https://img.shields.io/badge/XGBoost-1.7+-orange.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-red.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

> **Complete Fashion Retail Data Analysis Project with Python**

---

## 📊 Project Overview

This project provides a comprehensive analysis of a fashion retail store dataset, including **data cleaning**, **exploratory data analysis**, **customer segmentation**, **campaign analysis**, and **revenue forecasting** using machine learning.

### 🎯 Project Objectives

- ✅ **Data Cleaning & Validation** - Identify and fix data quality issues
- ✅ **Sales Analysis** - Analyze product, category, and country performance
- ✅ **Customer Segmentation** - RFM analysis with 5 customer segments
- ✅ **Campaign Analysis** - Evaluate marketing campaign performance
- ✅ **Revenue Forecasting** - Machine learning models (XGBoost, Random Forest)

---

## 📁 Dataset Structure

The project uses **7 CSV data files**:

| File | Description | Records |
|------|-------------|---------|
| `customers.csv` | Customer information | ~600 |
| `products.csv` | Product details | ~500 |
| `sales.csv` | Sales transactions | ~2,200 |
| `sale_items.csv` | Sales line items | ~2,250 |
| `stock.csv` | Inventory data | ~4,000 |
| `campaigns.csv` | Marketing campaigns | ~20 |
| `channels.csv` | Sales channels | ~10 |

---

## 📈 Key Results

### Business Overview

| Metric | Value |
|--------|-------|
| **Total Transactions** | 2,253 |
| **Total Quantity Sold** | 6,715 |
| **Total Revenue** | €324,236.66 |
| **Total Profit** | €141,153.29 |
| **Number of Customers** | 580 |
| **Number of Products** | 499 |

### 🏆 Top Products by Revenue

| Rank | Product | Revenue | Profit | Margin |
|------|---------|---------|--------|--------|
| 1 | Relaxed Ribbed Trousers | €2,379 | €1,130 | 47.5% |
| 2 | Modern Cotton Tee | €1,920 | €904 | 47.1% |
| 3 | Modern High-Waist Trousers | €1,908 | €621 | 32.6% |
| 4 | Dresses Drop 1 | €1,858 | €990 | 53.3% |
| 5 | Bold High-Waist Dress | €1,804 | €1,052 | 58.3% |

### 📊 Category Performance

| Category | Revenue | Profit | Margin |
|----------|---------|--------|--------|
| Shoes | €70,074 | €30,473 | 43.5% |
| T-Shirts | €69,693 | €30,783 | 44.2% |
| Dresses | €68,391 | €29,847 | 43.6% |
| Sleepwear | €62,277 | €26,001 | 41.8% |
| Pants | €53,803 | €24,050 | 44.7% |

### 🌍 Sales Markets (No Local Stock)

| Country | Transactions | Revenue | Profit |
|---------|--------------|---------|--------|
| Italy | 415 | €59,458 | €26,131 |
| Netherlands | 326 | €46,841 | €20,328 |
| Spain | 276 | €41,115 | €17,806 |
| Portugal | 201 | €29,931 | €12,992 |

---

## 👥 Customer Segmentation (RFM Analysis)

RFM analysis divides customers into **5 segments**:

| Segment | Customers | Percentage |
|---------|-----------|------------|
| ⭐ Champions | 162 | 27.9% |
| ⚠️ At Risk | 149 | 25.7% |
| 💪 Potential Loyalists | 131 | 22.6% |
| 🤝 Loyal Customers | 122 | 21.0% |
| ❌ Lost Customers | 16 | 2.8% |

**Total Customers:** 580

---

## 🤖 Machine Learning Models

### Model Performance Comparison

| Model | MAE | RMSE | R² |
|-------|-----|------|-----|
| **XGBoost** | **€1,258** | **€1,859** | **0.513** |
| Random Forest | €1,298 | €1,902 | 0.489 |
| Linear Regression | €2,104 | €2,789 | -0.123 |
| Naive Baseline | €3,261 | €4,554 | -1.053 |

### 🏆 Best Model: XGBoost

- **61.4% improvement** over baseline
- **R² = 0.513** indicates good predictive power
- Captures weekly seasonality and campaign effects

### Top Feature Importance (XGBoost)

| Feature | Importance |
|---------|------------|
| Revenue Lag 7 Days | 0.22 |
| Rolling Mean 7 Days | 0.18 |
| Revenue Lag 14 Days | 0.15 |
| Rolling Mean 14 Days | 0.12 |
| Is Weekend | 0.05 |

---

## 💡 Business Insights & Recommendations

### 1. Inventory Management 🏪
- **Open local warehouses** in Italy, Netherlands, Spain, Portugal
- **Increase stock** of high-margin products (Pants: 44.7% margin)
- **Prioritize Dresses** (58.3% margin for top products)

### 2. Marketing & Campaigns 📣
- **Only 10% of sales** influenced by campaigns (229 out of 2,253)
- **Increase campaign frequency** to reach more customers
- **Target "At Risk" customers** with special offers

### 3. Customer Strategy 🤝
- **Loyalty program** for 162 Champions
- **Re-engagement campaigns** for 149 At Risk customers
- **Win-back offers** for 16 Lost Customers

### 4. Product Strategy 👗
- **Feature top 5 products** in marketing materials
- **Bundle deals** with popular products
- **Develop similar collections** to Dresses Drop 1

---

## 🚀 Installation & Setup

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation Steps

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/fashion-retail-analytics.git
cd fashion-retail-analytics

# 2. Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the project
python main.py
