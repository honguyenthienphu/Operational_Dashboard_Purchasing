# [Power BI] Explore Ecommerce Dataset - Purchasing Dashboard
<h2>I. Introduction</h1>
<p>In this project, I made a Purchasing Operation Dashboard for market visual, helping manager make better decisions and operations.</p>
<p>The dataset is based on the AdventureWorks database supports standard online transaction processing scenarios for a fictitious bicycle manufacturer - Adventure Works Cycles</p>
<p>My primary objective is to assess the dataset and create a dashboard that help team Purchasing Make Order enough for sales, on time and with optimal price</p>
<h2>II. Requirements</h2>
<ul>
  <li>Design Thinking</li>
  <li>Power BI</li>
  <li>Cleaning Data</li>
  <li>Visualization</li>
</ul>
<h2>III. Data Access</h2>
<h3>Tables:</h3>
<table>
  <tr>
    <th>No</th>
    <th>Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Calendar</td>
    <td>Dim Date table</td>
  </tr>  
  <tr>
    <td>2</td>
    <td>Measures_Tables</td>
    <td>Measures table for Purchasing metrics</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Product</td>
    <td>Products sold or used in the manfacturing of sold products</td>
  </tr>  
  <tr>
    <td>4</td>
    <td>ProductInventory</td>
    <td>Product inventory information</td>
  </tr>
  <tr>
    <td>5</td>
    <td>ProductTable</td>
    <td>Product detailed information</td>
  </tr>
  <tr>
    <td>6</td>
    <td>ProductVendor</td>
    <td>Cross-reference table mapping vendors with the products they supply</td>
  </tr>
  <tr>
    <td>7</td>
    <td>PurchaseOrderDetail</td>
    <td>Individual products associated with a specific purchase order</td>
  </tr>
  <tr>
    <td>8</td>
    <td>Purchasing.PurchaseOrderHeader</td>
    <td>General purchase order information</td>
  </tr>
  <tr>
    <td>9</td>
    <td>ShipMethod</td>
    <td>Shipping company lookup table</td>
  </tr>
  <tr>
    <td>10</td>
    <td>Vendor</td>
    <td>Companies from whom Adventure Works Cycles purchases parts or other goods</td>
  </tr>
</table>
<h3>Design Thinking: 5W1H</h3>
<ul>
  <li>What: Description of the procurement plan (raw materials, finished goods, and semi-finished products) to meet the production schedule at optimal costs and within a reasonable timeframe</li>
  <li>Who: Head of Supply Chain use the dashboard to make decision</li>
  <li>When & Where: In the meeting between Supply Chain team and Production team</li>
  <li>Why: Review the procurement plan to balance the money flow with the production schedule.</li>
  <li>How: Understand the production schedule and requirements from the production team to develop an optimal procurement plan</li>
</ul>
<h3>Empathy Map</h3>
<img src="https://github.com/user-attachments/assets/8df53bae-8aed-42be-aec1-18e8ea87e490" alt="Empathy Map" style="width: 100%;">

<h2>III. Insights</h2>
<h3>Project Model</h3>
<p>Inventory management has two models to determine the reorder point:</p>
<ul>
  <li>MTS - Make To Stock: A production and inventory management strategy where goods are manufactured and stocked in advance based on anticipated customer demand</li>
  <li>MTO - Make To Order: A production strategy where products are manufactured only after receiving a customer's order</li>
</ul>
<p>&rarr; Choose Make to Stock model for the fixed model in this Project</p>
<h3>Metrics need to measure</h3>
<p>1. Safety Stock & Reorder Point</p>
<ul>
  <li>Determine the SKUs need to order base on Safety Stock Level and Reorder Point</li>
  <li>When quantity reach Reorder Point: Need to place order base on standard leadtime</li>
  <li>When quantity reach Safety Stock Level: Need a rush order to fulfil the requirements</li>
</ul>
<p>2. Order Quantity</p>
<ul>
  <li>Calculation Orde Quantity based on demand</li>
  <li>Safety Stock and Reorder Point have already been determined for each item in this case, the required order quantity only needs to exceed the Safety Stock</li>
