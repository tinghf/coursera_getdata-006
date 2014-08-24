coursera_getdata-006
====================

# Source data description
Source data:
  https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
A full description is available at the site where the data was obtained:
  http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

# R script description
  
R script (run_analysis.R) performs the following to clean up the data:

* read in the training and test sets, merge them to create one data set
    - train/X_train.txt with test/X_test.txt: a 10299 x 561 data frame, as in the original description ("Number of Instances: 10299" and "Number of Attributes: 561")
    - train/subject_train.txt with test/subject_test.txt: a 10299 x 1 data frame with subject IDs,
    - train/y_train.txt with test/y_test.txt: a 10299 x 1 data frame with activity IDs.

* extracts only the measurements (features) on the mean and standard deviation for each measurement appropriately labels the columns with descriptive names
The result is a 10299 x 66 data frame, as 66 out of 561 attributes are measurements on the mean and standard deviation.

* replaces activity values in the dataset with descriptive activity names from features.txt

* Reads activity_labels.txt and applies descriptive activity names to name the activities in the data set:
    - walking
    - walkingupstairs
    - walkingdownstairs
    - sitting
    - standing
    - laying

* creates a second, independent tidy dataset with an average of each variable for each each activity and each subject. Export it as a csv file.

* The script also appropriately labels the data set with descriptive names, all feature names (attributes) and activity names are converted to lower case, underscores and brackets are removed.

* Then it merges the 10299x66 data frame containing features with 10299x1 data frames containing activity labels and subject IDs.

* The result is saved as merged_data.txt, a 10299x68 data frame such that the first column contains subject IDs,
the second column activity names, and the last 66 columns are measurements. Subject IDs are integers between 1 and 30 inclusive.

* Finally, the script creates a second independent tidy data set with the average of each measurement for each activity/subject.

* The result is saved as data_set_with_average.txt, a 180x68 data frame, where as before, the first column contains subject IDs, the second column contains activity names (see below), and then the averages for each of the 66 attributes are in columns 3...68. There are 30 subjects and 6 activities, thus 180 rows in this data set with averages.

