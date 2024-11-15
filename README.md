# _%tblMaker()_

The SAS macro **_%tblMaker()_** can currently be used to create summary tables in the form of a standard **Table 1** seen in medical journals. This macro automatically detects categorical/continuous variables, calculates appropriate descriptive statistics, reports data missingness, and performs appropriate statistical tests across column groupings. 

```sas
/* This is a SAS code example */
data example;
    set sashelp.class;
    where age > 12;
    keep name age height weight;
run;
```
