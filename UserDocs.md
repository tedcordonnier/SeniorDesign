## Anaconda Navigator and Jupyter Notebook

To run the Automated Correlation Analysis Tool, we must run this file in Python. Since my file is using the .ipynb extension, it is easiest to use Jupyter Notebook to run this file. I installed Anaconda Navigator, which comes with Jupyter Notebook. An explanation of installing Anaconda Navigator can be found here.
https://docs.anaconda.com/free/navigator/index.html

Once you have Jupyter Notebook up and running, open my file. Before running, ensure that for each library that has been imported at the beginning of the code, your Anaconda has those libraries installed. You can use the Anaconda CMD to install these libraires. Here is a link to installing packages
https://conda.io/projects/conda/en/latest/user-guide/concepts/installing-with-conda.html

## Editing the file to change the .csv's file path, the target column, and settings

At the top of the file the user can find the .csv file path location, the target column, as well as the settings. 
The user must first have a specified .csv file that they want to do correlation analysis on. This file path must be provided so that the program knows which file to analyze. 

The user must also provide a target variable. This target variable is the column that the user wants to compare to all other columns, to test to correlatoin between them. The target variable should generally be the variable that the user wants to optimize for. Some examples would be sales, quality rating, etc.

The settings are for advanced users who want to add additional information to the output, as well as change how the program runs certain tests.

This program will use that file, as well as the target variable and the given settings, to compute the correlaton of the target to each column. 

![image](https://github.com/tedcordonnier/SeniorDesign/assets/83316488/ec81eb77-a94c-4164-8458-9f4295877aa8)

## Running the file

Now, run the file inside of the Jupyter Notebook. 

This program will then automatically determine the data types of each column, and then loop through each column using the apropriate test of correlation on the target vs. column. 

For each of the combinations of target and columns that are found to have correlation, the program displays the test that is used as well as the details of the test, and finally the correlation between these variables. This is to ensure that if the user wants to know more informatioon about the correlaton test results, they can see the exact numbers of the result. 

## Results Explained

The correlatoin is divided into 5 main categories. These are large, medium, small, none, and unable. I provide the final correlation to the user in buckets. For the large, medium, and small correlations, the results of the correlation tests have different cutoff points for what is regarded by the statistical community as large, medium, and small. For this reason, I simply place the column name into the bucket that they fall into, based on the test used and the resulting number of the test. The none bucket means no correlaton. The unable bucket means that there are certain criteria for this test of correlation to be used, and if that criteria is not met, the test does not get executed and the column name goes into the unable bucket.

The way I provide the final correlation to the user had to be done this way becuase of the nature of these tests. 
Unless I created a formula that could standardise the results of each of the different tests used into one score, this is the solution that had to be used, which is placing each of the different results into buckets. Which bucket they go into is determined by which test was used and the resulting number of the test. 

![image](https://github.com/tedcordonnier/SeniorDesign/assets/83316488/1455a99d-867d-4426-9c09-f5feafaccaed)

The results of each test can be a bit difficult to interpret for the average user. The results also differ from test to test with there being different output variables. To explain each test:

#### Explanation of Each Test

But before I explain each test, a commonality between all the tests is the p-value. The p-value represents how likely you are to have found a particular set of observations if the variables are independent. In other words, it is the likelyhood that the result has occured by chance, instead of due to the correlation between the variables. We want this value to be below 0.05, which is the most common threshold that is used. If it is below this threshold, we can say that the results of the test (showing correlation or not), is valid.

Chi^2 Test of Correlation: Categorical vs Categorical. Creates a crosstab (table that counts amount of each data in each group) of the categorical data, and then compares the results to the expected results if the variables were independent. Then the chi2 value is calculated, along with the critical value (cv) from the chart of the chi2 distribution. If chi2 is greater than the critical value, we can move on to using the test called Cramer's V. Chi2 value does not give us the degree of correlation, so we must use Cramer's V. The result of Cramer's V then allows us to put the column from target vs. column into buckets, based on the value. v > 0.5 = Large, v > 0.3 = Medium, v > 0.1 = Small, v < 0.1 = None.

Spearmans/Pearsons Test of Correlation: Numerical vs Numerical. Spearman's correlation determines the strength and direction of the monotonic relationship between your two variables. The result of Spearmans is a x value between -1 and 1, which determines the strength and direction of correlation. x > 0.5 = Large Positive, x > 0.3 = Medium Positive, x > 0.1 = Small Positive, -0.1 < x < 0.1 = None, x < -0.1 = Small Negative, x < -0.3 = Medium Negative, x < -0.5 = Large Negative.

ANOVA: Categorical vs Numerical. This test uses expected means of each group, and checks to see if there is a significant difference between these group means. If the output from ANOVA is greater than the critical value found in the one-way ANOVA distribution, then we can also calculate Eta^2. Since ANOVA cannot quantify the strength of the relationship, Eta^2 is used, and then the values of Eta^2 determine the strength of the relationship. x > 0.14 = Large, x > 0.06 = Medium, x > 0.01 = Small x < 0.01 = None.

Binned Chi^2 Test of Correlation: Numerical vs Categorical. Same as Chi^2 except the numerical values are put into bins so that chi^2 can be used.

## Final Result

These results are then shown at the end of the program.	These reuslts appear in a format similar to the picture given, with listing the target, and then listing the column names that fall into each of the buckets.

![image](https://github.com/tedcordonnier/SeniorDesign/assets/83316488/4e7beeda-4119-46af-be3d-80d6e51d732a)



## FAQ (Frequently Asked Questions)


#### Which datasets can I use this program on?

Many datasets work, however certain datasets should be avoided to be used inside of this program. Datasets that should be avoided

Datasets that have have columns that would not be useful to find correlation over.
  A good example would be things such as addresses or names, these are things that correlation cannot be found between due to the limit of statistics
Datasets that have many of it columns having all unique values


#### Performance of the program when the number of rows or columns is large?

I have tested with 20+ different columns and datasets with tens of thousands of columns without much slowdown. The program generally takes a couple of seconds to run. There are little to no issues with using a large dataset.

