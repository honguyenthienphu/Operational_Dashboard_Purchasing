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
<h3>Value need to measure</h3>
