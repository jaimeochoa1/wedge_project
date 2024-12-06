Task 1: Data Upload to BigQuery

Description: Imported transactional data from local CSV files into a Google BigQuery table umt-msba.wedge_project_ochoa.transactions.

Approach: Utilized pandas and pandas_gbq to read CSV files and upload them.
Verified the successful data import by executing queries on sample records.

Results: Data successfully loaded into BigQuery with a total of approximately 85 million rows across all files.


Task 2: Sample Generation

Description: Extracted a 250MB sample of transactional records for owners (excluding card_no = 3) and saved it as a tab-delimited file.

Approach: Adjusted the sample size until the target file size was achieved.
The final sample contains 1,454,891 records and is hosted in Google Drive due to GitHub's file size limit.

Results: [Download sampled_owners_250MB.txt](https://drive.google.com/file/d/1u9yqHtiYTzSKQQbPErYPoHtsHtvSlx7P/view?usp=sharing)


Task 3: Summary Tables and SQLite Database

Description: Generated summary tables and saved them in BigQuery:
- `sales-by-date-by-hour-table`: Aggregates total sales, transactions, and item counts grouped by date and hour.
- `sales_by_owner_by_year_by_month_table`: Provides a breakdown of sales and activity by owner, year, and month.
- `sales_by_product_by_year_by_month-table`: Tracks sales metrics by product, year, and month.


Approach: Queried BigQuery to aggregate data for the summary tables. Results were saved as tables in the BigQuery dataset (`umt-msba.wedge_project_ochoa`) for ease of access and further analysis.

Results:
sales-by-date-by-hour-table: Aggregates total sales, transactions, and item counts grouped by date and hour. Stored in umt-msba.wedge_project_ochoa.sales-by-date-by-hour-table.

Observations: The sales_by_date_by_hour table contains 39,421 rows, representing the aggregation of sales data by date and hour for the entire time period covered in the dataset. The earliest date in the dataset is January 1, 2010, and the latest is January 31, 2017. This confirms that the table spans the expected date range and provides hourly granularity for each day.

Validation Notes:
Total Rows: The table contains 39,421 rows, which matches expectations based on the 7-year time frame and hourly aggregation.
Date Range: Data spans from 2010-01-01 to 2017-01-31, confirming complete temporal coverage.

Completeness: No apparent gaps in the date range, ensuring a continuous record of hourly sales activity.

Results:
sales_by_owner_by_year_by_month_table: Provides a breakdown of sales and activity by owner, year, and month. Stored in umt-msba.wedge_project_ochoa.sales_by_owner_by_year_by_month_table.

Observations: The spot check for the sales_by_owner_by_year_by_month_table yielded 808,896 total rows, spanning from January 1, 2010, to January 1, 2017. This aligns with the expected duration of the dataset, covering the entire transactional history up to the end of the Wedge Project's analysis timeframe. The large number of rows suggests a comprehensive breakdown of sales and activity grouped by owner, year, and month, as intended by the query structure.

Validation Notes: 
Row Count: The high row count confirms the successful aggregation of data at the specified granularity (owner, year, month). Each row represents a unique combination of these dimensions.

Date Range: The start_date and end_date match the timeframe of the Wedge Project data, indicating no missing periods.

Query Accuracy: The use of PARSE_DATE to derive dates from year and month ensures correct validation of the date range. All observations fall within the expected limits, validating the integrity of the table creation process.

Results:
sales_by_product_by_year_by_month-table: Tracks sales metrics by product, year, and month. Stored in umt-msba.wedge_project_ochoa.sales_by_product_by_year_by_month-table.

Observations: Row Count: The table contains a total of 1,269,425 rows, indicating a detailed breakdown of product sales metrics across years and months.

Date Range: The data spans from 2010-01-01 to 2017-01-01, which aligns with the expected dataset time frame.

Validation Notes:
The total row count and date range are consistent with the expectations for this summary table.
The summarized product sales data is accurate, with correct detail level and relevant metrics.

Additional Notes: The SQLite database has been compressed and split due to size limitations.

Download links for the split files:
wedge_summary.zip.part01 (https://drive.google.com/file/d/1wy557d7A6Gzhff8oIzFgedPl0jpT5QwK/view?usp=sharing)
wedge_summary.zip.part02 (https://drive.google.com/file/d/1-DAveXT3lhrCMPQ7LPdboRnGTUF1-ysb/view?usp=sharing)
wedge_summary.zip.part03 (https://drive.google.com/file/d/11-piXYr8YjEqo0lrRIwJ-gQEzJ9R7trL/view?usp=sharing)

File Structure

Jupyter Notebook: Contains all code and documentation for tasks.
wedge_project.ipynb

SQLite Database: Stored as a compressed zip file, available via Google Drive links.

Sample File: Hosted on Google Drive for download.

Instructions for Reviewers
Clone the repository:
bash
Copy code
git clone https://github.com/jaimeochoa1/wedge_project.git

Review the Jupyter notebook for code and results.
Download the SQLite database and sample file from the provided links.
Unzip the SQLite database and open it using your preferred SQLite client.

Challenges and Solutions

GitHub File Size Limit: Large files exceeded the 100MB limit. 
As a solution: Hosted the 250MB sample on Google Drive.

Compressed the SQLite database and split it into parts.
Dynamic Sample Sizing: Used Python to dynamically adjust sample size until the target size was achieved.

Additional Notes
Please reach out with any questions or issues accessing the files.



