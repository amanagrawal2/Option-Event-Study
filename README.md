# Options event study - Extended

## Common stock:
# _crsp.ipynb_
 - Downloaded the whole CRSP Database for the period of 2013-17
 - Imported the CSV 
 - Dropped the column "Unnamed: 0"
 - Renamed the column "date" to "DataDate"
 - Converted the "DataDate"s to Datetime
 - Created a list of unique PERMCOs in the crsp file
 - Split the Dataframe into smaller Datarames based upon PERMCO using a for loop
 - Sorted the rows according to the DataDate
 - Dropped the rows with NaN values in the column "PRC" and "TICKER"
 - Reset the index
 - If the Dataframe has some data in it then export the dataframe to a csv with the file name as "{first ticker of that dataframe}_crsp.csv".
 - Note that the filename is just used as a reference for the user and not the code.
