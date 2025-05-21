# 🛒 Blinkit Sales Data Analysis – Python Project

This project presents a detailed data analysis of Blinkit's product sales using Python. The goal is to uncover key performance indicators (KPIs) and insights that can guide business decisions in the retail and e-commerce space.

---

## 📌 Project Overview

This analysis dives into sales performance based on various attributes such as item type, fat content, and outlet location. The dataset includes detailed fields such as item sales, ratings, and types, allowing for KPI tracking and visualization.

---

## 👤 Author

**Aravind Prabhakar A**

---

## 🧰 Libraries Used

- pandas
- numpy
- matplotlib
- seaborn

---

## 📂 Dataset

The dataset (`blinkit_data.csv`) includes fields such as:

- `Item Type`
- `Item Fat Content`
- `Sales`
- `Rating`
- `Outlet Location Type`

> **Note**: The data was preprocessed to clean inconsistencies, especially in categorical values like fat content (e.g., converting `LF`, `low fat`, `reg` to `Low Fat` and `Regular`).

---

## 🎯 Business Goals

- Analyze total and average sales
- Identify most and least performing item types
- Examine influence of item fat content on sales
- Compare outlet location types by sales distribution

---

## 📈 Key Insights

### KPIs Extracted:
- **Total Sales**: Sum of all product sales
- **Average Sales**: Mean sales per item
- **Number of Items Sold**
- **Average Customer Rating**

### Visualizations Included:
- Pie chart of sales by fat content
- Bar chart of sales by item type
- Grouped bar chart of outlet tier vs. fat content sales

---

## 📊 Sample Code Snippets

```python
# Total sales by fat content
sales_by_fat = df.groupby('Item Fat Content')['Sales'].sum()
plt.pie(sales_by_fat, labels=sales_by_fat.index, autopct='%.1f%%', startangle=90)
plt.title('Sales by Fat Content')
plt.axis('equal')
plt.show()

