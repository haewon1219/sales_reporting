# sales_reporting

### Introduction
<img width="604" alt="스크린샷 2024-04-09 오후 5 29 31" src="https://github.com/haewon1219/sales_reporting/assets/162613635/f5a068b7-1704-431e-b123-56c45fa0b923">

In this project, I aimed to leverage Excel to create sales reports using a dataset consisting of 27,620 rows and 11 columns. The primary objective was to extract meaningful insights from the data to inform business decisions and track sales performance.

### Data Cleaning
- Loaded the dataset into Excel and conducted initial data inspection to understand its structure and potential challenges.
<img width="1372" alt="스크린샷 2024-04-08 오후 6 05 07" src="https://github.com/haewon1219/sales_reporting/assets/162613635/8182aee6-e15a-484f-8b1a-a559f3d81775">

- Identified and addressed missing or null values within the dataset.
- Ensured consistency and accuracy by checking for data errors.
<img width="1372" alt="스크린샷 2024-04-08 오후 6 13 05" src="https://github.com/haewon1219/sales_reporting/assets/162613635/5df393c4-d3ab-4f6d-ad2d-53e4658d7c08">

### Data Analysis
- Defined the key metrics and indicators necessary for the sales reports.
- Utilised category classification and sales/quantity categorisations to facilitate data analysis.
![Black and White Purple Blue Basic Flow Chart Whiteboard Brainstorm (2)](https://github.com/haewon1219/sales_reporting/assets/162613635/1d43cd35-1766-4c9b-aafe-8a76208d25ef)
- Calculated performance metrics such as growth rates, comparing actual sales to targets.
- Computed growth rates using previous sales data to provide insights into sales trends and patterns.

### Report Formatting and Structure Design
<img width="1305" alt="스크린샷 2024-04-09 오후 5 54 59" src="https://github.com/haewon1219/sales_reporting/assets/162613635/02e529b0-39f0-426c-bc44-6ae5c3880f39">
- Designed the layout and structure of the sales reports to ensure clarity and readability.
- Established formulas and connections between raw data and report elements.
- Employed absolute references to maintain data integrity and consistency.
- Implemented formulas to calculate daily, monthly, and yearly sales/quantity figures.

Calculate daily sales: =SUMIFS(raw!G:G,raw!$F:$F,$E12,raw!$A:$A,report!$W$6)
Calculate monthly sales: =SUMIFS(raw!G:G,raw!$F:$F,$E12,raw!$A:$A,"<=" & report!$W$6, raw!$A:$A, ">=" & report!$W$5)
Calculate yearly sales: =SUMIFS(raw!G:G,raw!$F:$F,$E12,raw!$A:$A,"<=" & report!$W$6)

### Pivot Table Creation
<img width="1630" alt="스크린샷 2024-04-09 오후 4 40 35" src="https://github.com/haewon1219/sales_reporting/assets/162613635/696647f9-e85b-457e-8617-82664510ec96">
- Generated pivot tables to display total sales, sales targets, and growth rates per category.

Retrieve the nth largest value from a range: =LARGE($B$3:$B$1048576, G4)
Retrieve category based on sales: =VLOOKUP(H4,$B$4:$E$1048576,4,FALSE)
Retrieve growth rate based on sales: =VLOOKUP(H4,$B$4:$E$1048576,3,FALSE)
