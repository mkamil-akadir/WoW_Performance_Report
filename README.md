> **Disclaimer**: This project was developed for work purposes, and due to confidentiality requirements, no actual data or proprietary details can be shared. However, please feel free to connect with me if you're interested in learning more about the process or discussing similar projects.


# Power BI Reporting Pipeline for Project Performance Insights

This project aims to create a Power BI report that provides stakeholders with actionable insights on project performance metrics, enabling data-driven decision-making. The report includes analyses of current week performance, week-over-week comparisons, and delta calculations over various timeframes (e.g., previous week, past six weeks, and past six months) against client-set targets for each metric.

## Project Introduction

To effectively design this report, I collaborated closely with key stakeholders to define the objectives, target audience, and data requirements. This initial preparation involved discussions with stakeholders to understand their decision-making needs, the performance indicators most critical to their goals, and the specific timeframes and metrics they use to gauge success. This alignment helped ensure that the report would be both relevant and insightful for its intended audience.

## Project Objective

The main objective of this project is to aggregate and process data from multiple sources, standardize and clean the data through ETL steps in Power Query, and build a comprehensive report in Power BI. This report enables stakeholders to make informed decisions based on real-time project performance data, supporting metrics such as:

- **Current week performance**: Overview of key metrics from the latest reporting period.
- **Week-over-week performance**: Comparison of key metrics from the current week to the previous week.
- **Delta Analysis**: Insights into performance changes over different timeframes (e.g., previous week, 6 weeks, 6 months) and against client-defined targets for each metric.

## Workflow

1. **Data Extraction**:
   - **AWS S3 & Athena**: Utilize Athena to query and extract utilization and AHT data stored on AWS S3.
   - **Tableau**: Download additional reports in table format directly from Tableau.
   
2. **Data Transformation (ETL with Power Query)**:
   - **Template Standardization**: Since each metric report has a different structure, Power Query is used to select only relevant columns and standardize them across datasets.
   - **Data Cleaning and Lookup Table Integration**:
     - A global lookup table provides mappings for project, market, and role names, which are used to harmonize the data.
     - M Language scripts in Power Query streamline transformations, making the process more dynamic and adaptable to changes.
   
3. **Data Storage and Organization**:
   - All processed CSV files are stored in a **SharePoint** directory, ensuring a centralized location for organized data.

4. **Power BI Data Processing**:
   - **Data Import**: Import processed data from SharePoint into Power BI.
   - **Data Modeling**: Establish relationships between tables in Power BI, and add a custom **calendar table** that follows a Saturday-to-Friday week-ending format, per organizational standards.
   
5. **Report Building**:
   - Create visualizations that offer insights into current week performance, week-over-week changes, and delta analysis over specified timeframes.
   - Configure metrics against client-set targets to highlight variances and performance gaps.

## Challenges Faced

- **Different Metric Templates**: Each metric report has a unique template, requiring selective column extraction and standardization during the ETL process.
- **Manual Data Extraction**: Data retrieval from various sources is largely manual, adding time to the process and potential for error.

## What I Learned

- **Process Optimization with Power Query**: Leveraging Power Query and M Language has allowed me to create a more dynamic ETL pipeline, significantly reducing manual adjustments.
- **Business Acumen and Communication**: Working closely with stakeholders to align on report objectives, audience needs, and data interpretation has improved my understanding of business requirements and enhanced the report’s relevance for decision-making.

## Tools and Technologies Used

- **AWS S3 & Athena**: For storage and querying of source data.
- **Tableau**: Serves as a source for additional reports.
- **Power Query**: Main ETL tool for data cleaning, merging, and transformation.
- **SharePoint**: Repository for processed CSV reports and lookup tables.
- **Power BI**: Reporting tool used for data modeling, relationships, and creating final dashboards.

## Advantages of this Pipeline

- **Streamlined Reporting**: Aggregates multiple sources into one report, reducing time and effort in data retrieval.
- **Dynamic ETL Process**: Power Query and M Language scripts make data transformations adaptable, reducing manual intervention.
- **Audience-Aligned Insights**: Focuses on metrics and timeframes crucial for stakeholders, providing actionable insights.
- **Scheduled Refresh in Power BI**: Enabled schedule refreshes in Power BI for real-time data updates from SharePoint.

## Usage Instructions

1. **Set Up Connections**:
   - Connect to AWS S3 via Athena to access source data.
   - Download necessary Tableau reports and save them as CSV files.
   
2. **Run ETL in Power Query**:
   - Use Power Query to select relevant columns, clean data, and apply lookup table mappings.
   
3. **Save Processed Data**:
   - Export transformed data to the SharePoint folder.
   
4. **Import to Power BI**:
   - Load all saved CSV files from SharePoint into Power BI.
   - Set up relationships, import the calendar table, and apply transformations for metric-specific insights.

## Future Enhancements

- **Automate Tableau Data Extraction**: Investigate options to automate the data extraction process from Tableau to reduce manual effort.


