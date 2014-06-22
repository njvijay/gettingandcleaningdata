# Getting And Cleaning Data - Course Project

This is part of John Hopkins's "Getting and Cleaning Data" course project. Check coursera.org for more details about this course

### Details about Data to be worked out

One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

Here are the data for the project: 

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

#### Project Details

The purpose of this project is to demonstrate my ability to collect, work with, and clean above mentioned data set. The goal is to prepare tidy data that can be used for later analysis. This project delivers the following : 

1. A R code, run_analysis.R, which explains transformation steps to create tidy data set as per following requirement from provided data 
2. A code book that describes the variables, the data, and any transformations or work that I  performed to clean up the data called CodeBook.md.  

A R script called run_analysis.Ri has been created and  that does the following:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 
