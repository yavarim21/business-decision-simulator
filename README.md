# business-decision-simulator

# **Business Decision & Profitability Simulator**

**Project Overview:**
Simulates business decisions for an online retail store, analyzing how changes in **price, cost, demand, currency, and inflation** affect **profit and risk**. The project uses **scenario-based analysis** and **Monte Carlo simulation** to model outcomes and provide **actionable insights** for data-driven pricing and inventory decisions.

---

## **Business Problem**

Retail managers need to make decisions under uncertainty:

* What happens to profit if prices increase or decrease?
* How does demand fluctuation impact revenue?
* Which products are most profitable with minimal risk?
* How do costs, inflation, or currency changes affect profitability?

This project answers these questions by modeling **profit and risk** under different scenarios.

---

## **Dataset**

* **Source:** Kaggle Online Retail Dataset
* **Key columns used:**

  * `InvoiceNo` – transaction ID
  * `StockCode` – product ID
  * `Quantity` – number of items sold
  * `UnitPrice` – sale price
* **Columns ignored in calculations:** `CustomerID`, `Description` (nulls retained to preserve data)

---

## **Data Cleaning & Outlier Handling**

* **Negative rows:** Removed rows with negative Quantity or UnitPrice (returns or errors).
* **Outlier detection:** Checked for extreme Quantity and UnitPrice values using **IQR and boxplots**.
* **Handling outliers:** Extreme values were either capped or removed to ensure realistic profit calculations.
* **Nulls:** CustomerID and Description nulls were retained to keep as much sales data as possible.

---

## **Cost & Profit Calculation**

* **Cost per unit:** 60% of UnitPrice (adjustable assumption)
* **Profit per unit:** UnitPrice − Cost
* **Total Profit:** Profit per unit × Quantity
* **Total Cost (optional):** Cost × Quantity

This provides the foundation for **scenario modeling and risk analysis**.

---

## **Scenario Analysis**

* Built multiple scenarios (Base, Optimistic, Pessimistic) by varying **price, cost, and demand**.
* Example:

| Scenario    | Price | Cost | Demand |
| ----------- | ----- | ---- | ------ |
| Base        | 0%    | 0%   | 0%     |
| Optimistic  | +5%   | -3%  | +10%   |
| Pessimistic | -5%   | +5%  | -15%   |

* Calculated **profit and revenue** under each scenario to identify **best- and worst-case outcomes**.

---

## **Risk Analysis**

* Applied **Monte Carlo simulation** to model uncertainty in **price and demand**.
* Generated a **distribution of profits** to assess:

  * Probability of loss
  * Worst-case / best-case profit
* Supports **data-driven decision-making under uncertainty**.

---

## **Key Insights**

* Identifies **top profitable products** with minimal risk.
* Shows **impact of price and demand changes** on total profit.
* Provides **actionable recommendations** for inventory, pricing, and cost strategies.

---

## **Visualizations & Dashboards**

* Profit by scenario (bar chart)
* Risk distribution (histogram)
* Product-level profitability table
* Optional: Interactive dashboards in **Power BI or Tableau**

---

## **How to Use**

1. Open the **Python notebooks** for step-by-step analysis.
2. Adjust **cost assumptions or scenario parameters** as needed.
3. Run the notebooks to generate **profit, risk, and insights**.
4. Optional: Open the dashboard files to explore visual insights interactively.




