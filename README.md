# cdg_interview_assignment

# Assignment 1

## Tasks

**[ ]** Write pseudo-code illustrating key operations

**[ ]** Produce a standardised company lookup table structure:

| uid | Name | country | state | City | Address | Telephone | url |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [generate one yourself] | Cleaned / standardized | Letters code or full name | [If applicable] | Cleaned / standardized | Cleaned / standardized | +[country]-[phone] | www.[url] |

Company related columns include the name, address, and contact details available for: shipper, consignee, forward company, notify company, also notify company, export name, booking contact and si contact.

## Steps

i. Review data and assess general structure

ii. Clean data, separate into distinct columns and rows where possible

iii. Retrieve *company related columns* and sort data accordingly

iv. create output *.xlsx* file

## Notes

## Questions

# Assignment 2

## Tasks

**[99]** Merge/aggregate: Combine the monthly and yearly datasets to a folder named “aggregate” in one CSV for each country each year.

**[99]** Remove duplicates: The dataset should not contain any duplicates.

**[99]** Retain as much data as possible: There should be no data lost while aggregating. For example, if the monthly data has 2 more columns than the same country’s yearly data, these two columns should be added to the final aggregated table. The same goes for any extra rows that might appear in either dataset.

**[99]** Format:
  a. Sort the data by a sailing date (column name: “Sailing DT”).
  b. Column names in the final dataset should be lowercase, and spaces replaced with “_” (underscore), e.g., “Sailing DT'' should be formatted to “sailing_dt.”
  c. Trim leading and trailing spaces, remove double spaces and tabs, and replace line breaks (if they exist) with a delimiter such as <br>.

## Steps

**[DONE]** i. load dataframes from monthly and yearly folders

**[DONE]** ii. check structures of dataframes, note differences in columns, clean data

**[DONE]** iii. merge dataframes

**[DONE]** iv. reformat column names

**[DONE]** v. investigate no. of unique values, remove duplicates in data

**[DONE]** vi. sort by 'sailing_dt', separate by country then separate by year
 
**[DONE]** vii. create output

**[ ]** viii. validate using unit tests for various edge cases

## Issues

**[FIXED]** os.walk detecting notebook checkpoints | move working directory

**[FIXED]** dataframe columns are not the same; some values have been added and/or moved | accounted for in merging process

**[FIXED]** two columns of 'export_name' and other columns also | use *pd.concat* instead of append

**[FIXED]** not all duplicates accounted for | use *b/l_no* for unique id

**[FIXED]** information regarding month/year (folder) which data was recorded missing | add month value when reading data

**[FIXED]** information regarding country (folder) | add country value when reading data

**[ ]** method to check if data has been lost; need to create some sort of method to compare with original data

## Notes

- monthly total rows = 6211, yearly total rows = 6341

- b/l_no 5313 unique values, booking_no 4891 unique values

- initial duplicates detected: 2691

- duplicates by subset *b/l_no*: 4548

- largest amount of unique values in column: b/l_no, 5313; use as row id

- *.xlsx* dataframe differences: added{' ORG EQ OFC', ' DEL EQ OFC', 'Forward Code ', ' Trunk POL', '  Trunk POD'}, moved{'Export Name'}

- dataframe differences with *monthly* and *yearly*: del_eq_ofc, forward_code, org_eq_ofc
 
- booking_no = AAR304421200, AAR204421200; have identical values for all values except booking_no, b/l_no

## Questions

- Which column is the id?

- Is the yearly folder for data obtained only for 1 year? 

- (follow=up) Regarding 'for each country each year', does that mean they are separated by certain years, e.g., is it determined by *sailing_dt*?

- How thorough should the unit tests be?

## Unit Tests & Edge Cases

**[ ]** column data has mismatched data types

**[ ]** certain columns have incorrect data types

**[ ]** missing important values: sailing_dt, country

