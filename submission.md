# Applied Data Analytics

## Wedge Project

This project involved processing and analyzing transactional data from the Wedge Co-op. Tasks included importing data into Google BigQuery, generating a sample dataset for owners, and creating summary tables stored in BigQuery. The results were validated for accuracy and completeness.

### Task 1: Data Upload to BigQuery

Description: Imported transactional data from local CSV files into a Google BigQuery table umt-msba.wedge_project_ochoa.transactions.

* Files for this task: 
transArchive_201001_201003_clean.csv: Contains active transactional data from January to March 2010, formatted and cleaned for BigQuery.

transArchive_201004_201006_clean.csv: Contains active transactional data from April to June 2010, formatted and cleaned for BigQuery.

transArchive_201007_201009_clean.csv: Contains active transactional data from July to September 2010, formatted and cleaned for BigQuery.

transArchive_201010_201012_clean.csv: Contains active transactional data from October to December 2010, formatted and cleaned for BigQuery.

transArchive_201101_201103_clean.csv: Contains active transactional data from January to March 2011, formatted and cleaned for BigQuery.

transArchive_201104_clean.csv: Contains active transactional data for April 2011, formatted and cleaned for BigQuery.

transArchive_201105_clean.csv: Contains active transactional data for May 2011, formatted and cleaned for BigQuery.

transArchive_201106_clean.csv: Contains active transactional data for June 2011, formatted and cleaned for BigQuery.

transArchive_201107_201109_clean.csv: Contains active transactional data from July to September 2011, formatted and cleaned for BigQuery.

transArchive_201110_201112_clean.csv: Contains active transactional data from October to December 2011, formatted and cleaned for BigQuery.

transArchive_201201_201203_clean.csv: Contains active transactional data from January to March 2012, formatted and cleaned for BigQuery.

transArchive_201201_201203_inactive_clean.csv: Contains inactive transactional data from January to March 2012, formatted and cleaned for BigQuery.

transArchive_201204_201206_clean.csv: Contains active transactional data from April to June 2012, formatted and cleaned for BigQuery.

transArchive_201204_201206_inactive_clean.csv: Contains inactive transactional data from April to June 2012, formatted and cleaned for BigQuery.

transArchive_201207_201209_clean.csv: Contains active transactional data from July to September 2012, formatted and cleaned for BigQuery.

transArchive_201207_201209_inactive_clean.csv: Contains inactive transactional data from July to September 2012, formatted and cleaned for BigQuery.

transArchive_201210_201212_clean.csv: Contains active transactional data from October to December 2012, formatted and cleaned for BigQuery.

transArchive_201210_201212_inactive_clean.csv: Contains inactive transactional data from October to December 2012, formatted and cleaned for BigQuery.

transArchive_201301_201303_clean.csv: Contains active transactional data from January to March 2013, formatted and cleaned for BigQuery.

transArchive_201301_201303_inactive_clean.csv: Contains inactive transactional data from January to March 2013, formatted and cleaned for BigQuery.

transArchive_201304_201306_clean.csv: Contains active transactional data from April to June 2013, formatted and cleaned for BigQuery.

transArchive_201304_201306_inactive_clean.csv: Contains inactive transactional data from April to June 2013, formatted and cleaned for BigQuery.

transArchive_201307_201309_clean.csv: Contains active transactional data from July to September 2013, formatted and cleaned for BigQuery.

transArchive_201307_201309_inactive_clean.csv: Contains inactive transactional data from July to September 2013, formatted and cleaned for BigQuery.

transArchive_201310_201312_clean.csv: Contains active transactional data from October to December 2013, formatted and cleaned for BigQuery.

transArchive_201310_201312_inactive_clean.csv: Contains inactive transactional data from October to December 2013, formatted and cleaned for BigQuery.

transArchive_201401_201403_clean.csv: Contains active transactional data from January to March 2014, formatted and cleaned for BigQuery.

