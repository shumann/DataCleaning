## Data Description for Tidy Data

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

## Data Dictionary for Tidy Data

  Subject
    Subject identifier undergoing the experiment
    Integer
    Values : 1 to 30
    
  Activity
    The activity of the subjects that were measured
    Factor: 6 Levels
      1              WALKING
      2     WALKING_UPSTAIRS
      3   WALKING_DOWNSTAIRS
      4              SITTING
      5             STANDING
      6               LAYING
    
  tBodyAcc_mean_X to Z
    Mean computed for body acceleration per subject per activity
    Numeric
  
  tBodyAcc_std_X to Z 
    Standard Deviation computed for body acceleration per subject per activity
    Numeric
  
  tGravityAcc_mean_X to Z
    Mean computed for gravity acceleration per subject per activity
    Numeric
  
  tGravityAcc_std_X to Z 
    Standard Deviation computed for gravity acceleration acceleration
    Numeric
    
  tBodyAccJerk_mean_X to Z
    Mean computed for body jerk acceleration per subject per activity
    Numeric
  
  tBodyAccJerk_std_X to Z 
    Standard Deviation computed for body jerk acceleration per subject per activity
    Numeric  

  tBodyGyro_mean_X to Z
    Mean computed for  gyroscope body acceleration per subject per activity
    Numeric
  
  tBodyGyro_std_X to Z 
    Standard Deviation computed for gyroscope body acceleration per subject per activity
    Numeric
    
  tBodyGyroJerk_mean_X to Z
    Mean computed for gyroscope body jerk acceleration per subject per activity
    Numeric
  
  tBodyGyroJerk_std_X to Z 
    Standard Deviation computed for gyroscope body jerk acceleration per subject per activity
    Numeric 
 
  tBodyGyroJerk_mean_X to Z
    Mean computed for gyroscope body jerk acceleration per subject per activity
    Numeric
  
  tBodyGyroJerk_std_X to Z 
    Standard Deviation computed for gyroscope body jerk acceleration per subject per activity
    Numeric   

  tBodyAccMag_mean 
    Mean of Mag Body acceleration per subject per activity
    Numeric  
  
  tBodyAccMag_std  
    Standard Deviation of Mag Body acceleration per subject per activity
    Numeric  
  
  tGravityAccMag_mean
    Mean of gravity acc per subject per activity
    Numeric
    
  tGravityAccMag_std
    Standard Deviation of gravity acc per subject per activity
    Numeric
    
  tBodyAccJerkMag_mean
    Mean of body acc per subject per activity
    Numeric
    
  tBodyAccJerkMag_std
    Standard Deviation of gravity acc per subject per activity
    Numeric    
    
  tBodyGyroJerkMag_mean
    Mean of body gyro jerk acc per subject per activity
    Numeric
    
  tBodyGyroJerkMag_std
    Standard Deviation of body gyro jerk acc per subject per activity
    Numeric           

  fBodyAcc_mean_X to Z
    Mean computed for Fourier transform on body acceleration per subject per activity
    Numeric
  
  fBodyAcc_std_X to Z 
    Standard Deviation computed for Fourier transform on body acceleration per subject per activity
    Numeric
 
  fBodyAcc_meanFreq_X to Z
     Mean computed for Fourier transform on body acceleration frequency per subject per activity
     Numeric
  
  fBodyAccJerk_mean_X to Z
    Mean computed for Fourier transform on jerk body acceleration per subject per activity
    Numeric
  
  fBodyAccJerk_std_X to Z 
    Standard Deviation computed for Fourier transform on jerk body acceleration per subject per activity
    Numeric

  fBodyAccJerk_meanFreq_X to Z
    Mean computed for Fourier transform on frequency ofjerk body acceleration per subject per activity
    Numeric
    
  fBodyGyro_std_X to Z 
    Standard Deviation computed Fourier transform for gyroscope body measurement per subject per activity
    Numeric
    
  fBodyGyroJerk_mean_X to Z
    Mean computed for Fourier transform gyroscope body jerk acceleration per subject per activity
    Numeric

  fBodyGyroJerk_meanFreq_X to Z
    Mean computed for Fourier transform on frequency Gyro body per subject per activity
    Numeric
 
  fBodyAccMag_mean             
  Numeric
  
  fBodyAccMag_std 
  Numeric
  
  fBodyAccMag_meanFreq  
  Numeric
  
  fBodyBodyAccJerkMag_mean 
  numeric
  
  fBodyBodyAccJerkMag_std      
  Numeric
  
  fBodyBodyAccJerkMag_meanFreq 
  Numeric
  
  fBodyBodyGyroMag_mean       
  Numeric
  
  fBodyBodyGyroMag_std         
  Numeric
  
  fBodyBodyGyroMag_meanFreq    
  Numeric
  
  fBodyBodyGyroJerkMag_mean 
  Numeric
  
  fBodyBodyGyroJerkMag_std   
  Numeric
  
  fBodyBodyGyroJerkMag_meanFreq
  Numeric
  
## Process applied on Raw Data. 

The process:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 
