## 📌 Project Title

**Basic Sales Summary from a Tiny SQLite Database Using Python**

---

## 📁 Project Description

This project demonstrates how to:

* Convert an online sales CSV file into a SQLite database
* Execute SQL queries using Python (`sqlite3`)
* Analyze and summarize sales data (total units sold & revenue per product)
* Visualize the results using a simple **bar chart**

It is a beginner-friendly example of integrating **SQL with Python** using tools like:

* `sqlite3`
* `pandas`
* `matplotlib`

---

## 📦 Dataset

The dataset is a CSV file named:

```
Online Sales Data.csv
```

### 📊 Columns in the file:

| Column Name      | Description                   |
| ---------------- | ----------------------------- |
| Transaction ID   | Unique ID for the transaction |
| Date             | Transaction date              |
| Product Category | Category of the product       |
| Product Name     | Specific product sold         |
| Units Sold       | Quantity of items sold        |
| Unit Price       | Price per unit                |
| Total Revenue    | Total price (Units × Price)   |
| Region           | Region of sale                |
| Payment Method   | Payment type used             |

---

## 🛠️ Tools Used

| Tool         | Purpose                           |
| ------------ | --------------------------------- |
| `sqlite3`    | Create & query SQLite database    |
| `pandas`     | Data manipulation and SQL loading |
| `matplotlib` | Data visualization (bar chart)    |

---

## 🚀 Getting Started

### 1. Clone or Download the Repo

```bash
git clone https://github.com/your-username/sales-summary-sqlite.git
cd sales-summary-sqlite
```

### 2. Install Dependencies

```bash
pip install pandas matplotlib
```

### 3. Place the CSV File

Ensure `Online Sales Data.csv` is in the same folder as the script.

---

## 🧮 How It Works

### Step 1: Load and Normalize the CSV

* Uses `pandas` to load the CSV
* Strips and normalizes column names for SQL compatibility

### Step 2: Create SQLite Database

* Connects to `sales_data.db`
* Loads the CSV data into a `sales` table

### Step 3: Query for Sales Summary

```sql
SELECT 
    product_name, 
    SUM(units_sold) AS total_units, 
    ROUND(SUM(total_revenue), 2) AS total_revenue 
FROM sales 
GROUP BY product_name 
ORDER BY total_revenue DESC;
```

### Step 4: Plot Top 10 Products

* Uses `matplotlib` to show a **bar chart** of the **top 10 products by revenue**
* Saves the chart as `top10_product_revenue_chart.png`

---

## 📸 Sample Output

| Output File                       | Description                     |
| --------------------------------- | ------------------------------- |
| `sales_data.db`                   | SQLite database with sales      |
| `top10_product_revenue_chart.png` | Clean bar chart of top products |

---

## 📂 Folder Structure

```
.
├── Online Sales Data.csv
├── create_sales_db_and_plot.py
├── sales_data.db
├── top10_product_revenue_chart.png
└── README.md
```

---

## ✅ Deliverables Summary

* [x] Python script to import CSV into SQLite
* [x] SQL query to summarize sales
* [x] `pandas` to print output
* [x] `matplotlib` bar chart for top 10 products
* [x] Chart image saved to file

---

## 🙋‍♂️ Author

**Santhi Raju Peddapati**
B.Tech in CSE (AI & ML)
(https://github.com/SanthiNani)
