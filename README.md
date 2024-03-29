# QlikLib
By [Zidmann](mailto:emmanuel.zidel@gmail.com) :bow:

## Description
Simple library of functions to use with Qlik project.

## How to use
In the QVW document, add these lines with vQliklibPath containing the path of the QlikLib library.

```bash
// Including the variables and the functions available in the QlikLib custom library
SET vQliklibPath='<directory>\QlikLib';
$(Must_Include='$(vQliklibPath)\core.qvs');
```

## Tests
The tests are launched in test/qliklibtest.qvw Qlik file which will load data from different sources (data1.csv, data2.csv, exempleSrc.txt).
Some functions have not been implemented yet in the tests :
- excel_worksheet_exist
- file_remove
- file_excel_sheet
- Building a string search function to catch some words from a list in a table

## Implemented functions

* console.qvs - Module containing all the console printing functions

| Name | Description |
| ---- | ---- |
| console_print | Print a message on the batch console |
| console_info | Print an information message in the specific format |
| console_sucess | Print a success message in the specific format |
| console_error | Print an error message in the specific format |
| console_jumpline | Jump a line in the console |
| console_delimitation | Printing a delimiter |


* log.qvs - Module containing all the log functions

| Name | Description |
| ---- | ---- |
| log_persist | Write in a file the content of the table dedicated to the log then purge the table |
| log_print | Log a message in the dedicated table and print it on the screen |
| log_info | Log an information message in the specific format |
| log_sucess | Log a success message in the specific format |
| log_error | Log an error message in the specific format |


* object.qvs - Module containing all the basic object management functions

| Name | Description |
| ---- | ---- |
| variable_exist | Check if a variable is defined in Qlik |
| file_exist | Check if a file exists at a specific path |
| table_exist | Check if a table exists |
| excel_worksheet_exist | Check if a worksheet exists in an Excel document |
| column_exist | Check if a column exists in a specific table |
| variable_fill | Set a default value to a variable in the case it is not defined |


* number.qvs - Module containing all the useful number functions

| Name | Description |
| ---- | ---- |
| number_pos | Return 0 if the number is positive or its value |
| number_neg | Return 0 if the number is negative or its value |
| number_sign | Return which sign has a number (0 is considered having no sign) |
| number_abs | Return the absolute value of a number |
| number_order | Return the order in the 10 base of a number |
| filesize_order | Return the appropriate order to use with a file size |
| filesize_unit | Return the appropriate unit to use with a file size |
| filesize_readable | Return the size of a file in a readable form |


* file.qvs - Module containing all the file management functions

| Name | Description |
| ---- | ---- |
| file_dirname | Extract the directory of a file |
| file_basename | Extract the basename of a file |
| file_extension | Extract the extension of a file |
| file_depth | Extract the depth of a file in a tree |
| file_dirname_unix | Extract the directory of a file in the case of a Unix path |
| file_basename_unix | Extract the basename of a file in the case of a Unix path |
| file_extension_unix | Extract the extension of a file in the case of a Unix path |
| file_depth_unix | Extract the depth of a file in a tree in the case of a Unix path |
| file_size | Extract the size of a file |
| file_option | Get from the path of a file the option to use to load or store data |
| file_remove | Deleting a file |


* table.qvs - Module containing all the table management functions

| Name | Description |
| ---- | ---- |
| table_drop | Dropping a table after checking it exists (to avoid any error) |
| table_rename | Renaming a table |
| column_drop | Dropping a column in a table after checking both exist (to avoid any error) |
| table_isempty | Checking if a table contains line or is empty |
| table_truncate | Recreating an empty table after checking it exists and contains data (to avoid any error) |
| column_rename | Renaming a column in a table |
| table_file_write | Write data from a table into a file |
| file_table_read | Load data from a file and put them in a table |
| file_table_multiple_read | Load data from one or several files and put them in a table |
| file_excel_sheet | Load data from an excel document and put them in a table |
| content_line_split | Take a table with key and values columns and splits the column values in several lines |
| content_line_concatenate | Take a table with key and value columns and concatenate the values in one line |


* histogram.qvs - Module containing all the histogram management functions

| Name | Description |
| ---- | ---- |
| histogram_ranges_from_values | Add a new column in a table with the range of the each value in a specific column according a table containing all the ranges |
| histogram_ranges_from_function | Add a new column in a table with the range of the each value in a specific column according a function |


* date.qvs - Module containing all the date management functions

| Name | Description |
| ---- | ---- |
| date_year | Extract the year from a date |
| date_month | Extract the month from a date |
| date_day | Extract the day from a date |
| date_yearmonth | Extract the year and the month set to the YYYY-MM pattern from a date |
| date_yearmonthday | Extract the year and the month set to the YYYY-MM-DD pattern from a date |


* string.qvs - Module containing all the string useful functions

| Name | Description |
| ---- | ---- |
| string_find_specific_content     | Building a string search function to catch some words from a list in a table |
| string_replace_special_character | Remove special characters in a string |