transArchive_201401_201403_inactive_clean.csv: Contains inactive transactional data from January to March 2014, formatted and cleaned for BigQuery.

transArchive_201404_201406_clean.csv: Contains active transactional data from April to June 2014, formatted and cleaned for BigQuery.

transArchive_201404_201406_inactive_clean.csv: Contains inactive transactional data from April to June 2014, formatted and cleaned for BigQuery.

transArchive_201407_201409_clean.csv: Contains active transactional data from July to September 2014, formatted and cleaned for BigQuery.

transArchive_201407_201409_inactive_clean.csv: Contains inactive transactional data from July to September 2014, formatted and cleaned for BigQuery.

transArchive_201410_201412_clean.csv: Contains active transactional data from October to December 2014, formatted and cleaned for BigQuery.

transArchive_201410_201412_inactive_clean.csv: Contains inactive transactional data from October to December 2014, formatted and cleaned for BigQuery.

transArchive_201501_201503_clean.csv: Contains active transactional data from January to March 2015, formatted and cleaned for BigQuery.

transArchive_201504_201506_clean.csv: Contains active transactional data from April to June 2015, formatted and cleaned for BigQuery.

transArchive_201507_201509_clean.csv: Contains active transactional data from July to September 2015, formatted and cleaned for BigQuery.

transArchive_201510_clean.csv: Contains active transactional data for October 2015, formatted and cleaned for BigQuery.

transArchive_201511_clean.csv: Contains active transactional data for November 2015, formatted and cleaned for BigQuery.

transArchive_201512_clean.csv: Contains active transactional data for December 2015, formatted and cleaned for BigQuery.

transArchive_201601_clean.csv: Contains active transactional data for January 2016, formatted and cleaned for BigQuery.

transArchive_201602_clean.csv: Contains active transactional data for February 2016, formatted and cleaned for BigQuery.

transArchive_201603_clean.csv: Contains active transactional data for March 2016, formatted and cleaned for BigQuery.

transArchive_201604_clean.csv: Contains active transactional data for April 2016, formatted and cleaned for BigQuery.

transArchive_201605_clean.csv: Contains active transactional data for May 2016, formatted and cleaned for BigQuery.

transArchive_201606_clean.csv: Contains active transactional data for June 2016, formatted and cleaned for BigQuery.

transArchive_201607_clean.csv: Contains active transactional data for July 2016, formatted and cleaned for BigQuery.

transArchive_201608_clean.csv: Contains active transactional data for August 2016, formatted and cleaned for BigQuery.

transArchive_201609_clean.csv: Contains active transactional data for September 2016, formatted and cleaned for BigQuery.

transArchive_201610_clean.csv: Contains active transactional data for October 2016, formatted and cleaned for BigQuery.

transArchive_201611_clean.csv: Contains active transactional data for November 2016, formatted and cleaned for BigQuery.

transArchive_201612_clean.csv: Contains active transactional data for December 2016, formatted and cleaned for BigQuery.

transArchive_201701_clean.csv: Contains active transactional data for January 2017, formatted and cleaned for BigQuery.

Results: Data successfully loaded into BigQuery with a total of approximately 85 million rows across all files.


### Task 2: Sample Generation

Description: Extracted a 250MB sample of transactional records for owners (excluding card_no = 3) and saved it as a tab-delimited file.

Files for this task:
sampled_owners_250MB.txt: Contains a 250MB sample of transactional records for owners (excluding card_no = 3).

