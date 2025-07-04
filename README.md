The goal of the project is to build pricing models that dynamically adjust parking fees in urban areas based on demand, traffic, occupancy, and other contextual factors. It includes:
•	A Baseline Linear Model
•	A Demand-Based Pricing Model
•	Optionally a Competitive Pricing Model
•	Visualization using Bokeh
________________________________________
2. Model 1: Baseline Linear Pricing
•	A simple model where price increases linearly with occupancy ratio.
•	alpha is a sensitivity factor (default = 0.1).
•	Example: If the parking lot is full, the price goes up from its base.
________________________________________
3. Model 2: Demand-Based Pricing
🔹 Demand Calculation
•	Demand is a weighted combination of:
o	Occupancy ratio (most important)
o	Queue length
o	Traffic condition (negative effect)
o	Whether it's a special day
o	Type of vehicle (e.g., truck vs. bike)
🔹 Dynamic Pricing Based on Demand
•	Adjusts base price using demand and elasticity factor lambda_.
•	Prices are clipped to within 50% to 200% of base price for fairness.
________________________________________
 Visualization with Bokeh
from bokeh.plotting import figure, show, output_notebook
•	Creates a line chart of demand_price over LastUpdatedTime using Bokeh.
•	This helps visualize how pricing varies dynamically with time.
