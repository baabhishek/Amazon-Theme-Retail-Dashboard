# Amazon-Theme-Retail-Dashboard
Conduct a thorough examination of Amazon's garment segment, encompassing sales data, revenue streams, and unit sales.

In an ever-evolving retail landscape, understanding the dynamics of the garment segment is crucial for stakeholders seeking to optimize their business strategies. This project aims to leverage Power BI analytics to delve into the performance of Amazon's garment segment, unraveling key insights into sales trends, revenue generation, and the strategic positioning of the online retail giant in the garment industry.

Objectives:

Comprehensive Analysis: Conduct a thorough examination of Amazon's garment segment, encompassing sales data, revenue streams, and unit sales.
Data-driven Insights: Utilize Data Analysis Expressions (DAX) to extract meaningful insights from raw data, enabling stakeholders to make informed decisions.
Visual Representation: Design visually captivating dashboards inspired by the Amazon website theme, facilitating intuitive data exploration and interpretation.
Product Overview: Present a high-level overview of the garment segment's performance, highlighting key metrics and trends to provide stakeholders with actionable insights.
Product Details: Delve deeper into product-level details, unveiling the performance of individual garments and identifying top-performing products.
Online Business Measurement: Evaluate the online positioning of Amazon's garment segment by analyzing sales performance across different channels and assessing the growth trajectory of online sales.
Stakeholder Empowerment: Empower stakeholders, including executives, marketers, and sales teams, with actionable insights derived from the Power BI analysis, enabling them to formulate effective business strategies.
Methodology:

Data Source: The information is sourced from Data.World.
Data Cleaning and Preparation: Employ robust data cleaning techniques to ensure data accuracy and consistency, preparing the dataset for analysis.
Data Modeling: Utilize DAX to create calculated columns and measures, facilitating advanced data modelling and manipulation for insightful analysis.
Dashboard Design: Design visually stunning dashboards with a user-friendly interface, incorporating intuitive navigation and interactive features to enhance the user experience.
Analysis and Visualization: Conduct an in-depth analysis of the garment segment's performance, leveraging powerful visualization tools to present key insights compellingly.
Iterative Refinement: Continuously iterate on the dashboard design and analytical approach based on stakeholder feedback and evolving business requirements.
DAX Queries Used:

Total Sales Calculation:
DAX
Copy code
Total Sales = SUM(Sales[Amount])
Total Units Sold:
DAX
Copy code
Total Units Sold = SUM(Sales[Units])
Average Revenue Per Unit:
DAX
Copy code
Average Revenue Per Unit = DIVIDE([Total Sales], [Total Units Sold])
Yearly Sales Growth:
DAX
Copy code
Yearly Sales Growth = 
CALCULATE(
    SUM(Sales[Amount]),
    DATESYTD(Sales[Date])
) - 
CALCULATE(
    SUM(Sales[Amount]),
    DATESYTD(Sales[Date], SAMEPERIODLASTYEAR(Sales[Date]))
)
Top Selling Products:
DAX
Copy code
Top Selling Products = 
TOPN(
    10,
    SUMMARIZE(
        Sales,
        Products[ProductName],
        "Total Sales", SUM(Sales[Amount])
    ),
    [Total Sales], DESC
)
Uploading Project to Power BI:

Data Preparation in Excel:

Organize the data in Excel with relevant columns such as Date, Product Name, Units Sold, Sales Amount, etc.
Clean the data to remove any inconsistencies or errors.
Uploading Data to Power BI:

Open Power BI Desktop.
Click on "Get Data" and choose "Excel".
Select your Excel file and load the data into Power BI.
Data Modeling:

Create relationships between different tables (e.g., Sales, Products) in the "Model" view.
Use DAX to create calculated columns and measures for analysis.
Designing the Dashboard:

In the "Report" view, use visualizations like bar charts, line charts, and tables to present data.
Apply filters and slicers to enable interactive data exploration.
Customize the design to align with the Amazon website theme for a cohesive look.
Publishing the Dashboard:

Once the dashboard is ready, click on "Publish" and select your workspace in the Power BI service.
Share the link to the live Power BI dashboard with stakeholders.
Deliverables:

Interactive Power BI Dashboard: A dynamic and visually engaging dashboard showcasing the performance of Amazon's garment segment, equipped with interactive features for data exploration.
Comprehensive Analysis Report: A detailed report outlining the findings of the Power BI analysis, accompanied by actionable insights and recommendations for stakeholders.
Presentation: An engaging presentation highlighting key insights and trends uncovered during the analysis, tailored for executive stakeholders and decision-makers.
Conclusion:

By leveraging the power of Power BI analytics, this project endeavors to provide stakeholders with invaluable insights into Amazon's garment segment, enabling them to make data-driven decisions and stay ahead in the competitive retail landscape. This dashboard ensures to provide valuable insights into the Amazon garment segment's performance and positioning in the retail industry.

<img width="600" alt="amazon" src="https://github.com/baabhishek/Amazon-Theme-Retail-Dashboard/assets/165395155/08de5926-5452-4d48-8cbb-58af4a0d56ba">


Here is the live dashboard link to access:
https://app.powerbi.com/view?r=eyJrIjoiNjBlZjU4YTktNmM3My00NzIxLThkYWQtODI4ZTM1NjJiNzZkIiwidCI6IjViNDYyNjIyLWI0ZDktNDk5OC05NGQ1LWNiMWJjMTljN2Y5NiJ9&pageName=ReportSection
