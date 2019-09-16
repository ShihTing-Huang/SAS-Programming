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










