### Supply Chain Analytics Report
<hr>

##### Objective: 
Given the datasets on Inventory, Warehouse, Orders, and Shipments, develop a report highlighting key insights
<br>
<br>
##### Data Overview: 
Data consists of 3 CSV files.

-  fulfillment: warehouse order fulfillment days corresponding to product name (ID).
-  inventory: warehouse inventory and cost per unit for each product
-  orders_and_shipments: A record of every order with columns like OrderID, Product Category, Customer details, etc.

#### Report:
We consider the following important metrics along with reasonings and definitions of the logic behind their calculation

- *Product Risk Category*: Each product has a per unit cost for storage in the warehouse and a per unit profit associated with it. We consider the average cost of storage against the average profit
  - **High Risk**: If the average cost is greater than the median cost AND the average profit is less than the median profit. This indicates the product is costing more than usual and generating less profit than usual, which is risky.

  - **Monitor**: If the average cost is greater than the median cost BUT the average profit is greater than or equal to the median profit. This suggests the product is costing more, but it’s still generating sufficient profit, so it should be monitored.

  - **Review**: If the average cost is less than or equal to the median cost BUT the average profit is less than the median profit. This indicates the product is costing less but not generating enough profit, so it needs review.

  - **Optimal**: If none of the above conditions are met, the product is considered optimal. This means the product is costing less than or equal to the median cost and generating profit greater than or equal to the median profit.
- *Sales and Profit over time*: Added a line chart to visualize sales and profit over time with an inbuilt drill-down to see annual, quarterly, and monthly trends
- *Stock Status*: Calculated whether a product is overstocked or understocked by comparing the warehouse inventory with the order quantity.  It’s useful for inventory management and ensuring optimal stock levels.
- *Average shipment days vs order quantities*: We observe the lowest shipment time when the order quantity is 3
- *Map Visual*: Displays orders corresponding to customer country. Helps identify trends, patterns, or outliers in data that are tied to specific locations
- *Profit by Product Category*: Gives us the categories that contribute the most to profit shares. We see that Cleats are the most profitable product. 

