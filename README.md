# Market Basket Analysis: Energy Consumption Forecast and Monitoring

This project applies the **Apriori algorithm** to a transactional grocery dataset to uncover hidden buying patterns through **Market Basket Analysis (MBA)**. The goal is to transform raw transactional data into actionable business intelligence for optimized product placement and promotional strategies.

---

## 📌 Project Overview

In the retail sector, manual analysis of massive datasets is inefficient due to data overload. This project utilizes automated data mining techniques to identify strong associations between products (e.g., items frequently purchased together) to enhance **cross-selling** and **up-selling** opportunities.

**Student:** Rabiul Islam  
**Student ID:** AIU22102258  
**Course:** Data Mining (Individual Assignment)  
**Institution:** Albukhary International University  

---

## 🛠️ Tech Stack

- **Language:** Python  
- **Libraries:** `pandas`, `mlxtend` (Apriori & Association Rules), `TransactionEncoder`  
- **Tools:** Jupyter Notebook, Kaggle Datasets  

---

## 📊 Dataset

The analysis was performed on a publicly available **Groceries Dataset** from Kaggle.

**Attributes**
- `Member_number`
- `Date`
- `itemDescription`

**Structure**
- Thousands of unique products
- Numerous transactions

**Format**
- Categorical data where each row represents an item within a transaction

---

## ⚙️ Methodology

The project follows a standard data mining framework (ETL process):

1. **Extract**  
   Raw data is read from CSV into a `pandas` DataFrame.

2. **Transform**  
   Data is one-hot encoded where each **transaction** is a row and each **unique product** is a column with binary values (`1` if present, `0` if not).

3. **Algorithm Implementation**  
   The **Apriori** algorithm is applied to find frequent itemsets meeting a minimum support threshold.

4. **Analysis**  
   Association rules are generated and filtered by **confidence** and **lift**.

---

## 📈 Key Experiments & Results

Experiments were conducted with:
- **Minimum support:** `0.001`
- **Minimum confidence:** `0.21`

### Top Product Combinations

| Antecedent        | Consequent         | Support   | Lift   |
|------------------|--------------------|----------:|-------:|
| Rolls/Buns       | Whole Milk         | 0.013968  | 0.804  |
| Yogurt           | Whole Milk         | 0.011161  | 0.822  |
| Soda             | Other Vegetables   | 0.009691  | 0.817  |
| Sausage          | Whole Milk         | 0.008955  | 0.939  |

**Insight:** The **Sausage → Whole Milk** combination showed the highest lift (**0.939**), indicating a very strong positive association between these two items.

---

## 💡 Conclusion

The Apriori algorithm successfully revealed hidden relationships in large transactional datasets. Businesses can use these insights to:

- Improve product placement (e.g., placing associated items in the same aisle)
- Develop targeted promotions and bundling strategies
- Enhance cross-selling and up-selling to increase profitability

---

## 📎 Notes

- Dataset source: Kaggle “Groceries Dataset”
- Analysis approach: Market Basket Analysis via Apriori + Association Rules
