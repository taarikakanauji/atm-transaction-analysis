# ATM Transaction Analysis - Power BI Report 

![Power BI Report](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/Power-BI-Report.jpg)

## Problem Statement

Stakeholders across various departments currently lack a centralized, data-driven view to effectively monitor and analyze ATM performance across different banks, locations, time periods, and transaction types. This data gap makes it difficult to identify underperforming ATMs, evaluate financial and non-financial transaction volumes, and make informed decisions based on critical indicators such as total transactions, revenue, operational costs, uptime, and profitability metrics. There is a clear need for an interactive dashboard that provides actionable insights across key operational and financial dimensions.

The dashboard delivers data-driven insights to uncover transaction trends, identify cost and revenue leakages, optimize ATM deployment and maintenance strategies, and maximize operational efficiency and profitability. It empowers key stakeholders with an interactive view to monitor financial health, assess historical and current margin ranges, track revenue performance, and make data-backed decisions with a clear understanding of cost drivers and transaction dynamics.

This dashboard enables stakeholders to track and analyze ATM performance and profitability based on parameters such as:

- Bank, ATM ID, State

- Time Frame (Year, Month, Quarter)

- ATM Type and Category

- Transaction Metrics: Financial Txns, Non-Financial Txns, Monthly Txn Volume

- Revenue Metrics: Monthly Revenue, MHA Revenue, CRA Contributions, Total ATM Revenue

- Cost Metrics: Spare Replacements, Site Maintenance, FLM, Supplies, AMC (ATM/UPS/VSAT), Rent, Utilities, Insurance, and Total Cost

- Profitability Metrics: Gross Profit, Gross Profit %, Margin Ranges

- Performance Metrics: Uptime, Revenue Performance, Compensation, and Penalties 


# Objective

`Centralize ATM Transaction Data`
Develop a unified dashboard that consolidates ATM data across banks, states, and time periods to provide a single source of truth for performance monitoring.

`Track and Analyze Transaction Volumes`
Enable stakeholders to monitor financial and non-financial transaction trends, identify high- and low-performing ATMs, and assess monthly and daily averages.

`Evaluate Revenue and Cost Drivers`
Provide insights into revenue streams (e.g., CRA, MHA Revenue) and detailed cost components (e.g., AMC, spare parts, site maintenance) to understand net profitability.

`Measure Operational Efficiency and Profitability`
Calculate and visualize gross profit margins, margin ranges (current and historical), and uptime to assess ATM effectiveness and return on investment.

`Enable Data-Driven Decision Making`
Deliver actionable insights that support strategic decisions related to ATM placement, maintenance planning, cost optimization, and revenue improvement initiatives.

## Key Questions

    Q : What is the average number of financial and non-financial transactions per ATM per month or per day?

    Q : Which states or regions generate the highest and lowest revenues from ATMs?

    Q : Which ATMs are underperforming in terms of transaction volume and profitability?

    Q : How much are we spending on maintenance, rent, and other services per ATM?

    Q : What is the average daily transaction count per ATM?

    Q : What is the bifurcation between financial and non-financial transactions for

    Q : What are the total and average expenditure costs for E-Bills, penalties and AMCs? 

    Q : How are the ATMs performing in terms of ranges for revenue.  

## Steps followed 

As a Business Analyst for a leading bank, I was responsible for creating an interactive ATM Transactions Analysis Dashboard to support stakeholders in tracking ATM performance, transaction trends, and overall operational activity across multiple banks and locations. The objective was to deliver actionable insights that would help optimize ATM deployment, enhance operational efficiency, improve profitability, and support strategic decision-making. Below is my step-by-step approach to designing this dashboard in Power BI:


- Step 1 : Upload all csv data files in mySQL work bench. After that, connect it with the Power BI platform using Connector by giving mySQL workbench credentials. Lastly, select the tables from the mySQL database.

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".

- Step 4 : After a thorough review and cleanup, we now have a data which contains no errors or empty values across columns — indicating a high-quality dataset ready for transformation and visualization.

- Step 5 : In the report view, under the view tab, default theme was selected.

- Step 6 : Creating KPI Cards for Key Metrics - To provide stakeholders with a clear summary, I created four KPI cards displaying high-level engagement indicators as shown below. These KPIs offer a real-time snapshot of audience interaction and help in making data-driven decisions quickly and effectively.

        Total Financial Transaction – Number of financial transactions.

        Total Non-Financial Transactions - Number of non-financial transactions.

        Total Cost - The total cost incurred.

        Average Monthly Revenue – The average monthly revenue.

        Gross Profit Percentage – The gross profit percentage.

   I formatted these KPI cards with currency symbols to make trends more visually intuitive. This allows executives to quickly grasp key performance indicators at a glance, without needing to explore detailed data.

  ![KPI](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/kpi.jpg)

           
