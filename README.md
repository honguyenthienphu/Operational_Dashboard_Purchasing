# [Power BI] Explore Ecommerce Dataset
<h2>I. Introduction</h1>
<p>In this project, I made a Operation Dashboard for market visual, helping manager make better decisions and operations.</p>
<p>The dataset is based on the AdventureWorks database supports standard online transaction processing scenarios for a fictitious bicycle manufacturer - Adventure Works Cycles</p>
<p>My primary objective is to assess the dataset and create a dashboard that help team Purchasing Make Order enough for sales, on time and with optimal price</p>
<h2>II. Requirements</h2>
<ul>
  <li>Design Thinking</li>
  <li>Power BI</li>
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
    <td>Purchasing.ProductVendor</td>
    <td>Cross-reference table mapping vendors with the products they supply</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Purchasing.PurchaseOrderDetail</td>
    <td>Individual products associated with a specific purchase order</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Purchasing.PurchaseOrderHeader</td>
    <td>General purchase order information</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Purchasing.ShipMethod</td>
    <td>Shipping company lookup table</td>
  </tr>
  <tr>
    <td>5</td>
    <td>Purchasing.Vendor</td>
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
<img src="https://github.com/user-attachments/assets/95e96afa-01c6-4541-b23a-9318f00df6bb" alt="Query 4" style="width: 100%;">

<h2>III. Insights</h2>
<h3>Project Model</h3>
<p>Inventory management has two models to determine the reorder point:</p>
<ul>
  <li>MTS - Make To Stock: A production and inventory management strategy where goods are manufactured and stocked in advance based on anticipated customer demand</li>
  <li>MTO - Make To Order: A production strategy where products are manufactured only after receiving a customer's order</li>
</ul>
<p>&rarr; Choose Make to Stock model for the fixed model in this Project</p>
<h3>Metrics need to measure</h3>
<p>1. Reorder index</p>
<ul>
  <li>Calculate base on Safety Stock Level and Reorder Point</li>
  <li>Reorder index = Safety Stock / Reorder Point</li>
    <li> >1: Need to reorder</li>
    <li> =1: Need to order</li>
    <li> <1: Need a rush order</li>
</ul>
<p>2. Order Quantity</p>
<ul>
  <li>Calculation Orde Quantity based on demand</li>
  <li>Safety Stock and Reorder Point have already been determined for each item in this case, the required order quantity only needs to exceed the Safety Stock</li>
</ul>

<h2>IV. Dashboard</h2>
<h3>1. Inventory</h3>
<p><b>Description: </b>Provides an overview of inventory, including inventory quantity, inventory value, the number of SKUs for purchasing and production, and product classification</p>
<p><b>Purpose: </b>To inform stakeholders about the current inventory status, identify shortages of materials, understand how value is allocated, and determine inventory locations</p>
<p><b>Key Metrics:</b></p>
<ul>
  <li>Stock Ratio: The inventory ratio of SKUs</li>
  <li>Reorder Point: The threshold at which new orders need to be placed</li>
  <li>Safety Stock: The minimum level of inventory to prevent stockouts</li>
  <li>Reorder Index: An indicator assessing the urgency of placing new orders</li>
</ul>
<img src="https://github.com/user-attachments/assets/0a6d68eb-263a-43ab-a280-8c41796d699c" alt="Query 4" style="width: 100%;">

<h3>2. Purchasing</h3>
<p><b>Description: </b>Provides an overview of the purchasing team's activities, including the number of Purchase Orders (POs), order value, and accounts payable</p>
<p><b>Purpose: </b>To inform stakeholders about the order value and outstanding debts to suppliers. Additionally, it provides insights into the lead time for materials</p>
<p><b>Key Metrics:</b></p>
<ul>
  <li>PO Amount: The value of purchase orders</li>
  <li>Total Due: The total current outstanding debt</li>
  <li>Lead Time: The time from placing an order to delivery</li>
</ul>
<img src="https://github.com/user-attachments/assets/bac00c20-e356-4103-b245-0e2a19618b2a" alt="Query 4" style="width: 100%;">

<h3>3. Product & Supplier</h3>
<p><b>Description: </b>Provides an overview of supplier and product information, including lead time, minimum order quantity (MOQ), price, etc</p>
<p><b>Purpose: </b>To propose improvements from suppliers to enhance the purchasing strategy (such as managing long-term debt or reducing material costs) and to identify suppliers with lower product prices</p>
<p><b>Key Metrics:</b></p>
<ul>
  <li>Credit Rating: Supplier credit rating based on accounts payable</li>
  <li>Standard Price/Last Receipt Cost: The base price of the product or the cost of the most recent receipt</li>
  <li>MOQ (Minimum Order Quantity): The minimum quantity that must be ordered from the supplier</li>
</ul>
<img src="https://github.com/user-attachments/assets/7d81e8b3-ba24-4f67-9e3d-b75f4f61e4cd" alt="Query 4" style="width: 100%;">
