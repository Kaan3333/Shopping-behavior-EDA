# Istanbul Retail Trends — Customer Behavior Analysis

Exploring customer shopping behavior in Istanbul to identify patterns in demographics, purchasing categories, and payment preferences.

---

## 📊 Dataset Description
- **Source:** place your CSV in `data/istanbul_sales_data.csv` (or add a public link here if available).  
- **Typical shape:** ~3k rows × 7 columns (please replace with the actual numbers from your data).  
- **Key variables:**  
  - `Invoice ID` — Unique transaction identifier  
  - `Gender` — Male / Female  
  - `Age` — Customer age  
  - `Category` — Product category purchased  
  - `Quantity` — Number of items purchased  
  - `Price` — Transaction price (per item or total — note which one in your notebook)  
  - `Payment Method` — e.g., Credit Card, Cash, E-Wallet  
- **Notable quirks:** missing values in some demographic fields, occasional outlier prices/quantities, category imbalance. (See notebook for exact cleaning details.)

---

## 🎯 Research Goal / Question
What features and demographic factors influence shopping behavior (quantity, price, category choice, payment method) — and how do they interact?

---

## 🔍 Steps You Took (short summary — not full code)
1. **Data cleaning**
   - Standardized column names, fixed types, handled missing values, removed obvious outliers.
2. **Univariate analysis**
   - Distribution checks for `Gender`, `Age`, `Category`, `Quantity`, `Price`, `Payment Method`.
3. **Bivariate analysis**
   - Cross-tabulations and groupby/aggregations to study relationships such as:
     - `Gender` vs `Payment Method`
     - `Category` vs `Quantity`
     - `Category` vs `Quantity` segmented by `Gender`
     - `Age` vs `Price` (correlation / trend)
     - `Price` vs `Quantity` (correlation)
     - `Payment Method` vs average basket value
   - Used pivot tables, chi-square tests (for categorical pairs) and Pearson/Spearman correlations (for numeric pairs) where appropriate.
4. **Exploratory Data Analysis (EDA) & Visualizations**
   - Bar charts, boxplots, histograms, heatmaps, and scatter plots to visualize distributions and relationships.
   - Saved key figures to `figures/`.

---

## 📌 Main Findings (summary — expand in the notebook)
- **Demographic skews:** Gender and age groups show different category preferences and payment-method usage.  
- **Payment-method differences:** Payment method distribution differs by gender and age; some methods associate with larger average basket values.  
- **Category vs Quantity:** Certain categories consistently have higher quantities per invoice; these patterns change when segmented by gender.  
- **Price–Quantity relationship:** Price and quantity show limited direct correlation — higher quantity doesn’t necessarily imply higher spend per item (check notebook for exact correlation coefficients).

---

## ⚙️ How to Reproduce the Project
**Prerequisites**
- Python 3.9+  
- `pip` and virtualenv/venv recommended.


**Steps:**
1. Clone this repository.
2. Open `EDA_shopping_behavior.ipynb` in Jupyter Notebook or JupyterLab.
3. Run all cells to reproduce the analysis.

---

## 🚀 Next Steps
- Build a predictive model for purchase quantity or price.
- Analyze seasonal trends if date data is available.
- Expand dataset with more demographic features for richer segmentation.
