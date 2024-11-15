# _%tblMaker()_

The SAS macro **_%tblMaker()_** can currently be used to create summary tables in the form of a standard **Table 1** seen in medical journals. This macro automatically detects categorical/continuous variables, calculates appropriate descriptive statistics, reports data missingness, and performs appropriate statistical tests across column groupings. 


# Installation
You can import the **_%tblMaker()_** function into your SAS session by running the following code:
```r
filename tblMaker url "https://raw.githubusercontent.com/bradyrippon/tblMaker/refs/heads/main/tblMaker.sas";
%include tblMaker;
```
This will execute the macro directly from this GitHub page. You can alternative download the raw code file and run locally. 


# Usage
**_%tblMaker(_** <br />
	**data** = _your dataset_, <br />
 	**byVar** = _column subsetting variable_, <br />
  	**missingRow** = _("Yes", "No") to display missing data rows (**Yes** default)_, <br />
   	**statContinuous** = _("Mean", "Median", "Both") for continuous data display (**Mean** default)_, <br />
    	**showTest** = _("Yes", "No") to display test column (**No** default)_, <br />
**);**


# Examples
Please note that the examples below were generated using the _journal_ style within **ods rtf** file exporting. You should use whichever style template you'd like to design your table. 

### SASHELP.baseball
```r
%tblMaker(
	data = SASHELP.baseball(keep = league natbat crruns division nassts),
	byVar = league
);
```
![summary table for SASHELP.baseball](https://github.com/bradyrippon/tblMaker/blob/main/figures/tbl-baseball.png)

### SASHELP.heart
```r
%tblMaker(
	data = SASHELP.heart(keep = status sex -- systolic chol_status bp_status),
	byVar = status
);
```
![summary table for SASHELP.heart](https://github.com/bradyrippon/tblMaker/blob/main/figures/tbl-heart.png)


