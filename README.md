# Ensemble-of-Rotated-Decision-Trees

This project has several dependencies. You must install Jupyter Notebook to run code within the file and view the results. In addition, the following Python packages must be installed for the Python kernel used when you run Jupyter notebook:
 - matplotlib
 - numpy
 - pandas
 - sci-kit learn
 - openpyxl

## Data citations:
 - Center for Economic and Policy Research. 2020. CPS ORG Uniform Extracts, Version 2.5. Washington, DC. https://xvk.aml.mybluehost.me/cps-uniform-data-extracts/cps-outgoing-rotation-group/cps-org-data/.
 - General Services Administration. 2025. "Inventory of Owned and Leased Properties (IOLP)." Last updated April 11, 2025. https://web.archive.org/web/20250412095936/https://catalog.data.gov/dataset/inventory-of-owned-and-leased-properties-iolp.
 - Office of Federal Student Aid. 2023. "National Student Loan Data System." Last updated August 12, 2023. https://catalog.data.gov/dataset/national-student-loan-data-system-722b0.
  
## Steps Performed in Accessing and Reformatting Data Files (none affecting data used):
CPS ORG Uniform Extracts:
 - Downloaded cepr_org_2019.zip
 - Extracted cepr_org_2019.dta
 - Converted cepr_org_2019.dta to CSV file
 - Removed all unused columns (only necessary to upload the data file to this online repository, which would otherwise exceed the size restriction on GitHub)

Inventory of Owned and Leased Properties:
 - Downloaded 2025-4-11-iolp-buildings.xlsx (no changes)

National Student Loan Data System:
 - Downloaded FL_Dashboard_AY2009_2010_Q1.xls
 - Converted FL_Dashboard_AY2009_2010_Q1.xls to CSV file
 - Renamed _unused_ columns titled "Recipients" or "$ of Loans Originated" to prevent repeating column names
