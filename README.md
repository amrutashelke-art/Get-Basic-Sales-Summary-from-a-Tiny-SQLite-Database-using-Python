# Get-Basic-Sales-Summary-from-a-Tiny-SQLite-Database-using-Python

## 📌 Objective
Use SQL inside Python to pull simple sales info (like total quantity sold, total revenue) and display it using basic print statements and a simple bar chart.

## 🧰 Tools Used
- Python
- SQLite (`sqlite3`)
- pandas
- matplotlib
- Jupyter Notebook

## 📁 Dataset
Created a SQLite database file `sales_data.db` with a `sales` table including:
- product (TEXT)
- quantity (INTEGER)
- price (REAL)

## 🧪 SQL Query Used
```sql
SELECT 
  product, 
  SUM(quantity) AS total_qty, 
  SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
