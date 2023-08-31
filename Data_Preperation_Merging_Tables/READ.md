## Data Preperation - Merging Tables

Here we will understand the VLOOKUP function in Google Spreadsheet


=VLOOKUP(search_key, Range, index, is_sorted)

![Screenshot 2023-08-31 081724](https://github.com/PreetyManna11/Step_by_Step_Procedure_to_Analyze_Data/assets/61684282/23369e9f-b8f3-4d82-94f0-6fe51b0930a9)


1. The search_key represents the unique identifier or key-value you want to look up. It can either be a value or a reference to a cell containing the value.
2. The range is the range of cells (in the source table) within which the VLOOKUP function should search.
3. The index is the column number within the range from which the corresponding value (the one in the same row as Search key) should be retrieved.
4. is_sorted is an optional parameter. It can either be TRUE or FALSE.
   * A FALSE value for “is_sorted” indicates that the first column of range does not need to be sorted in ascending order. So, the VLOOKUP function searches for an exact match of the “search_key”.
    * If there is more than one value equal to “search_key”, then VLOOKUP accesses the first occurrence of the “search_key”.

When you use VLOOKUP function to merge two tables together, there might be several scenerios as follows:

- Case 1 : Suppose both the tables are in different workbook

Formula: =VLOOKUP(search_key,Importrange(“{sheetsURL}”, “{sheetname}!{cellrange}”), index,is_sorted)

- Case 2 : Suppose both the tables are in same workbook but different sheet

Formula: =VLOOKUP(lookup_value, ‘Sheet2’!cell range, 2, False)

- Case 3 : Suppose both the tables are in same workbook and same sheet

Formula: =VLOOKUP(lookup_value, cell range, 2, False)











### Source

- Coding Ninjas

#### Hi, I'm Preety! 👋


#### 🚀 About Me
I have completed my graduation from SRM, Chennai and now I am working as a Software Engineer at Cognizant. I have a keen interest in the field of Data Analytics and look forward to enhance my knowledge in the same. 


#### 🛠 Tools required for Analyzing the Data using the framework
MS Excel, Google Spreadsheet


## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/preety-manna-687a73194/) 
  
