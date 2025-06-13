# Medical and Medicaid DIfferences from 2015-2018 in California

This public data set was created by the Centers for Medicare &amp; Medicaid Services that summarizes counts of enrollees who are dually-eligible for both Medicare and Medicaid program, including those in Medicare Savings Programs. A query was created to visualize the correlation between dual eligible and unemployed individuals between 2015 and 2018.

I did not use any queries to clean for duplicates, blanks/nulls and trimms as this data is already clean. I just wanted to showcase how I can visualize healthcare data in California. 

## Files 

2015_to_2018_CA_enrollments.csv - Dual enrollments data
unemployedchange_15_18.csv - Unemployment Change Data

## Tools Used
- BigQuery for SQL execution
- Tableau

## Author
[Casey Lemos](https://github.com/caseyishere)

### Questions to answer
1. In what counties in California has the number of dual-eligible individuals increased the most from 2015 to 2018?
2. How does the change in California for unemployed individuals from 2015-2018 correlate with the change in number of duals?

### Objective
Find the counties in California which have experienced the largest increase of dual enrollment households and compare how county-level dual enrollments have changed relative to unemployment.

### BigQuery SQL

<img width="1025" alt="Dual_enrollment_query_screenshot" src="https://github.com/user-attachments/assets/2ce2d49b-302f-4b20-ac85-d2e34fd61e17" />
<img width="1032" alt="Dual_enrollment_sc_18-22" src="https://github.com/user-attachments/assets/0c43d957-1e24-4417-b57e-c0b3c6b0c929" />

This query calculates the difference in dual enrollments from 12/01/18 and 12/01/15. The public totals is the number of total enrollees across all dual eligible programs. The FIPS is just the state code. 

These where the results: 
<img width="1042" alt="Dual_18_15_results" src="https://github.com/user-attachments/assets/b3a3fc25-ff9a-43d6-8330-5b7f0128a5fd" />