Results: [Download sampled_owners_250MB.txt](https://drive.google.com/file/d/1u9yqHtiYTzSKQQbPErYPoHtsHtvSlx7P/view?usp=sharing)


### Task 3: Summary Tables and SQLite Database

Files for this task:
wedge_summary.db: Contains the SQLite database with summary tables.
wedge_summary.zip: Compressed version of the SQLite database.
wedge_summary.zip.part01, wedge_summary.zip.part02, etc.: Split files of the ZIP archive (approximately 45 MB each) for easier upload and sharing.


Generated summary tables and saved them in BigQuery:
- `sales-by-date-by-hour-table`: Aggregates total sales, transactions, and item counts grouped by date and hour.
- `sales_by_owner_by_year_by_month_table`: Provides a breakdown of sales and activity by owner, year, and month.
- `sales_by_product_by_year_by_month-table`: Tracks sales metrics by product, year, and month.

Additional Notes: The SQLite database has been compressed and split due to size limitations.

Download links for the split files:
wedge_summary.zip.part01 (https://drive.google.com/file/d/1wy557d7A6Gzhff8oIzFgedPl0jpT5QwK/view?usp=sharing)
wedge_summary.zip.part02 (https://drive.google.com/file/d/1-DAveXT3lhrCMPQ7LPdboRnGTUF1-ysb/view?usp=sharing)
wedge_summary.zip.part03 (https://drive.google.com/file/d/11-piXYr8YjEqo0lrRIwJ-gQEzJ9R7trL/view?usp=sharing)

## Query Comparison Results

Fill in the following table with the results from the 
queries contained in `gbq_assessment_query.sql`. You only
need to fill in relative difference on the rows where it applies. 
When calculating relative difference, use the formula 
` (your_results - john_results)/john_results)`. 



|  Query  |  Your Results  |  John's Results | Difference | Rel. Diff | 
|---|---|---|---|---|
| Total Rows         | 85760139  |85760139   | 0  | 0  |
| January 2012 Rows  | 1070907   | 1070907   |  0 | 0   |
| October 2012 Rows  | 1042287   | 1042287   | 0  | 0  |
| Month with Fewest  |  Feb.     |  Feb.     | No  | NA  |
| Num Rows in Month with Fewest  |6556770    | 6556770| 0  |  0 |
| Month with Most    | May       |May        | No  | NA  |
| Num Rows in Month with Most  |7578372   | 7578372  |  0 |  0 |
| Null_TS  |7123792 | 7123792  |  0 | 0  |
| Null_DT  | 0  | 0  | 0  | 0  |
| Null_Local  | 234843|234843   | 0  | 0  |
| Null_CN  | 0  | 0  | 0  |  0 |
| Num 5 on High Volume Cards  | 14987|14987| No  | NA  |
|  Num Rows for Number 5 |460630|460630|  0 |0   |
| Num Rows for 18736  |12153 | 12153  | 0  | 0  |
| Product with Most Rows  |banana organic|banana organic| No  | NA  |
| Num Rows for that Product  | 908639  | 908639 | 0  |  0 |
| Product with Fourth-Most Rows  |avocado hass organic|avocado hass organic| No  | NA  |
| Num Rows for that Product  |456771 |456771| 0  | 0  |
| Num Single Record Products  | 2769  |  2769 | 0  | 0  |
| Year with Highest Portion of Owner Rows  | 2014  | 2014  | No  | NA |
| Fraction of Rows from Owners in that Year  | 0.7591 | 0.7591  | 0  | 0  |
| Year with Lowest Portion of Owner Rows  | 2011  | 2011  | No  | NA |
| Fraction of Rows from Owners in that Year  | 0.7372 |0.7372| 0  | 0  |

## Reflections

The Wedge Project was both challenging and rewarding. It took quite a long time to complete, but I feel that I’ve learned so much throughout the process. Initially, I wasn’t a big fan of Google BigQuery, just as Python was not my favorite tool when I started working with it last spring. However, with practice, these tools have become more familiar, and Python is now one of my favorites to use. Tackling programs outside my comfort zone has been a valuable learning experience.

One of the most satisfying moments was when something finally worked as intended—it made all the effort worth it. However, the data load process was by far the most frustrating part. It required hours of waiting, which was challenging for someone like me who lacks patience and juggles a busy work/life/school schedule. Despite these challenges, I’m grateful for the opportunity to work on this project and for the knowledge and skills I gained along the way.


## File Structure

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



