# Test Plan

## Project: Statistical Correlation Analysis and Automation Program

## Part I. Description of Overall Test Plan

The test plan for the Automated Correlation Analysis project encompasses a comprehensive approach to ensure the program's functionality, performance, and reliability. Testing strategies include unit tests to validate the correctness of correlation computations, integration tests to ensure correct interaction between the program's components, and performance tests to assess the tool with varying datasets. Emphasis is placed on ensuring the program accurately calculates correlations between the target column and all other columns in a CSV file, handles different data types, and provides meaningful error messages for invalid inputs.

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



#### TC01 - Accuracy with Known Dataset
**Test Case ID**: TC01  
**Purpose**: Validate calculation accuracy for known dataset.  
**Description**: Perform correlation calculations on a dataset with pre-determined correlation values.  
**Inputs**: CSV file with known correlation coefficients between columns.  
**Outputs**: The program outputs correlation coefficients that match the known values.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Whitebox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC02 - Large Dataset Performance
**Test Case ID**: TC02  
**Purpose**: Test handling of large datasets.  
**Description**: Assess the program's performance and accuracy on a very large dataset.  
**Inputs**: CSV file with a large number of rows and columns.  
**Outputs**: Accurate correlation coefficients within a reasonable processing time.  
**Normal/Abnormal/Boundary**: Boundary  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Performance  
**Unit/Integration**: Integration

#### TC03 - Missing Data Handling
**Test Case ID**: TC03  
**Purpose**: Ensure error handling for missing data.  
**Description**: Test the program's ability to handle datasets with missing values.  
**Inputs**: CSV file with missing values in various columns.  
**Outputs**: Program handles missing data gracefully, by excluding missing values 
**Normal/Abnormal/Boundary**: Abnormal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC04 - Non-numeric Data Handling
**Test Case ID**: TC04  
**Purpose**: Validate handling of non-numeric data.  
**Description**: Ensure the program correctly ignores or processes non-numeric columns based on configuration.  
**Inputs**: CSV file containing a mix of numeric and non-numeric columns.  
**Outputs**: Non-numeric columns are correctly excluded from the analysis or appropriately processed.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC05 - Scalability with Dataset Size
**Test Case ID**: TC05  
**Purpose**: Test program's scalability with varying dataset sizes.  
**Description**: Evaluate performance degradation as dataset size increases.  
**Inputs**: Multiple CSV files of increasing size.  
**Outputs**: Linear or sub-linear increase in processing time with respect to dataset size.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Whitebox  
**Functional/Performance**: Performance  
**Unit/Integration**: Integration

#### TC06 - Delimiter Variability Handling
**Test Case ID**: TC06  
**Purpose**: Ensure correct operation with different delimiter types.  
**Description**: Validate the program's ability to process CSV files with various delimiters (e.g., commas, semicolons).  
**Inputs**: CSV files with different delimiters.  
**Outputs**: Correct correlation coefficients regardless of the delimiter used.  
**Normal/Abnormal/Boundary**: Boundary  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC07 - Header Row Processing
**Test Case ID**: TC07  
**Purpose**: Verify correct processing of datasets with header rows, as well as it's error handling if the data is missing 
**Description**: Ensure the program correctly identifies and uses header rows for column names.  
**Inputs**: CSV file with a header row.  
**Outputs**: Correlation calculations are correctly applied to columns as identified by the header row.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC08 - Inconsistent Row Length Error Handling
**Test Case ID**: TC08  
**Purpose**: Test error handling for files with inconsistent row lengths.  
**Description**: Evaluate the program's response to CSV files where some rows have more columns than others.  
**Inputs**: Malformed CSV file.  
**Outputs**: An appropriate error message is displayed, and the program terminates gracefully.  
**Normal/Abnormal/Boundary**: Abnormal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC09 - Categorical Data Correlation
**Test Case ID**: TC09  
**Purpose**: Validate correct correlation calculation with categorical data (optional, if applicable).  
**Description**: Test the program's ability to handle categorical data via encoding or other methods before calculating correlations.  
**Inputs**: CSV file with categorical data.  
**Outputs**: Accurately calculated correlation coefficients considering the encoded or transformed categorical data.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC10 - Usability and Output Clarity
**Test Case ID**: TC10  
**Purpose**: Assess program's usability and clarity of output.  
**Description**: Evaluate the clarity, readability, and usefulness of the program's output, including correlation coefficients and any warnings or errors.  
**Inputs**: Any CSV file.  
**Outputs**: Output is clearly formatted, easily understandable, and actionable.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Integration