- Step 7 : Representing cost analysis bifurcated by ATM Cost and Maintainence – I added a custom donut chart to showcase the ATM cost and maintenance costs division spanning different months.

        Fields Used:

        Values: CRA, ATM AMC, Spare Rep., Site Maint., UPS AMC, ATM AMC, VSAT AMC.


   The chart revealed that the highest expenses came from three areas namely: CRA, Spare Rep., and ATM AMC. All the other cost areas were less than half of these, indicating good control over those areas.

  ![Cost Analysis](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/cost-analysis.jpg)

- Step 8 : Representing ATM, MHA and Monthly revenue by states  – I used a bar chart to display the ATM, MHA and monthly revenues across different states for an overall revenue perspective. 

        Fields used:

        Y-Axis: ATM Revenue, MHA Revenue, Monthly Revenue

        X-axis: State

   The chart revealed that multiple states including Tripura, Nagaland, Meghalaya and Mizoram each contributed to near equal revenues in the respective categories. The leader state was Assam, driving the highest revenues in all categories while Sikkim reported the lowest reveues. This also suggests that the low sized states have reported lower revenues compared to the larger ones. The striking statistic was the drastic lower levels of MHA revenues in comparison to the ATM and Monthly revenues.

  ![ATM MHA Monthly Revenue](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/atm-mha-monthly-revenue.jpg)


- Step 9 : Representing monthly financial and non-financial transactions trends – I added a bar chart to depict the number of financial and non-financial transactions during the months of the year 2024, highlighting patterns in platform usage over time. 

        Fields used:

        Y-Axis: Financial Txn, Non Financial Txn

        X-Axis: Month-Year (Mar-24, Aug-24, Nov-24, Dec-24)

  The chart revealed that financial transactions were the main area of interest for the customers in comparison to non-financial transactions.  This insight helps identify optimal days for content release and user interaction strategies.

  ![Monthly Financial vs Non-Financial](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/Monthly-fin-non-fin.jpg)

- Step 10 : Monthly Transactions - This line chart provides a visual representation of transaction volume trends across four specific months in 2024.

        Fields used:

        X-axis: Month-Year (Mar-24, Aug-24, Nov-24, Dec-24)

        Y-axis : Monthly Transaction

  The chart shows that the highest number of monthly transactions occurred in March 2024, reaching over 16 million. This was followed by a steady decline through August and November, dipping below 15 million. In December 2024, transactions slightly rebounded to just above 15 million, indicating a mild recovery at year-end..    

  ![Monthly Transactions](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/monhly-Txn.jpg)


- Step 11 : Adding Filters to the Dashboard – To enhance user experience, I incorporated five slicers that let users filter the data based on their preferences. These slicers can be easily accessed through a filter icon positioned at the top of the dashboard.

Setting Up Slicers for Interactive Filtering – I configured slicers to allow users to interactively navigate the report and concentrate on specific areas of interest. These dynamic filters enable users to drill down into key dimensions for more focused analysis.

  I added slicers for:

  `ATM Type`

  `State`

  `ATM id`

  I chose dropdown-style slicers for a clean interface, ensuring they influence all report visuals. This allows business teams to filter data—for example, comparing the transaction frequencies in terms of various scenarios. 

 ![Filter Pane](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/filter-pane.jpg)

- Step 12 : To enhance the usability and interactivity of the Power BI report, I added a Reset Filters icon that allows users to quickly clear all slicer selections and return the report to its original default view. This feature increases user confidence by making it easy to undo any filter changes, offering more flexibility and a smoother user experience.

First, I inserted a reset or refresh icon using the Insert > Image option and placed it to the left of the filter icon for better visibility and easy access.

Next, I manually cleared all slicer selections, including ATM Type, State, and ATM ID.

Finally, I enabled the Action feature on the reset icon by setting the Type to Bookmark and linking it to the Clear all Filters bookmark. This configuration ensures that clicking the icon resets all slicers and filters to their default (unselected) state.
  

# **ATM Transactions Detail Analysis**  

Detail ATM Txn page, designed for additional ATM transaction analysis, focuses on highlighting critical revenue figures, trends, and transaction ranges. Its primary objective is to provide insights into what’s performing well and what isn’t—across both financial and non-financial transactions. These insights serve as a valuable foundation for making informed, strategic decisions that will drive the bank’s continued growth and success.

  ![Power BI Report D](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/Power-BI-Report-D.jpg)

