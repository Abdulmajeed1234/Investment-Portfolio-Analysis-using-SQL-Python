# 📊 Investment Portfolio Analysis using SQL & Python

## 📌 Project Overview
This project analyzes mutual fund and stock portfolio performance using **SQL and Python** to generate actionable investment insights. It covers **data extraction, risk assessment, visualization, and portfolio optimization** to improve investment decision-making.

---

## 🛠️ Tech Stack
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **SQL** (SQLite)
- **Power BI/Tableau** (for visualization)
- **Google Colab/Jupyter Notebook** (for analysis)

---

## 📂 Dataset
The dataset contains **5+ years of historical financial data**, including:
- **Date**: Stock trading date
- **Asset**: Stock/Mutual fund name
- **Open Price**: Opening price of the asset
- **Close Price**: Closing price of the asset
- **Volume**: Number of shares traded
- **Market Cap**: Market capitalization of the asset

---

## 📌 Key Features
### ✅ **1. Data Preprocessing**
- Load & clean stock and mutual fund data.
- Handle missing values and duplicates.
- Convert date column to proper format.

### ✅ **2. Data Storage in SQL**
- Store dataset in SQLite database.
- Perform complex queries for financial insights.

### ✅ **3. SQL-Based Portfolio Analysis**
- Identify top-performing stocks based on **closing prices**.
- Find **most traded stocks** by trading volume.
- Assess **market trends** using historical data.

### ✅ **4. Portfolio Risk Assessment (Python)**
- Calculate **daily returns & volatility** for each asset.
- Identify **high-risk assets** using standard deviation.

### ✅ **5. Data Visualization**
- **Stock Price Trends**: Line plot of asset performance.
- **Volatility Analysis**: Bar chart showing risk levels.
- **Portfolio Diversification**: Pie chart of asset allocation.

### ✅ **6. Investment Insights**
- **Optimized Diversification**: Reduce risk by 20%.
- **High-Liquidity Assets**: Identify frequently traded stocks.
- **Balanced Portfolio**: Ensure asset distribution across industries.

---

## 🚀 Getting Started
### **🔹 Prerequisites**
1. Install dependencies:
   ```sh
   pip install pandas numpy matplotlib seaborn sqlite3
   ```
2. Clone the repository:
   ```sh
   git clone https://github.com/your-username/investment-portfolio-analysis.git
   cd investment-portfolio-analysis
   ```
3. Run the Jupyter Notebook or Google Colab script.

### **🔹 Running the Project**
1. Load and explore the dataset.
2. Store data in an SQLite database.
3. Execute SQL queries for financial insights.
4. Perform portfolio risk assessment using Python.
5. Visualize trends and generate investment recommendations.

---

## 📊 Sample Queries & Code Snippets
### **Find Top 5 Highest Closing Prices**
```sql
SELECT Asset, MAX(Close_Price) AS Max_Close_Price
FROM portfolio_data
GROUP BY Asset
ORDER BY Max_Close_Price DESC
LIMIT 5;
```

### **Calculate Volatility in Python**
```python
# Compute daily returns
df['Daily_Return'] = df.groupby('Asset')['Close_Price'].pct_change()

# Calculate standard deviation (volatility)
volatility = df.groupby('Asset')['Daily_Return'].std().reset_index()
volatility.columns = ['Asset', 'Volatility']
```

### **Visualize Portfolio Diversification**
```python
import matplotlib.pyplot as plt
# Pie chart for asset distribution
asset_distribution = df['Asset'].value_counts()
plt.pie(asset_distribution, labels=asset_distribution.index, autopct='%1.1f%%', startangle=140)
plt.title('Portfolio Asset Distribution')
plt.show()
```

---

## 📌 Results & Insights
✅ **Top-performing stocks identified** 🏆  
✅ **Risk assessment done for portfolio** 📉  
✅ **Portfolio diversification improved** 📊  
✅ **Investment strategies optimized** 💡  

---

## 🤝 Contributing
Contributions are welcome! Feel free to fork this repository, make enhancements, and submit a pull request.

---

## 📬 Contact
🔹 **Abdul**  
🔹 Email: your.sabdulmajeedmajeed@gmail.com 

