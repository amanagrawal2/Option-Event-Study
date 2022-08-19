# **Options event study - Extended**

## Common stock:
### _crsp.ipynb_
 - Downloaded the whole CRSP Database for the period of 2013-17
 - Created an empty list for permco
 - Imported the CSV
 - Added unique permco to the empty list "permco"
 - Flattened the list of lists ("permco"). This is due to the fact that I am reading the large csv file in chunks becasue of memory constraints of hardware
 - Once I have a list of all the unique PERMCOs in the crsp file, I read the large crsp file again. This is due to the fact that I can only read the csv in chunks, thus can't load it as a variable. 
 - Cleaned the loaded chunk:
    - Dropped the column "Unnamed: 0"
    - Renamed the column "date" to "DataDate"
    - Converted the "DataDate"s to Datetime
 - Split the Dataframe into smaller Dataframes based upon PERMCO and only take the required columns
 - Exported the Dataframe to csv with filename : {permco}_crsp.csv
 
Note: Due to the nature of "chunk based csv reading", I am exporting these dataframes and then rereading the individual crsp file if there is more data to be added to it in a later chunk cycle of larger crsp file.