#### TC11 - Categorical Data Correlation Accuracy
**Test Case ID**: TC11  
**Purpose**: Ensure accurate correlation calculation with categorical data.  
**Description**: Test the program's ability to accurately calculate and report correlation coefficients for categorical variables, using appropriate statistical methods like Cramér's V or Chi-Square test.  
**Inputs**: CSV file containing categorical data columns.  
**Outputs**: Correct correlation coefficients for categorical data, consistent with expected values from statistical analysis software.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC12 - Continuous Data Correlation Precision
**Test Case ID**: TC12  
**Purpose**: Validate the precision of correlation calculations for continuous data.  
**Description**: Evaluate the program's precision in calculating correlation coefficients (e.g., Pearson's r) for continuous variables, ensuring it matches precision standards of established statistical software.  
**Inputs**: CSV file with continuous numerical data.  
**Outputs**: Correlation coefficients for continuous data that are precise and match those calculated by reference statistical software.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC13 - Mixed Data Types Correlation Handling
**Test Case ID**: TC13  
**Purpose**: Verify correct correlation analysis with mixed data types.  
**Description**: Assess the program's capability to handle datasets containing both categorical and continuous data types, ensuring it chooses the appropriate correlation calculation methods for each pair of variables.  
**Inputs**: CSV file with a mix of categorical and continuous data columns.  
**Outputs**: Accurate correlation coefficients for all pairs of variables, correctly applying different methods as needed for categorical vs. continuous data.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC14 - Program Settings Effectiveness
**Test Case ID**: TC14  
**Purpose**: Assess the impact and effectiveness of user-configurable program settings on correlation analysis outcomes.  
**Description**: Evaluate how the adjustment of settings like `bins`, `max_unique_values_threshold`, `showCrosstab`, `showBinnedCrosstab`, and `showGroupMeans` affects the calculation and presentation of correlation analyses. This test will involve running the program with different settings configurations to observe the changes in output, especially focusing on the handling of categorical data, the applicability of chi-square tests, and the utility of ANOVA where applicable.  
**Inputs**: Multiple CSV files with varying characteristics to test each setting's impact under different conditions.  
**Outputs**: Varied depending on settings, expected to accurately reflect the setting change
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Integration

#### TC15 - Output Categories Validation
**Test Case ID**: TC15  
**Purpose**: Ensure output arrays accurately reflect the correct categories for categorical data.  
**Description**: This test verifies that the program correctly identifies and outputs the categories for categorical variables, especially after any internal processing such as binning or when applying chi-square tests. The test will compare the categories identified by the program against the actual categories present in the input data to ensure accuracy and completeness.  
**Inputs**: CSV files with categorical data, including some with a high number of categories and others with fewer, distinctly identifiable categories.  
**Outputs**: Output arrays/lists that should accurately match the categories found in the input data, without any missing or incorrectly added categories.  
**Normal/Abnormal/Boundary**: Normal  
**Blackbox/Whitebox**: Blackbox  
**Functional/Performance**: Functional  
**Unit/Integration**: Unit

#### TC16 - Comparison with Reputable Statistics Tool
**Test Case ID**: TC16  
**Purpose**: Compare program's correlation analysis results with those from a reputable statistics tool, such as SPSS, to validate accuracy.  
**Description**: This test involves running correlation analyses using the program on various datasets and comparing the results with those obtained from SPSS or another reputable statistics tool. The focus is on ensuring that the correlation coefficients, p-values, and any other statistical measures provided by the program are consistent with those produced by the established tool, within a reasonable margin of error.  
**Inputs**: Datasets that include a mix of categorical, continuous, and mixed data types.  
**Outputs**: Correlation analysis results from the program and the comparison tool. The expected outcome is a high degree of similarity between the two sets of results, indicating the program's accuracy.  
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
| TC05     | Abnormal        | Black Box         | Functional             | Integration      |
| TC06     | Normal          | White Box         | Functional             | Integration      |
| TC07     | Normal          | Black Box         | Functional             | Integration             |
| TC08     | Normal          | Black Box         | Functional             | Integration      |
| TC09     | Normal          | Black Box         | Functional             | Integration             |
| TC10     | Normal          | Black Box         | Functional             | Integration             |
| TC11     | Normal          | Black Box         | Functional             | Integration      |
| TC12     | Normal          | Black Box         | Functional             | Integration             |
