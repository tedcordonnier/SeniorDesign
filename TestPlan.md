# Test Plan

## Project: Statistical Correlation Analysis and Automation Program

## Part I. Description of Overall Test Plan

The test plan for the Automatic Correlation Calculator project encompasses a comprehensive approach to ensure the program's functionality, performance, and reliability. Testing strategies include automated unit tests to validate the correctness of correlation computations, integration tests to ensure seamless interaction between the program's components, and performance tests to assess the tool's efficiency with varying sizes of datasets. Emphasis is placed on ensuring the program accurately calculates correlations between the target column and all other columns in a CSV file, handles different data types, and provides meaningful error messages for invalid inputs.

## Part II. Test Case Descriptions

## Test Cases
List a series of 10-25 tests for validating your project outcomes. For each test case provide the following:
1. Test case identifier (a number or unique name)
2. Purpose
3. Description
4. Inputs
5. Outputs
6. Normal/Abnormal/Boundary
7. Blackbox/Whitebox
8. Functional/Performance
9. Unit/Integration

Note that some of these categories may be inappropriate for your project and may be omitted if you can justify doing so. For items 6-9, only one term should apply.



#### R01 — User can view code
**Test Case ID**: TC01  
**Purpose**: Validate calculation accuracy for known dataset.  
**Description**: Perform correlation calculations on a dataset with pre-determined correlation values.  
**Inputs**: CSV file with known correlation coefficients between columns.  
**Outputs**: The program outputs correlation coefficients that match the known values.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Whitebox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit


#### R02 — User can create/upload a recipe
**Test Case ID**: TC02  
**Purpose**: Test handling of large datasets.  
**Description**: Assess the program's performance and accuracy on a very large dataset.  
**Inputs**: CSV file with a large number of rows and columns.  
**Outputs**: Accurate correlation coefficients within a reasonable processing time.  
**Normal/Abnormal/Boundary**: Boundary  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Performance  
**Unit/Integration**: Integration

**Test Case ID**: TC03  
**Purpose**: Ensure error handling for missing data.  
**Description**: Test the program's ability to handle datasets with missing values.  
**Inputs**: CSV file with missing values in various columns.  
**Outputs**: Program handles missing data gracefully, either by imputation or by excluding missing values, depending on the configuration.  
**Normal/Abnormal/Boundary**: Abnormal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

**Test Case ID**: TC04  
**Purpose**: Validate handling of non-numeric data.  
**Description**: Ensure the program correctly ignores or processes non-numeric columns based on configuration.  
**Inputs**: CSV file containing a mix of numeric and non-numeric columns.  
**Outputs**: Non-numeric columns are correctly excluded from the analysis or appropriately processed.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

**Test Case ID**: TC05  
**Purpose**: Test program's scalability with varying dataset sizes.  
**Description**: Evaluate performance degradation as dataset size increases.  
**Inputs**: Multiple CSV files of increasing size.  
**Outputs**: Linear or sub-linear increase in processing time with respect to dataset size.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Whitebox  
**Functional/Performance**: Performance  
**Unit/Integration**: Integration

**Test Case ID**: TC06  
**Purpose**: Ensure correct operation with different delimiter types.  
**Description**: Validate the program's ability to process CSV files with various delimiters (e.g., commas, semicolons).  
**Inputs**: CSV files with different delimiters.  
**Outputs**: Correct correlation coefficients regardless of the delimiter used.  
**Normal/Abnormal/Boundary**: Boundary  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

**Test Case ID**: TC07  
**Purpose**: Verify correct processing of datasets with header rows.  
**Description**: Ensure the program correctly identifies and uses header rows for column names.  
**Inputs**: CSV file with a header row.  
**Outputs**: Correlation calculations are correctly applied to columns as identified by the header row.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

**Test Case ID**: TC08  
**Purpose**: Test error handling for files with inconsistent row lengths.  
**Description**: Evaluate the program's response to CSV files where some rows have more columns than others.  
**Inputs**: Malformed CSV file.  
**Outputs**: An appropriate error message is displayed, and the program terminates gracefully.  
**Normal/Abnormal/Boundary**: Abnormal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

**Test Case ID**: TC09  
**Purpose**: Validate correct correlation calculation with categorical data (optional, if applicable).  
**Description**: Test the program's ability to handle categorical data via encoding or other methods before calculating correlations.  
**Inputs**: CSV file with categorical data.  
**Outputs**: Accurately calculated correlation coefficients considering the encoded or transformed categorical data.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

**Test Case ID**: TC10  
**Purpose**: Assess program's usability and clarity of output.  
**Description**: Evaluate the clarity, readability, and usefulness of the program's output, including correlation coefficients and any warnings or errors.  
**Inputs**: Any CSV file.  
**Outputs**: Output is clearly formatted, easily understandable, and actionable.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Integration


| Test ID  | Normal/Abnormal | Blackbox/Whitebox | Functional/Performance | Unit/Integration |
|----------|-----------------|-------------------|------------------------|------------------|
| TC01     | Normal          | Black Box         | Functional             | Integration      |
| TC02     | Normal          | White Box         | Functional             | Integration      |
| TC03     | Normal          | Black Box         | Functional             | Integration      |
| TC04     | Normal          | Black Box         | Functional             | Integration      |
| TC05     | Abnormal        | Black Box         | Functionsal             | Integration      |
| TC06     | Normal          | White Box         | Functional             | Integration      |
| TC07     | Normal          | Black Box         | Functional             | Integration             |
| TC08     | Normal          | Black Box         | Functional             | Integration      |
| TC09     | Normal          | Black Box         | Functional             | Integration             |
| TC10     | Normal          | Black Box         | Functional             | Integration             |
| TC11     | Normal          | Black Box         | Functional             | Integration      |
| TC12     | Normal          | Black Box         | Functional             | Integration             |