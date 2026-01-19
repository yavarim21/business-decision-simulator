# business-decision-simulator
Simulates business decisions for an online retail store, analyzing how price, cost, demand, currency, and inflation affect profit and risk. Uses scenario analysis and Monte Carlo simulation to model outcomes and provide actionable insights for data-driven pricing and inventory decisions

Data Cleaning & Outlier Handling

Removed negative Quantity and UnitPrice rows (returns or invalid data).

Checked for outliers in Quantity and UnitPrice using IQR and boxplots.

Capped or removed extreme values to ensure realistic profit and scenario modeling.

Null CustomerID and Description values were retained to preserve as much sales data as possible.
