# 🔍 Smart Risk Segmentation in Hire Purchase Loan Audit

This project showcases how Internal Audit can be enhanced with **Data Analytics** by using a simulated dataset of **Hire Purchase (Auto Loan)** customers.  
We explore how to evaluate credit behavior, assess financial burden, and segment customer risk using real-world inspired business rules.

---

## 📊 Project Objective

To demonstrate the application of data analytics in Internal Audit through:

- Credit risk analysis using NCB Score
- Financial burden analysis using Installment-to-Income Ratio
- Rule-based **Risk Segmentation** (High / Medium / Low)
- Visualization & Insight extraction to support risk-based audit

---

## 📁 Dataset

A simulated dataset representing auto loan (hire purchase) customers with the following key columns:

- `Age`  
- `Income` (monthly)
- `Monthly Payment`
- `NCB Score`
- `Missed Payments`
- `Payment Status` (`On Time`, `Late`, `Default`)

> **Note:** The data used is entirely self-generated and for educational/demo purposes only.

---

## ⚙️ Tools Used

- 🐼 `Pandas` for data handling  
- 📊 `Seaborn`, `Matplotlib` for visualizations  
- 📈 `NumPy` for numerical operations  
- 💡 Google Colab as the main working environment

---

## 🧠 Key Analysis Steps

1. **Data Cleaning**  
   - Remove invalid records (e.g., age < 18, income ≤ 0, NCB score out of range)

2. **EDA (Exploratory Data Analysis)**  
   - Distribution of credit scores  
   - Correlation between missed payments and NCB  
   - Income vs Installment behavior grouped by payment status

3. **Installment-to-Income Ratio**  
   - A new feature to measure payment burden

4. **Risk Segmentation**  
   - Rule-based segmentation using:
     - `Installment-to-Income Ratio`
     - `NCB Score`

```python
# Example rules:
if ratio > 0.6 or NCB < 550 → High Risk  
elif ratio > 0.4 or NCB < 600 → Medium Risk  
else → Low Risk
