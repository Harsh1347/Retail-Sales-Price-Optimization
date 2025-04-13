# Price Elasticity Analysis and Sales Optimization in Retail

## 📘 Project Context

This project was developed as part of the course **CSCI-B565: Data Mining** (Fall 2024) at **Indiana University Bloomington**.

This project aims to enhance pricing strategies in retail through a detailed analysis of historical transaction data. By estimating price elasticity and applying optimization techniques, it provides data-driven price recommendations to maximize revenue and profitability.

## 🧠 Project Objective

To develop a price recommendation system that:
- Calculates demand elasticity for individual products.
- Identifies optimal price points for revenue and profit maximization.
- Implements constraints to ensure realistic and actionable pricing recommendations.

## 📊 Dataset

The dataset represents sales and inventory records for a fictional retail toy chain, **Maven Toys**, operating in Mexico. It includes:
- Daily transaction logs.
- Product-level pricing.
- Store locations and inventory.
- Derived fields like revenue, profit, and expected gains.

Additional datasets were constructed to introduce dynamic pricing and enable elasticity calculations.

## 🧪 Methods & Techniques

### 1. **Exploratory Data Analysis (EDA)**
- Data validation (nulls, duplicates, outliers).
- Identified top-selling, profitable, and high-revenue items.
- Time series trends and seasonality analysis.

### 2. **Price Elasticity Estimation**
- Used linear and log-log regression models to estimate elasticity.
- Clustered products by store, city, or region to capture varying demand behavior.
- Elasticity formula used:
  \[
  \text{Elasticity} = \frac{\%\text{ change in quantity demanded}}{\%\text{ change in price}}
  \]
  Log-log model:
  \[
  \ln(Q) = \beta_0 + \beta_1 \ln(P) + \epsilon
  \]

### 3. **Revenue & Profit Optimization**
- Developed Python optimization script based on elasticity.
- Enforced constraints:
  - Price increase only (≤ 10% or $0.50).
  - Prices end in `.x5` or `.x9`.
  - Max 1% unit sales reduction allowed.
- Returned either new optimized price or 0 change if conditions unmet.

## 💡 Key Results

- Most products were inelastic (elasticity ≈ -0.001), allowing for safe price increases.
- Revenue gains were significant for high-volume items even with minor price bumps.
- Example:
  - *Magic Sand*: $0.50 price increase → $545 revenue boost with no unit sales drop.
  - *Splash Balls*: Moderately elastic; small price hike caused slight sales dip.

## 💻 User Interface

Developed a **Streamlit** application to:
- Input store-specific data.
- View top 5 items with optimal price recommendations.
- Download elasticity and revenue projections as CSV.

### Features:
- Select store, city, location.
- View real-time analysis.
- Export detailed recommendations.

## 🔭 Future Scope

- Integrate external factors (weather, demographics).
- Analyze competitor pricing for dynamic benchmarking.
- Extend model to include price reductions and seasonal promotions.
- Include inventory and product recommendation systems.

## 📚 References

1. [Understanding Price Elasticity](https://conjointly.com/guides/understanding-price-elasticity-of-demand/)
2. [Elasticity via ML](https://thedatageneralist.com/using-machine-learning-to-estimate-price-elasticity/)
3. [Profit Optimization with Newton's Method](https://towardsdatascience.com/optimization-newtons-method-profit-maximization-part-3-applied-profit-maximization-23a8c16167cd)
4. Research on Price Ending Effects and Consumer Behavior
5. [Maven Analytics - Retail Dataset](https://mavenanalytics.io/data-playground)
