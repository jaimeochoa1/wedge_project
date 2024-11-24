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

Description: Generated summary tables and saved them in an SQLite database:
The summary tables include Sales by Date and Hour, which aggregates total sales, transactions, and item counts grouped by date and hour. Additionally, Sales by Owner by Year and Month provides a breakdown of sales and activity by owner, year, and month. Finally, Sales by Product Description by Year and Month tracks key sales metrics by product, year, and month.

Approach: Queried BigQuery for aggregated data.
Stored results in an SQLite database (wedge_summary.db).

Results: SQLite database: Available as a zip file split into smaller parts for upload.

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



