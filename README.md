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
