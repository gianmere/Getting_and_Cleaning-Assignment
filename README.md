# Getting and Cleaning data - tha Assignment
This repository contains my work for the course project for the Coursera course "Getting and Cleaning data".

It contains 4 files:
* README.md - This file
* CodeBook.md - a code book that describes the variables, the data, and any transformations performed to clean up the data
* run_analysis.R - the script for performing the analysis
* tidy_data.txt - a tidy data set as requested

## About run_analysis.R

To run the script, go in the directory where it is and use the command:

source(run_analysis.R)

If there isn't a sub-directory called "UCI HAR Dataset" in the directory there the script runs, it downloads the zip file with all tha datas, unzips it and performs all the oprations to obtain the data set requested from the assignment.

the script requestes the following packages:
* data.table
* dplyr

You have to install them before run the script.

The script writes a file called tidy_data.txt with the data set requested from the assignment.

## About tidy_data.txt

It contains the data set requested from the assignment.

You can view it going in the directory where it is and using the commands:

data <- read.table("tidy_data.txt", header = TRUE)  
View(data)  

The data set is tidy because it satisfy the properties:
* Each variable misured is in one column
* Each osservation is in one row
* There is a table for each "kind" of variable (only one table)

The names of the column is meaningfull. 
They are strings written in upper camel case (see https://en.wikipedia.org/wiki/Camel_case).
The suffix ''Mean()'' means the misure is about a mean.
The suffix ''()'' means the misure is about a standard deviation.
For each measure is indicate it's about axis x,y or z.

For more informations, see the file CodeBook.md

