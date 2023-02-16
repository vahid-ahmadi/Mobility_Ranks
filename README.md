# Mobility_Ranks

consider I have a data set which has columns:
1. county id (counties are in US)
2. county names
3. GEO data of the center of counties
4. average of "mobility" variable in each county: average
5. standard deviation of "mobility" variable in each county: see


Create a column called "group". write data's group number in this column. I want to group data. with this mechanism:
1. put the first data (first row) as the first group
2. consider data i
3. for data i check these two conditions between data i and every data j (j is all data: j<i) (start j from 1 to i-1):
a. if GEO distance between two data i and j less than a threshold called DIST.
b. average_i - average_j / sqrt(se_i^2 - se_j^2) < 1.96
4. check these two conditions and if it can pass both of these two conditions, mark group of data j for for data i. create a column called "group". write data's group number in this column
5. do it from data number 2 to all data

code is available in First_Attempt
