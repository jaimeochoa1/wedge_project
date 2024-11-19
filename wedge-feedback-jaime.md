## Feedback 

Again, you really don't want data in your repos. 

I'm not seeing your `submission.md` as I initiallly look at your repo. Please fill that in or point me to it. Your README write-up is excellent, however. 

I was expecting to see code notebooks or files for each task. I'm going to assume they're all in `wedge_project.ipynb`, but let me know if I'm missing anything. 

Generally this looks good. You'll need to do a revision, but the changes are minor. 

### Task 1

* Put all of your imports in the first cell. You have `import os` written 9 times in this notebook. Pandas gets imported 7 times. This makes it look like you don't know how importing works. 
* It's more typical to do one table per file. That way if anything goes wrong the "damage" is contained. But putting everything in a single table is also fine. 
* Some comments would be good around `check_data` and `get_owner_records`. It's not clear to me how this fits in with the flow. 

### Task 2

Lines like this only go in .py files that you want to call from the command line or load as modules: 

```
if __name__ == "__main__":
    owners = get_owner_records()
```

I'm mildly surprised this worked as written: 

```
    query = f"""
    SELECT *
    FROM `umt-msba.wedge_project_ochoa.transactions`
    WHERE card_no IN {owner_ids}
    """
```
When I did this I had to put the parentheses around the card numbers. Myabe your `tuple` trick above does it? The results look correct. 

It looks like this sample is only 88 MB, not 250 MB as required, so when you re-submit the `submission.md` file, play around with the size of your sample to get 

### Task 3

You have errors in the queries on this task. Here's what you have for the second query: 

```
    SELECT
        card_no,
        EXTRACT(YEAR FROM DATETIME(datetime)) AS year,
        EXTRACT(MONTH FROM DATETIME(datetime)) AS month,
        SUM(total) AS total_sales,  -- Using 'total' column as the total sales amount
        COUNT(trans_no) AS transactions,
        SUM(quantity) AS items
    FROM `umt-msba.wedge_project_ochoa.transactions`
    WHERE card_no != 3
    GROUP BY card_no, year, month
    ORDER BY card_no, year, month
```

Compare this to my solution, which is built on the work we did in Intro to SQL: 
```
                   SELECT card_no,
                   EXTRACT(YEAR from datetime) as year,
                   EXTRACT(MONTH from datetime) as month,
                   ROUND(SUM(total),2) AS sales,
                   COUNT(distinct(
                      CONCAT(CAST(EXTRACT(DATE from datetime) AS STRING),
                             CAST(register_no AS STRING),
                             CAST(emp_no AS STRING),
                             CAST(trans_no AS STRING)))) as transactions,
                   SUM(CASE WHEN (trans_status = 'V' or trans_status = 'R') THEN -1 ELSE 1 END) as items
                   FROM `umt-msba.wedge_transactions.transArchive_*`
                     WHERE department != 0 and
                          department != 15 and
                         (trans_status IS NULL or 
                          trans_status = ' ' or 
                          trans_status = 'V' or 
                          trans_status = 'R') 
                    GROUP BY card_no, year, month
                    ORDER BY card_no, year, month    
```

Everything else looks very efficient, other than the unneeded `__name__ == "__main__"` stuff. 
