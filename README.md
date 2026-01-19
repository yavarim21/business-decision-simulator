Here’s a **revised, polished version** of your README that’s slightly more concise, professional, and LinkedIn/GitHub friendly. I clarified some phrasing, improved flow, and emphasized outcomes and skills demonstrated:

---

# business-decision-simulator

# **Business Decision & Profitability Simulator**

**Project Overview:**
Simulates business decisions for an online retail store, analyzing how changes in **price, cost, demand, currency, and inflation** impact **profit and risk**. Utilizes **scenario-based analysis** and **Monte Carlo simulation** to model outcomes, providing **actionable insights** for data-driven pricing and inventory strategies.

---

## **Business Problem**

Retail managers face uncertainty and need answers to questions such as:

* How will profit change if prices rise or fall?
* How do demand fluctuations affect revenue?
* Which products maximize profit while minimizing risk?
* How do costs, inflation, or currency variations affect profitability?

This project addresses these questions by modeling **profit and risk under multiple scenarios**.

---

## **Dataset**

* **Source:** Kaggle Online Retail Dataset
* **Key columns used:**

  * `InvoiceNo` – transaction ID
  * `StockCode` – product ID
  * `Quantity` – number of items sold
  * `UnitPrice` – sale price
* **Columns ignored in calculations:** `CustomerID`, `Description` (nulls retained to preserve sales data integrity)

---

## **Data Cleaning & Outlier Handling**

* **Negative rows:** Removed negative Quantity or UnitPrice values (returns or data errors).
* **Outliers:** Checked for extreme Quantity and UnitPrice values using **IQR and boxplots**.
* **Handling outliers:** Extreme values capped or removed for realistic profit calculations.
* **Nulls:** Retained CustomerID and Description nulls to preserve as much sales data as possible.

---

## **Cost & Profit Calculation**

* **Cost per unit:** 60% of UnitPrice (adjustable assumption)
* **Profit per unit:** UnitPrice − Cost
* **Total Profit:** Profit per unit × Quantity
* **Total Cost (optional):** Cost × Quantity

This forms the foundation for **scenario modeling and risk analysis**.

---

## **Scenario Analysis**

* Created multiple scenarios (Base, Optimistic, Pessimistic) by adjusting **price, cost, and demand**:

| Scenario    | Price | Cost | Demand |
| ----------- | ----- | ---- | ------ |
| Base        | 0%    | 0%   | 0%     |
| Optimistic  | +5%   | -3%  | +10%   |
| Pessimistic | -5%   | +5%  | -15%   |

* Calculated **profit and revenue per scenario** to highlight best- and worst-case outcomes.

---

## **Risk Analysis**

* Applied **Monte Carlo simulation** to model uncertainty in **price and demand**.
* Generated a **distribution of total profit** to evaluate:

  * Probability of loss
  * Worst-case and best-case profit
* Enables **data-driven decisions under uncertainty**.

---

## **Key Insights**

* Identifies **top profitable products** with minimal risk.
* Shows **impact of price and demand changes** on total profit.
* Provides **actionable recommendations** for inventory, pricing, and cost strategies.

---

## **Visualizations & Dashboards**

* **Bar charts:** Profit by scenario per product
* **Histogram:** Profit distribution from Monte Carlo simulation
* **Tables:** Product-level profitability
* Optional: Interactive dashboards in **Power BI or Tableau**

---

## **How to Use**

1. Open the **Python notebooks** for step-by-step analysis.
2. Adjust **cost assumptions or scenario parameters** as needed.
3. Run notebooks to generate **profit, risk, and insights**.
4. Optionally, explore the dashboard files for **interactive visualizations**.

---

### **Skills Demonstrated**

Python, Pandas, NumPy, Matplotlib, Seaborn, Scenario Analysis, Monte Carlo Simulation, Data Cleaning, Outlier Handling, Data Visualization, Decision Analysis