</ul>
<p>3. Fulfilment Rate</p>
<ul>
  <li>Fulfilment Rate = Completed Order / Total Orders</li>
  <li>Fill rate, also called order fulfillment rate, is the percentage of orders that can ship from vendor's available stock without any lost sales, backorders, or stockouts</li>
</ul>
<p>4. Rejected Rate</p>
<ul>
  <li>Rejected Rate = Rejected Quantity / Ordered Quantity</li>
  <li>Rejected Rate means the ratio of total defected number of units to total number of units delivered to company</li>
</ul>

<h2>IV. Dashboard</h2>
<h3>1. Overview</h3>
<p><b>Description: </b>Provides an overview of purchasing status including Total PO, Purchased Vendor, Purchased Cost, Fulfilment Rate</p>
<p><b>Purpose: </b>To inform stakeholders about the current purchased metrics, indentify the purchased cost, which category is the most highest value and cost. Which category has the highest Rejected Rate</p>
<p><b>Key Metrics:</b></p>
<ul>
  <li>Purchased Cost: The total cost for all purchased orders (total debt)</li>
  <li>Fulfilment Rate: The current ratio of order fill in total</li>
  <li>Rejected Rate: The ratio of total defected number of units to total number of units delivered to company</li>
</ul>
<img src="https://github.com/user-attachments/assets/a37d9bdb-a113-46d3-abdd-d3231599e0b6" alt="Overview" style="width: 100%;">
<h3>2. Inventory</h3>
<p><b>Description: </b>Provides an overview of inventory, including inventory quantity, inventory value for purchasing and production, and product classification</p>
<p><b>Purpose: </b>To inform stakeholders about the current inventory status, identify shortages of materials, understand how value is allocated, and determine inventory locations</p>
<p><b>Key Metrics:</b></p>
<ul>
  <li>Inventory Cost: The total current inventory value in stock</li>
  <li>Reorder Point: The threshold at which new orders need to be placed</li>
  <li>Safety Stock: The minimum level of inventory to prevent stockouts</li>
</ul>
<img src="https://github.com/user-attachments/assets/5a8cffe0-2af9-4bc8-9d5e-12771341ee24" alt="Inventory" style="width: 100%;">

<h3>3. Vendors</h3>
<p><b>Description: </b>Provides an overview of vendor information, including vendor classification, credit rating, total cost (total debt), ontime delivery rate, preferred vendor or not</p>
<p><b>Purpose: </b>To propose improvements from suppliers to enhance the purchasing strategy (such as managing long-term debt or reducing material costs) and to identify suppliers with lower product prices</p>
<p><b>Key Metrics:</b></p>
<ul>
  <li>Credit Rating: Supplier credit rating based on accounts payable</li>
  <li>Total Due: The total current outstanding debt</li>
  <li>Lead Time: The time from placing an order to delivery</li>
</ul>
<img src="https://github.com/user-attachments/assets/6fb53508-7824-40ed-8411-b32a1360f1ad" alt="Vendors" style="width: 100%;">

<h3>4. Products</h3>
<p><b>Description: </b>Provides an overview of product information, including rejected rate, unit price, lead time, minimum order quantity (MOQ), price, etc</p>
<p><b>Purpose: </b>To propose improvements from product. Classify product majority and also compare the price for specific product among multiple vendors</p>
<p><b>Key Metrics:</b></p>
<ul>
  <li>ABC Class: ABC classification is a ranking system for identifying and grouping SKUs in terms of how useful they are for achieving inventory goals<li>
  <li>Standard Price/Last Receipt Cost: The base price of the product or the cost of the most recent receipt</li>
  <li>MOQ (Minimum Order Quantity): The minimum quantity that must be ordered from the supplier</li>
</ul>
<img src="https://github.com/user-attachments/assets/8d3b7deb-466a-46d1-a94f-2107f3f0afd7" alt="Products" style="width: 100%;">

<h3>5. Recommendations</h3>
<p><b>Description: </b>Provides advice for purchasing improvements in purchasing process base on metrics in previous dashboard</p>
<img src="https://github.com/user-attachments/assets/dc9a754e-1190-4f45-8dbe-339d7f3e25ec" alt="Recommendations" style="width: 100%;">
