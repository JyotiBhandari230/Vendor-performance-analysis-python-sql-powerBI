# 📊 Vendor Performance Analysis – Retail Inventory & Sales  

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)  
[![SQL](https://img.shields.io/badge/SQL-Data%20Analysis-orange)](https://en.wikipedia.org/wiki/SQL)  
[![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-yellow)](https://powerbi.microsoft.com/)  
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-red)](https://jupyter.org/)  

Analyzing **vendor efficiency and profitability** to support smarter purchasing and inventory decisions using **SQL, Python, and Power BI**.  

---

## 📌 Table of Contents  
- [Overview](#overview)  
- [Pipeline](#pipeline)  
- [Business Problem](#business-problem)  
- [Dataset](#dataset)  
- [Tools & Technologies](#tools--technologies)  
- [Project Structure](#project-structure)  
- [Data Cleaning & Preparation](#data-cleaning--preparation)  
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
- [Research Questions & Key Findings](#research-questions--key-findings)  
- [Dashboard](#dashboard)  
- [How to Run This Project](#how-to-run-this-project)  
- [Final Recommendations](#final-recommendations)  
- [Author & Contact](#author--contact)  

---

## 📖 Overview  
This project evaluates vendor performance in a **retail sales & inventory** setting.  
It identifies **profitable vendors, cost efficiency, and sales contribution**, helping businesses optimize vendor selection and inventory planning.  

---

## 🔄 Pipeline  
1. **Data Ingestion** → Load data into SQL  
2. **Cleaning & Transformation** → Prepare structured dataset  
3. **Exploratory Data Analysis (EDA)** → Vendor trends, profit margins, performance  
4. **Visualization** → Build interactive dashboards in Power BI  
5. **Insights & Strategy** → Data-driven vendor management  

---

## 💡 Business Problem  
Effective inventory and sales management are critical in the retail sector. This project aims to:  

- Identify **underperforming brands** needing pricing or promotional adjustments  
- Determine **vendor contributions** to sales and profits  
- Analyze the **cost-benefit of bulk purchasing**  
- Investigate **inventory turnover inefficiencies**  
- Statistically validate **differences in vendor profitability**  

---

## 📂 Dataset  
- Multiple CSV files located in `/data/` folder (sales, vendors, inventory)  
- Summary tables created from ingested data and used for analysis  

---

## 🛠️ Tools & Technologies  
- **SQL** → CTEs, Joins, Filtering  
- **Python** → Pandas, Matplotlib, Seaborn, SciPy  
- **Power BI** → Interactive Visualizations  
- **GitHub** → Version control & collaboration  

---

## 📂 Project Structure  
vendor-performance-analysis/
│
├── README.md
├── .gitignore
├── requirements.txt
├── Vendor Performance Report.pdf
│
├── notebooks/                  # Jupyter notebooks
│   ├── EDA.ipynb
│   ├── vendor_performance_analysis.ipynb
│   ├── db creation & scripting.ipynb
│
├── scripts/                    # Python scripts for ingestion and processing
│   ├── ingestion_db.py
│   └── get_vendor_summary.py
│
├── dashboard/                  # Power BI dashboard file
│   └── dashboard data
│   └── vendor_performance_dashboard.pbix
│   └── Dashboard Image.png
├── dataset/                  # Project Dataset
│   └── data.txt



---

## 🧹 Data Cleaning & Preparation  
- Removed transactions with:  
  - Gross Profit ≤ 0  
  - Profit Margin ≤ 0  
  - Sales Quantity = 0  
- Created **summary tables** with vendor-level metrics  
- Converted data types, handled outliers, merged lookup tables  

---

## 📊 Exploratory Data Analysis (EDA)  
**Negative or Zero Values Detected**  
- Loss-making sales (Gross Profit min: -52,002.78)  
- Sales at or below cost (Profit Margin = -∞)  
- Unsold inventory (slow-moving stock)  

**Outliers Identified**  
- High Freight Costs (up to 257K)  
- Extreme purchase/actual price variations  

**Correlation Analysis**  
- Weak: Purchase Price vs Profit  
- Strong: Purchase Qty vs Sales Qty (0.999)  
- Negative: Profit Margin vs Sales Price (-0.179)  

---

## 🔍 Research Questions & Key Findings  
1. **Brands for Promotions** → 198 brands with low sales but high profit margins  
2. **Top Vendors** → 10 vendors = 65.7% of purchases (risk of over-reliance)  
3. **Bulk Purchasing Impact** → 72% cost savings per unit in large orders  
4. **Inventory Turnover** → $2.71M worth of unsold inventory  
5. **Vendor Profitability**  
   - High Vendors: Mean Margin = 31.17%  
   - Low Vendors: Mean Margin = 41.55%  
6. **Hypothesis Testing** → Statistically significant differences in vendor strategies  

---

## 📈 Dashboard  
Power BI Dashboard highlights:  
- Vendor-wise sales & margins  
- Inventory turnover  
- Bulk purchase savings  
- Performance heatmaps  

📊 **Dashboard Preview**:  
  <img width="1363" height="774" alt="dashboard image" src="https://github.com/user-attachments/assets/31665245-b2d4-4513-bf13-32d056392e11" />


---

## ⚡ How to Run This Project  
```bash
# Clone the repository
git clone https://github.com/yourusername/vendor-performance-analysis.git
cd vendor-performance-analysis

# Install dependencies
pip install -r requirements.txt

# Run the ingestion pipeline:
python scripts/ingestion_db.py
python scripts/get_vendor_summary.py

# Open Jupyter Notebooks:
notebooks/EDA.ipynb
notebooks/vendor_performance_analysis.ipynb

# Open Power BI Dashboard:
dashboard/vendor_performance_dashboard.pbix

---

##  📌 Final Recommendations

Based on the vendor performance analysis, the following recommendations are proposed to strengthen operations and maximize profitability:

1. **🌐 Diversify Vendor-Based Risk**  
   - Reduce dependency on a few vendors by expanding the supplier base.  
   - This helps mitigate risks of supply chain disruption and ensures business continuity.

2. **📦 Optimize Bulk Order Strategy**  
   - Place bulk orders with top-performing vendors to leverage discounts and ensure timely availability.  
   - Maintain a balance to avoid overstocking and holding costs.

3. **💰 Reprice Slow-Moving High-Margin Vendors**  
   - Identify vendors whose products have high margins but low sales velocity.  
   - Reprice strategically to boost sales without compromising profitability.

4. **📉 Clear Unsold Inventory Strategically**  
   - Use promotions, discounts, or bundling techniques to clear slow-moving or unsold stock.  
   - Prevents capital lock-in and frees up storage for fast-moving products.

5. **📢 Improve Marketing for Underperforming Vendors**  
   - Increase visibility and targeted promotions for vendors with potential but lower performance.  
   - Implement digital marketing, campaigns, or loyalty programs to boost their sales contribution.

✅ By applying these strategies, the organization can reduce risks, improve vendor collaboration, and achieve sustainable growth.

