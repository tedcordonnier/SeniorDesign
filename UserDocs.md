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

## Final Result

These results are then shown at the end of the program.	These reuslts appear in a format similar to the picture given, with listing the target, and then listing the column names that fall into each of the buckets.

![image](https://github.com/tedcordonnier/SeniorDesign/assets/83316488/4e7beeda-4119-46af-be3d-80d6e51d732a)

