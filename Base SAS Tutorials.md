**PROC IMPORT** is the SAS procedure used to read data from excel into SAS.

```sas
PROC IMPORT 
DATAFILE="filename"
OUT=SAS-data-set 
DBMS=identifier 
  REPLACE;
  SHEET="Sheet-name";
  GETNAMES=YES; 
  DATAROW=N;
  RANGE="range-name";
RUN;
```

1. **DATAFILE=** option tells SAS where to find the Excel file that you want to import  (Complete filename path).
**For example** : DATAFILE = "C:\Desktop\age.xls"

2. **OUT**= option tells SAS to create a dataset with any name of your choice. By default, the imported dataset is saved on WORK library (temporary library)    
 Examples :
i. OUT = Age .  In this statement, PROC IMPORT uses the WORK library. This implies OUT = Age is equivalent to OUT = Work.Age .
ii. OUT = Input.Age.  In this statement, PROC IMPORT uses the Input library (Permanent library).

3. **DBMS**= option tells SAS the type of file to read.
 Examples :
i. DBMS =  XLS for Excel 97-2003 workbooks ii.DBMS =  XLSX for Excel 2007 - 2013 workbooks

4. **REPLACE** is used to overwrite the existing SAS dataset (If any) mentioned in the OUT= option.
5. **SHEET**= option is used to specify which sheet SAS would import.
 Examples :
i.  SHEET =  "Sheet1" - To import data from worksheet named sheet1. ii. SHEET =  "Goal" - To import data from worksheet named Goal.

6. **GETNAMES**= YES tells SAS to use the first row of data as variable names.

By default, PROC IMPORT uses GETNAMES= YES. If you type GETNAMES= NO, SAS would not read variable names from first row of the sheet.

7. **DATAROW**= option is used to specify starting row from where SAS would import the data.

For example : DATAROW =5 tells SAS to start reading data from row number 5.

Note : 

i. When GETNAMES=YES, DATAROW must be greater than or equal to 2.
ii. When GETNAMES=NO, DATAROW must be greater than or equal to 1

8. **RANGE**= option is used to specify which range SAS would import.

Examples :

i. RANGE="Sheet1$B2:D10"
 This would tell SAS to import data from range B2:D10 from sheet1

ii. RANGE="Information"
 This would tell SAS to import data from excel defined name range. In the example shown above, it is Information.










