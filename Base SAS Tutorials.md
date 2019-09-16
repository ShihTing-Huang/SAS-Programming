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
