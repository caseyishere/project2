# Medical and Medicaid DIfferences from 2015-2018 in California

This public data set was created by the Centers for Medicare &amp; Medicaid Services that summarizes counts of enrollees who are dually-eligible for both Medicare and Medicaid program, including those in Medicare Savings Programs. This project utilizes public data from the American Community Survey (ACS) by the U.S. Census Bureau for unemployment figures, and the Centers for Medicare & Medicaid Services (CMS) Dual Eligible Enrollment dataset for healthcare enrollment statistics. This project explores the relationship between changes in county-level unemployment and changes in dual eligible (Medicare/Medicaid) enrollment in California from 2015 to 2018. Understanding this connection can inform public health and economic policy initiatives. A query was created to visualize the correlation between dual eligible and unemployed individuals between 2015 and 2018. I chose to analyze this data set because it is important to understand the relationship between economic indicators like unemployment and healthcare program enrollment for vulnerable populations as we can inform policy decisions regarding social safety nets and healthcare access.

I did not use any queries to clean for duplicates, blanks/nulls and trimms as this data is already clean. I just want to showcase how I can visualize healthcare data in California and make a correlation about it.  

## Files 

- 2015_to_2018_CA_enrollments.csv - Dual enrollments data
- unemployedchange_15_18.csv - Unemployment Change Data

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

These where the results. Kern county had the biggest difference in dual enrollment with over 2,000 new enrollees. 
<img width="1042" alt="Dual_18_15_results" src="https://github.com/user-attachments/assets/b3a3fc25-ff9a-43d6-8330-5b7f0128a5fd" />

The second query : 
<img width="985" alt="uneployed change sql " src="https://github.com/user-attachments/assets/1da6b072-dc7e-4dd2-9b93-b9007cbc62f4" />
<img width="981" alt="unemplyed changed sqll" src="https://github.com/user-attachments/assets/c2b02176-4815-4110-87c5-460d78a794bb" />
<img width="973" alt="unemployed change sqql" src="https://github.com/user-attachments/assets/d404616a-b50c-46fb-a2e5-c398cc0ebc4b" />
This query answers the second question. The unemployed_change and duals_change CTEs(Common Table Expression) are calculating u_change and total_duals_diff. ACS stands for American Community Survey. 

<img width="993" alt="Unemployment_results" src="https://github.com/user-attachments/assets/7e6bda45-1b12-4342-bffc-2a665f456a0c" />

The results showcase the unemployment change and the increase in new enrollees that occured between 2015 and 2018.

## Tableau Dashboard

[View the interactive dashboard on Tableau Public!](https://public.tableau.com/views/MedicalandMedicaidDifferences/MedicalandMedicaidDifferences)
<img width="1440" alt="County_name_filter" src="https://github.com/user-attachments/assets/faf39d33-765f-49ea-842c-a96c268272f2" />

To filter a county, click on a county name under the county name filter on the right side of the page. 


## Conclusion

Kern country had the highest increase in dual-eligible enrollments. With an increase in employed individuals, an increase in dual enrollments occur. 

To look at my visuals in Tableau click on this link : https://public.tableau.com/app/profile/casey.lemos/viz/MedicalandMedicaidDifferences/MedicalandMedicaidDifferences



