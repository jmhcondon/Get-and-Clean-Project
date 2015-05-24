**** Please refer to the README.md for a detailed explanation of the script or how the table was created, including all transformations of the original dataset.*****

**** The "sub_act_feature_avgs.txt" file was created by write.table() in R.  To view it properly please use read.table. *****

This is the codebook describing the independent tidy data set withthe average of each selected 
mean and standard deviation variable for each activity and each subject.

Each row consists of the average value for each of the selected measurements on the mean and standard deviation 
feature for a single subject performing a single activity. Each subject performed each of the 
six activities, Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, and Laying, numbered 1 to 6 respectively.  
Since 30 subjects participated, this results in 30 subjects by 6 activities each, for a total of 180 rows.  
Each row has 66 columns, one for the average value of all the observation for the 66 mean and std features 
for that subject performing that activity. Also, all the column features names have been simplified and made 
syntactically correct.


*** DATASET COLUMNS ***
These are the columns in the dataset. There are 66 average and standard deviation feature variable columna, 
plus one for the subject and one for the activity and another for the activity number.  The order of the variables 
refects their order in the data set.

 subject 
 - The subject who was being tested.  A number from 1 to 30.
 
 activitycode 
 - A number associated with each activity performed by each subject in the research trials.  A number from 1 to 6.
 
 activityname 
- One the 6 activities performed by each subjects that was measured by the Samsung Galaxy S smartphone 
- accelerometer and gyroscope.  These were:
1. Walkinig
2. Walking Upstaires
3. Walking Downstairs
4. Sitting
5. Standing
6. Laying

**** Averaged mean and standard deviation features

[Note: All features being averaged were originally normalized and bounded within
[-1,1] 

 tBodyAcc.mean.X 
 tBodyAcc.mean.Y 
 tBodyAcc.mean.Z 
 tBodyAcc.std.X 
 tBodyAcc.std.Y 
 tBodyAcc.std.Z 

These are the averaged mean and standard deviation of total linear acceleration due to the mass of the subject's body.  
Linear acceleration was recorded along the X, Y, and Z axes r by the Samsung smartphone's accelerometer. 
They are measured within the time domain and had original measurements had units of standard gravity "g'.  

 tGravityAcc.mean.X 
 tGravityAcc.mean.Y 
 tGravityAcc.mean.Z 
 tGravityAcc.std.X 
 tGravityAcc.std.Y 
 tGravityAcc.std.Z 
 
 These are the averaged mean and standard deviation of total linear acceleration due to gravity alone.  
 Linear acceleration was recorded along the X, Y, and Z axes r by the Samsung smartphone's accelerometer. 
 They are measured within the time domain and had original measurements had units of standard gravity "g'.  
 
 tBodyAccJerk.mean.X 
 tBodyAccJerk.mean.Y 
 tBodyAccJerk.mean.Z 
 tBodyAccJerk.std.X 
 tBodyAccJerk.std.Y 
 tBodyAccJerk.std.Z 
 
 These are the averaged mean and standard deviation due to the subject's body of linear acceleration jerk, 
 or the change in linear acceleration.  Jerk was derived by taking the derivative of linear acceleration
 along the X, Y, and Z axes. 

 tBodyGyro.mean.X 
 tBodyGyro.mean.Y 
 tBodyGyro.mean.Z 
 tBodyGyro.std.X 
 tBodyGyro.std.Y 
 tBodyGyro.std.Z
 
 These are the averaged mean and standard deviation of total angular velocity due to the mass of the subject's body.  Angular velocity was recorded along the X, Y, and Z axes r by the Samsung smartphone's gyroscope. They are measured within the time domain and had original measurements  units of radians/sec.  
  
 tBodyGyroJerk.mean.X 
 tBodyGyroJerk.mean.Y 
 tBodyGyroJerk.mean.Z 
 tBodyGyroJerk.std.X 
 tBodyGyroJerk.std.Y 
 tBodyGyroJerk.std.Z 
 
 These are the averaged mean and standard deviation due to the subject's body of angular acceleration jerk, 
 or the change in angular acceleration.  Jerk was derived by taking the second derivative of angular velocity 
 along the X, Y, and Z axes.  It has units of radians per second^3

 tBodyAccMag.mean 
 tBodyAccMag.std 
 tGravityAccMag.mean 
 tGravityAccMag.std 
 tBodyAccJerkMag.mean 
 tBodyAccJerkMag.std 
 tBodyGyroMag.mean 
 tBodyGyroMag.std 
 tBodyGyroJerkMag.mean 
 tBodyGyroJerkMag.std 
 
 These measures are the mean and standard deviations of the magnitude (mag) of the underlying feature. 
 All of the above features are based on the original time domain signal from the Samsung phone, 
 as denoted by the leading 't'.
 
 fBodyAcc.mean.X 
 fBodyAcc.mean.Y 
 fBodyAcc.mean.Z 
 fBodyAcc.std.X 
 fBodyAcc.std.Y 
 fBodyAcc.std.Z 
 fBodyAccJerk.mean.X 
 fBodyAccJerk.mean.Y 
 fBodyAccJerk.mean.Z 
 fBodyAccJerk.std.X 
 fBodyAccJerk.std.Y 
 fBodyAccJerk.std.Z 
 fBodyGyro.mean.X 
 fBodyGyro.mean.Y 
 fBodyGyro.mean.Z 
 fBodyGyro.std.X 
 fBodyGyro.std.Y 
 fBodyGyro.std.Z 
 fBodyAccMag.mean 
 fBodyAccMag.std 
 fBodyBodyAccJerkMag.mean 
 fBodyBodyAccJerkMag.std 
 fBodyBodyGyroMag.mean 
 fBodyBodyGyroMag.std 
 fBodyBodyGyroJerkMag.mean 
 fBodyBodyGyroJerkMag.std 

All of these features are the result of applying a Fast Fourier Transform (FFT) 
to transform the time domain signal to a frequency domain signal. This is denoted by the leading 'f'.

*** Table Row Organization

Each row represents summary of all the experimental observations od one subject's (numbered 1 to 6) 
performance on one of the six activities.  The rows are grouped by subject and activity, therefore 
each subject has six consecutive rows, one for each activity.  This group of 6 row for each subject 
is ordered by the subject id (1 o 30, and the activity code (1 to 6).  There are a total of 180 rows, 
each with the same 69 columsn described above.




