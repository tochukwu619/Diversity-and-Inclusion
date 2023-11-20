# Diversity-and-Inclusion

---
### TABLE OF CONTENT
1. [PROJECT OVERVIEW](#project-overview)
2. [DATA SOURCE](#data-source)
3. [TOOLS](#tools)
4. [DATA PREPARATION](#data-preparation)
5. [EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)
6. [DATA ANALYSIS](#data-analysis)
7. [RESULTS](#results)
8. [RECOMMENDATION](#recommendation)
9. [LIMITATION](#limitation)
10. [REFERENCE](#reference)
---
### PROJECT OVERVIEW

The project is on the analysis of data gotten from a Company to monitor the diversity and inclusion of the promotions that happened in the company over a period of time.
![Diversity Dashboard](https://github.com/tochukwu619/Diversity-and-Inclusion/assets/125865918/1a69a46c-350c-4572-8d70-d1d714a299d7)

### DATA SOURCE

The dataset used for this project is labelled as ’03 Diversity-Inclusion-Dataset.xlsx’.

### TOOLS

-	Microsoft Excel
-	Microsoft power BI

### DATA PREPARATION

Using Microsoft Excel, the data was cleaned by ensuring that there were no duplicates. Spelling checks were also performed on the fields for consistency. Blank-value check was done to ensure that there was no inappropriate blank cell.

### EXPLORATORY DATA ANALYSIS

The following KPIs were defined during this project:
•	Hires
•	Promotion
•	Turnovers
•	Performance 

### DATA ANALYSIS

Using Microsoft Power BI, measures were developed for this analysis.  The number of men is calculated as:
```
Number of Men = CALCULATE(COUNTROWS('Pharma Group AG'), 'Pharma Group AG'[Gender]="Male")
```

The number of women is calculated as:
```
Number of Women = CALCULATE(COUNTROWS('Pharma Group AG'), 'Pharma Group AG'[Gender]="Female") 
```

Average performance rating is calculated as:
```
Average Rating = AVERAGE('Pharma Group AG'[FY20 Performance Rating])
```

Number of people that left during FY 20 is calculated as:
```
Leaver = CALCULATE(COUNTROWS('Pharma Group AG'), 'Pharma Group AG'[FY20 leaver?]="Yes") 
```

Percentage men hired is calculated as:
```
% of Hires Men = DIVIDE(CALCULATE(COUNTROWS('Pharma Group AG'), 'Pharma Group AG'[New hire FY20?] = "Y", 'Pharma Group AG'[Gender] = "Male"), CALCULATE(COUNTA('Pharma Group AG'[New hire FY20?]), 'Pharma Group AG'[New hire FY20?] = "Y")) 
```

Percentage women hired is calculated as:
```
% of Hires Women = DIVIDE(CALCULATE(COUNTROWS('Pharma Group AG'), 'Pharma Group AG'[New hire FY20?] = "Y", 'Pharma Group AG'[Gender] = "Female"), CALCULATE(COUNTA('Pharma Group AG'[New hire FY20?]), 'Pharma Group AG'[New hire FY20?] = "Y")) 
```

Percentage turnover is calculated as:
```
% Turnover = DIVIDE(CALCULATE(COUNTA('Pharma Group AG'[In base group for turnover FY20]), 'Pharma Group AG'[In base group for turnover FY20] = "Y"), COUNTA('Pharma Group AG'[In base group for turnover FY20])) 
```

Percentage men promoted is calculated as:
```
% Men Promoted = DIVIDE(CALCULATE(COUNTROWS('Pharma Group AG'), 'Pharma Group AG'[Promotion in FY21?]="Yes", 'Pharma Group AG'[Gender]="Male"), CALCULATE(COUNTA('Pharma Group AG'[Promotion in FY21?]), 'Pharma Group AG'[Promotion in FY21?]="Yes")) 
```

Percentage women promoted is calculated as:
```
% Women Promoted = DIVIDE(CALCULATE(COUNTROWS('Pharma Group AG'), 'Pharma Group AG'[Promotion in FY21?]="Yes", 'Pharma Group AG'[Gender]="Female"), CALCULATE(COUNTA('Pharma Group AG'[Promotion in FY21?]), 'Pharma Group AG'[Promotion in FY21?]="Yes")) 
```


### RESULTS

It was observed that:
-	The average performance rating is 2.41.
-	All nationalities are not properly represented in all departments of the company.
-	There are no men represented in HR department.
-	Sales & marketing department has the highest percentage turnover.

### RECOMMENDATION

There is a limited diversity in terms of promotion in the different departments. 

### LIMITATION

No noticeable limitations for this project.

### REFERENCE

[Forage](www.theforage.com)


