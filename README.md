coursera_getdata-006
====================

Here are the data for the project:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

A R script called run_analysis.R was created that does the following: 

* Merges the training and the test sets to create one data set.
* Extracts only the measurements on the mean and standard deviation for each measurement. 
* Uses descriptive activity names to name the activities in the data set
* Appropriately labels the data set with descriptive variable names. 
* Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 

## To run: 
* unzip the data for project into some directory with read write access (e.g. c:\temp)
* copy run_analysis.R there;
* set working directory there in R-Studio (either use setwd() or use GUI);
* run following in R-Studio: 
    source("run_analysis.R")
* it will run the file and the following will be generated:
    ** merged_data.txt:   33 means / 33 std features are extracted;
    ** data_set_with_average:    descriptive label names are grabbed from activity_labels.txt(in original data) and a tidy data set was created with the average of each 
    
  