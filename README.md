<h1 align="center">🛍️ Customer Shopping Behaviour Analysis</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
</p>

<p align="center">
  <strong>A comprehensive end-to-end data pipeline transforming raw retail data into actionable business intelligence.</strong>
</p>

<hr />

## 📖 Project Narrative
In today's retail landscape, understanding "who" is buying is as important as "what" they are buying. This project analyzes **3,900 customer records** [cite: 5] to solve a critical business challenge: identifying which demographics drive high-value revenue and how loyalty programs impact the bottom line[cite: 2].

---

## 🛠️ Detailed Technical Workflow

### 🐍 Phase I: Data Engineering (Python)
The first phase focused on preparing the raw dataset using `Pandas` to ensure data integrity[cite: 4].
<ul>
  <li><strong>Intelligent Imputation:</strong> I identified 37 missing values in <code>review_rating</code>[cite: 6]. Rather than using a global average, I calculated the <b>median rating per product category</b> to maintain contextual accuracy (e.g., a high-rated 'Clothing' item shouldn't be influenced by a low-rated 'Footwear' average)[cite: 7].</li>
  <li><strong>Feature Engineering:</strong> 
    <ul>
      <li><b>Age Segmentation:</b> Created four life stages (Young Adult, Adult, Middle-aged, Senior) to better visualize spending power[cite: 11].</li>
      <li><b>Quantitative Mapping:</b> Transformed text-based frequencies (e.g., "Weekly") into a numerical <code>purchase_frequency_days</code> column (7 days) for time-series potential[cite: 12].</li>
    </ul>
  </li>
  <li><strong>Database Optimization:</strong> Standardized column names to lowercase and underscores to ensure a seamless <code>SQLAlchemy</code> push to MySQL[cite: 9, 16].</li>
</ul>

### 🗄️ Phase II: SQL Relational Analytics
Data was migrated to a <code>customer_behaviour</code> database to perform complex relational querying[cite: 15, 16].
<ul>
  <li><strong>Advanced SQL Logic:</strong>
    <ul>
      <li><b>Window Functions:</b> Used <code>ROW_NUMBER()</code> with <code>PARTITION BY</code> to rank the Top 3 most-purchased products in every category[cite: 21, 251, 252].</li>
      <li><b>Conditional Aggregation:</b> Calculated the "Discount Rate" percentage for each product using <code>CASE WHEN</code> logic[cite: 244, 245].</li>
      <li><b>Customer Lifecycle:</b> Segmented the database into <i>New</i> (1 purchase), <i>Returning</i> (2-10), and <i>Loyal</i> (10+) to prioritize marketing efforts[cite: 23, 248].</li>
    </ul>
  </li>
</ul>

### 📊 Phase III: Business Intelligence (Power BI)
The final stage focused on executive-level visualization in <code>dashboard2.pbix</code>[cite: 25].
<ul>
  <li><strong>Revenue Analysis:</strong> Visualized revenue contribution by Age Group and Location to highlight the most profitable demographics[cite: 27].</li>
  <li><strong>Program Evaluation:</strong> Compared <i>Subscribers vs. Non-Subscribers</i> to quantify the financial impact of the loyalty program[cite: 28].</li>
  <li><strong>Strategy Metrics:</strong> Displayed Total Revenue, Average Order Value (AOV), and Customer Count as primary KPIs[cite: 26].</li>
</ul>

---

## 💡 Strategic Recommendations
<ul>
  <li><strong>Conversion Strategy:</strong> The data revealed a massive "Returning" segment[cite: 31]. Targeted email campaigns should focus on converting these into "Loyal" status to secure recurring revenue[cite: 32].</li>
  <li><strong>Logistics Upselling:</strong> Shipping type directly impacts spend[cite: 33]. Incentivizing "Express" shipping for high-value items can drive a higher AOV[cite: 33].</li>
  <li><strong>Inventory Prioritization:</strong> Focus stock allocation on the <i>Top 3 items per category</i> identified during SQL analysis to minimize storage costs while maximizing sales[cite: 34].</li>
</ul>

---

## 📂 Project Files
<pre>
├── Customerbehaviour.ipynb   # Full Python Data Engineering Script [cite: 4]
├── customer_queries.sql      # 10+ Advanced SQL Problem Solvings [cite: 231]
├── dashboard2.pbix           # Interactive Power BI Dashboard [cite: 25]
└── Project_Report.pdf        # Detailed Documentation
</pre>

<hr />

<p align="center">
  <b>Gaurav Yadav</b> | BSc Computer Science Student | Aspiring Data Analyst
</p>
