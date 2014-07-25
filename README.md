## The Course Program meets the following intent 

The R Program (run_analysis.R):

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 

## Process followd

1. To aid the peer review only one file was created with complete data sourcing and cleaning.
2. All means and standard deviations were extracted. No programmer's judgement was applied to arrive at the inclusion or exclusion of means.
3. The descriptive column names were applied before the extraction of required measurements. 
   The reason is to keep the file future ready when other columns may also be required for separate analysis. 
4. The column names were processed for comma, hyphen only. The hyphens were replaced with "_" (underscore) for easy reference to column names.
5. The mix of cases (upper and lower) in column names were not disturbed as they do not hinder readability.

## Steps

1. The downloaded files were unzipped in data repository
2. All data files were read into respetive data frames
3. All train data were consolidated into "consolidated_train" data frame
4. All test data were consolidated into  "consolidated_test" data frame
5. Test and train data were consolidated "consolidated_all" data frame
6. The feature (measurement) names were cleaned up and stored in 'f_all_m"
6. The subject and activity were added and all columns were renamed from "f_all_m" into data frame "consolidated_all"
7. The required measurement variables having "meean" and "std" embedded in variable names were extrated to a new dataframe "consolidated_mean_std"
8. The descritive label names were substituted from "activity_labeltxt" into "consolidated_data_merged"
9. The dataframe "tidy_data"" was created to get group means by "Subject"" and "Activity"" for extrated measurements.
10. The text file "tide_data.txt" was created  for submission.