The KPI Metrics section provides a quick snapshot of the business’s performance through key indicators. These include: Average E-Bill, Average Penalty, Average VSAT AMC, Average CRA, and Average Uptime—offering a concise view of the operational health.

The Range Analysis section displays the overall distribution of ATMs across various revenue ranges, with the ability to filter by selected month. This offers a high-level overview of ATM performance based on revenue brackets.

The Detailed Analysis section presents a tabular breakdown of essential metrics such as Monthly Revenue, E-Bill, Penalty, VSAT AMC, CRA, and Average Uptime—all categorized by revenue performance ranges. While transaction volumes are crucial, tracking expenditures is equally important. This table can also be filtered by ATM Type for more granular insights.

**Insights**

States show variation in ATM revenue , uptime and High penalties and CRA values are clustered in certain regions

Some ATMs report 0% uptime, indicating critical service gaps

ATMs with high e-bill but low revenue need performance review

Majority of ATMs (2,137) are in Above 30% margin and Over 1,200 ATMs had 200+ transactions, indicating high usage

**Challenges**

Low Uptime: Certain ATMs have extremely low uptime, directly affecting customer service.

Penalty Costs: Some locations face high penalties due to SLA breaches or service delays.

Disproportionate CRA Costs: CRA appears to dominate operational cost in several ATMs.

Underperforming Locations: ATMs with revenue and low usage indicate underutilization.

**Recommendation**

Investigate ATMs with low uptime and initiate urgent maintenance or replacement.

Optimize CRA Contracts: Focus on renegotiating or centralizing cash handling services.

Phase Out Underperformers: Review low-revenue ATMs for relocation or closure.

Boost High-Margin ATM Support: Invest in ATMs showing >30% margins for better ROI.

# Snapshot of Report (Power BI Service)

  ![Power Service Full 1](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/Power-Service-Full-1.jpg)

  

# Report Snapshot (Power BI DESKTOP)

  ![Power BI Report Full 1](https://github.com/taarikakanauji/atm-transaction-analysis/raw/main/images/Power-BI-Report-Full-1.jpg)


# **Project Resources: ATM Transactions Analysis**  

### **Detailed Report (PDF)**  
[Insights of ATM Transactions Analysis](https://github.com/taarikakanauji/atm-transaction-analysis/blob/main/Insights%20for%20ATM%20Transaction.pdf)  

### **Power BI Desktop Demo**  
[Power BI Demo (MKV)](https://github.com/taarikakanauji/atm-transaction-analysis/blob/main/Power-BI-Demo.mkv)  

### **Power BI Service Demo**  
[Power BI Service Demo (MKV)](https://github.com/taarikakanauji/atm-transaction-analysis/blob/main/Power-Service-Demo.mkv)  

### **Dataset Folder**  
[Dataset Files](https://github.com/taarikakanauji/atm-transaction-analysis/tree/main/dataset)  

### **PBIP Files**  
- **Report:** [Report Files](https://github.com/taarikakanauji/atm-transaction-analysis/tree/main/ATM%20Transaction%20Analysis.Report)  
- **Semantic Model:** [Semantic Model Files](https://github.com/taarikakanauji/atm-transaction-analysis/tree/main/ATM%20Transaction%20Analysis.SemanticModel)  
- **Project File:** [ATM Transactions Analysis PBIP](https://github.com/taarikakanauji/atm-transaction-analysis/blob/main/ATM%20Transaction%20Analysis.pbip)  
- **Gitignore:** [.gitignore](https://github.com/taarikakanauji/atm-transaction-analysis/blob/main/.gitignore)  

### **Project README (Setup Guide)**  
[README.md](https://github.com/taarikakanauji/atm-transaction-analysis/blob/main/README.md)  

# Conclusion

This ATM Transaction Analysis dashboard empowers stakeholders to:

- Uncover key revenue patterns and trends across various ATM types, locations, and transaction types (both financial and non-financial).

- Identify high- and low-performing ATMs based on revenue ranges and operational metrics such as E-Bill, Penalty, VSAT AMC, CRA, and Uptime.

- Monitor key performance indicators in real time to ensure operational efficiency and cost-effectiveness.

- Leverage interactive slicers and filters for targeted insights by ATM Type, State, and ATM ID, enhancing decision-making granularity.

By leveraging these insights, resources can be strategically allocated to high-performing ATMs, while underperforming locations can be addressed with targeted actions. The ability to reset filters and drill down into detailed metrics ensures a user-friendly experience and supports data-driven decisions. Ultimately, this dashboard serves as a powerful tool for monitoring performance, optimizing costs, and driving the bank’s growth and operational excellence in the ATM network.


