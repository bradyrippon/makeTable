# _%tblMaker()_

The SAS macro **_%tblMaker()_** can currently be used to create summary tables in the form of a standard **Table 1** seen in medical journals. This macro automatically detects categorical/continuous variables, calculates appropriate descriptive statistics, reports data missingness, and performs appropriate statistical tests across column groupings. 

```r
%tblMaker(
	data = SASHELP.baseball(keep = league natbat crruns division nassts),
	byVar = league
);
```


<div style="background-color: #f4f4f4; padding: 10px; border-radius: 5px; font-family: monospace;">
  <span style="color: #007acc;">data</span> example;<br>
  &nbsp;&nbsp;&nbsp;&nbsp;<span style="color: #d73a49;">set</span> sashelp.class;<br>
  &nbsp;&nbsp;&nbsp;&nbsp;<span style="color: #6f42c1;">where</span> age &gt; 12;<br>
  &nbsp;&nbsp;&nbsp;&nbsp;keep name age height weight;<br>
<span style="color: #007acc;">run</span>;
</div>

Here's more text here.

