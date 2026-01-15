# Ensemble-of-Rotated-Decision-Trees

### Dependencies
This project has several dependencies. You must install Jupyter Notebook to run code within the file and view the results. In addition, the following Python packages must be installed for the Python kernel used when you run Jupyter notebook:
 - matplotlib
 - numpy
 - pandas
 - sci-kit learn
 - openpyxl

### Data Citations
 - Center for Economic and Policy Research. 2020. CPS ORG Uniform Extracts, Version 2.5. Washington, DC. https://xvk.aml.mybluehost.me/cps-uniform-data-extracts/cps-outgoing-rotation-group/cps-org-data/.
 - General Services Administration. 2025. "Inventory of Owned and Leased Properties (IOLP)." Last updated April 11, 2025. https://web.archive.org/web/20250412095936/https://catalog.data.gov/dataset/inventory-of-owned-and-leased-properties-iolp.
 - Office of Federal Student Aid. 2023. "National Student Loan Data System." Last updated August 12, 2023. https://catalog.data.gov/dataset/national-student-loan-data-system-722b0.
  
### Steps Performed in Accessing and Reformatting Data Files (none affecting data used)
CPS ORG Uniform Extracts:
 - Downloaded cepr_org_2019.zip
 - Extracted cepr_org_2019.dta into data subfolder
 - Converted cepr_org_2019.dta to CSV file
 - In CSV file, renamed column names as follows: "union" to "Union", "weekpay" to "Weekly Pay", and "wage4" to "Yearly Wage"
   - This helped with clarity and ensured variable names had a consistent style.
 - Removed all unused columns
   - This step was necessary to upload the data file to this online repository, which would otherwise exceed the size restriction on GitHub. If you repeat these steps with the file on a local system, removing unused columns will likely not be required.


Inventory of Owned and Leased Properties:
 - Downloaded 2025-4-11-iolp-buildings.xlsx into data subfolder (no changes)


National Student Loan Data System:
 - Downloaded FL_Dashboard_AY2009_2010_Q1.xls into data subfolder
 - Converted FL_Dashboard_AY2009_2010_Q1.xls to CSV file
 - Renamed _unused_ columns titled "Recipients" or "$ of Loans Originated" to prevent repeating column names
