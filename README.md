# Ensemble-of-Rotated-Decision-Trees
Random forests, a kind of ensemble of decision trees with a random component, have demonstrated themselves to be quite useful in drawing boundaries that effectively categorize data. However, the boundaries they give are difficult to interpret. In this project, I create and test ensembles of rotated decision trees, hoping that they might make more interpretable boundaries without losing accuracy. These ensembles are compared with random forests in their ability to categorize data from three data sets: the 2019 CPS ORG uniform extracts, the inventory of owned and leased properties, and the national student loan data system. (See more information in ensemble_code_and_tests.ipynb and citations below.)

For context, a decision tree is a kind of machine learning model that categorizes data based on two or more quantitative variables. For two-dimensional data, the boundary it draws consists of vertical and horizontal lines. I created the rotated decision tree as a variation of this model, such that (potentially more optimal) diagonal lines are possible. Essentially, it is a decision tree that rotates two-dimensional data by some specified amount, categorizes it, then rotates it back.

An ensemble consists of multiple models and makes decisions based on their results. As stated before, random forests are an ensemble of decision trees. The majority-vote ensemble I test contains 30 rotated decision trees, one for every 3 degrees from 0 to 87. Here, "majority-vote" means that the 30 rotated decision trees in the ensemble vote to create the resulting boundary that categorizes data. I create and compare 12 such ensembles and 12 random forests side-by-side, 4 for each of the 3 data sets.

More details are available in ensemble_code_and_tests.ipynb, which can be viewed on GitHub or opened with Jupyter Notebook on a local system.

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
