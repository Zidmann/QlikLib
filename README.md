# QlikLib
By [Zidmann](mailto:emmanuel.zidel@gmail.com) :bow:

## Description
Simple library of functions to use with Qlik project

## How to use

In the QVW document, add these lines with vQliklibPath containing the path of the QlikLib library.

```bash
// Including the variables and the functions available in the QlikLib custom library
SET vQliklibPath='<directory>\QlikLib';
$(Must_Include='$(vQliklibPath)\core.qvs');
```

## Implemented functions

| Name | Description |
| ---- | ---- |
| console_print | Print a message one the batch console |
| console_info | Print an information message in the specific format |
| console_sucess | Print a success message in the specific format |
| console_error | Print an error message in the specific format |
| console_jumpline | Jump a line in the console |
| console_delimitation | Printing a delimiter |


| Name | Description |
| ---- | ---- |
| variable_exist | Check if a variable is defined in Qlik |
| file_exist | Check if a file exists at a specific path |
| table_exist | Check if a table exists |
| excel_worksheet_exist | Check if a worksheet exists in an Excel document |
| column_exist | Check if a column exists in a specific table |
| variable_fill | Set a default value to a variable in the case it is not defined |


| Name | Description |
| ---- | ---- |
| number_pos | Return 0 if the number is positive or its value |
| number_neg | Return 0 if the number is negative or its value |
| number_sign | Return which sign has a number (0 is considered as having no sign) |
| number_abs | Return the absolute value of a number |
| number_order | Return the order in the 10 base of a number |


| Name | Description |
| ---- | ---- |
| file_dirname | Extract the directory of a file |
| file_basename | Extract the basename of a file |
| file_extension | Extract the extension of a file |
| file_dirname_unix | Extract the directory of a file in the case of a Unix path |
| file_basename_unix | Extract the basename of a file in the case of a Unix path |
| file_extension_unix | Extract the extension of a file in the case of a Unix path |
| file_size | Extract the size of a file |
| file_option | Get from the path of a file the option to use to load or store data |
| file_remove | Deleting a file |


| Name | Description |
| ---- | ---- |
| table_drop | Dropping a table after checking it exists (to avoid any error) |
| table_rename | Renaming a table |
| column_drop | Dropping a column in a table after checking both exist (to avoid any error) |
| column_rename |  |
| table_file_write | Write data from a table into a file  |
| file_table_read | Load data from a file and put them in a table |
| file_table_multiple_read | Load data from one or several files and put them in a table |
| file_excel_sheet | Load data from an excel document and put them in a table |


| Name | Description |
| ---- | ---- |
| date_year |  |
| date_month |  |
| date_day |  |
| date_yearmonth |  |
| date_yearmonthday |  |


| Name | Description |
| ---- | ---- |
| string_main | Extract the main content of a string |
