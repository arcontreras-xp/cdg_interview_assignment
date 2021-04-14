# cdg_interview_assignment

# Tasks

**[50]** Merge/aggregate: Combine the monthly and yearly datasets to a folder named “aggregate” in one CSV for each country each year.

**[50]** Remove duplicates: The dataset should not contain any duplicates.

**[25]** Retain as much data as possible: There should be no data lost while aggregating. For example, if the monthly data has 2 more columns than the same country’s yearly data, these two columns should be added to the final aggregated table. The same goes for any extra rows that might appear in either dataset.

**[75]** Format:
  a. Sort the data by a sailing date (column name: “Sailing DT”).
  b. Column names in the final dataset should be lowercase, and spaces replaced with “_” (underscore), e.g., “Sailing DT'' should be formatted to “sailing_dt.”
  c. Trim leading and trailing spaces, remove double spaces and tabs, and replace line breaks (if they exist) with a delimiter such as <br>.

# Steps Taken

**[DONE]** i. load dataframes from monthly and yearly folders

**[DONE]** ii. check structures of dataframes, note differences in columns

**[DONE]** iii. merge dataframes

**[DONE]** iv. reformat column names

**[ ]** v. investigate no. of unique values, remove duplicates in data

**[ ]** vi. sort by 'sailing_dt', separate by country then separate by year
 
**[ ]** vii. create output

# Issues

**[FIXED]** os.walk detecting notebook checkpoints | move working directory

**[ ]** not all duplicates removed by *.drop_duplicates()*; 2691 duplicates removed

**[ ]** duplicates not detected; column '' has inconsistent data formats | reformat column

# Notes

- monthly total rows = 6211

- yearly total rows = 6341

- booking_no = AAR304421200, AAR204421200; have identical values for all values except booking_no, b/l_no


