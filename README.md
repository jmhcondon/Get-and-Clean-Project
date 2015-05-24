**************
The "sub_act_feature_avgs.txt" file output by the script was created by write.table() using row.name=FALSE. To view it
properly in R please use read.table() using row.name=FALSE.
**************

**************
To run the script the files created from unzipping samsung_exercise_data.zip must be in the working directory. The zip file may be downloaded at the following URL:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles% 2FUCI%20HAR%20Dataset.zip

A full description of the dataset is available at:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition +Using+Smartphones
**************

The is the README.md for the Get and Clean course project.  The purpose of the assignment
was to demonstrate the ability to collect, work with and clean a data set. The goal was to
prepare a tidy data set that could be used for later analysis.

It is intended to accompany the run_analysis.R script and the the tidy data set
"sub_act_features_avg.txt" that is generated by the script. It is designed to describwe how the script works, background of
the data being collecte and worked, a detailed discussion of the variables, and the transformations made by the scripyt
in order to create the final tidy data set. 

**************
See CodeBook.md for a list and description of the variables and structure of the tidy dataset generated 
by the script.
**************

The project uses data generated by the Human Activity Recognition Using Smartphones data
set from experiments conducted by Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio,
Luca Oneto of the Smartlab - Non Linear Complex Systems Laboratory DITEN - Universit‡
degli Studi di Genova. Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws www.smartlab.ws

This data set was made available at the following URL:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles% 2FUCI%20HAR%20Dataset.zip

A full description of the dataset is available at:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition +Using+Smartphones

The readMe which accompanies the dataset describes the experiments and the individual
datasets provided. I'll exerpt some of the most important information below.

DESCRIPTION OF THE EXPERIMENT

The experiments have been carried out with a group of 30 volunteers within an age bracket
of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS,
WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II)
on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear
acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have
been video-recorded to label the data manually. The obtained dataset has been randomly
partitioned into two sets, where 70% of the volunteers was selected for generating the
training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise
filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128
readings/window). The sensor acceleration signal, which has gravitational and body motion
components, was separated using a Butterworth low-pass filter into body acceleration and
gravity. The gravitational force is assumed to have only low frequency components,
therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of
features was obtained by calculating variables from the time and frequency domain.

DESCRIPTION OF THE EXPERIMENTAL FEATURES CAPTURED

The features_info.txt file described in some detail the data included in the complete
dataset.

*********** BEGIN EXTRACT ****************

Feature Selection =================

The features selected for this database come from the accelerometer and gyroscope 3-axial
raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time)
were captured at a constant rate of 50 Hz. Then they were filtered using a median filter
and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove
noise. Similarly, the acceleration signal was then separated into body and gravity
acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth
filter with a corner frequency of 0.3 Hz.

Subsequently, the body linear acceleration and angular velocity were derived in time to
obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these
three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag,
tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag).

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing
fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag,
fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals).

These signals were used to estimate variables of the feature vector for each pattern:
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ
tGravityAcc-XYZ 
tBodyAccJerk-XYZ 
tBodyGyro-XYZ 
tBodyGyroJerk-XYZ 
tBodyAccMag
tGravityAccMag 
tBodyAccJerkMag 
tBodyGyroMag 
tBodyGyroJerkMag 
fBodyAcc-XYZ 
fBodyAccJerk-XYZ
fBodyGyro-XYZ 
fBodyAccMag 
fBodyAccJerkMag 
fBodyGyroMag 
fBodyGyroJerkMag

The set of variables that were estimated from these signals are:

mean(): Mean value 
std(): Standard deviation 
mad(): Median absolute deviation 
max(): Largest value in array 
min(): Smallest value in array 
sma(): Signal magnitude area
energy(): Energy measure. Sum of the squares divided by the number of values. 
iqr(): Interquartile range 
entropy(): Signal entropy 
arCoeff(): Autorregresion coefficients with Burg order equal to 4 
correlation(): correlation coefficient between two signals
maxInds(): index of the frequency component with largest magnitude mean
Freq(): Weighted average of the frequency components to obtain a mean frequency skewness(): 
skewness of the frequency domain signal 
kurtosis(): kurtosis of the frequency domain signal 
bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window. 
angle(): Angle between to vectors.

Additional vectors obtained by averaging the signals in a signal window sample. These are
used on the angle() variable:

gravityMean 
tBodyAccMean 
tBodyAccJerkMean 
tBodyGyroMean 
tBodyGyroJerkMean


DATA PROVIDED IN THE DATASET

Each record provides: 
- Triaxial(XYZ) acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

FILES CONTAINED IN THE DATASET

The dataset includes the following files:

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector. 
- 'features.txt': List of all features. 
- 'activity_labels.txt': Links the class labels with their activity name. 
- 'train/X_train.txt': Training set. 
- 'train/y_train.txt': Training labels. 
- 'test/X_test.txt': Test seT. 
- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are
equivalent. - 'train/subject_train.txt' Each row identifies the subject who performed the
activity for each window sample. Its range is from 1 to 30.

- 'train/Inertial Signals/total_acc_x_train.txt' The acceleration signal from the
smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128
element vector. The same description applies for the'total_acc_x_train.txt' and
'total_acc_z_train.txt' files for the Y and Z axis.

- 'train/Inertial Signals/body_acc_x_train.txt' The body acceleration signal obtained by
subtracting the gravity from the total acceleration.

- 'train/Inertial Signals/body_gyro_x_train.txt' The angular velocity vector measured by
the gyroscope for each window sample. The units are radians/second.

*********** END EXTRACT ****************

VARIABLE UNITS

Accelerometer Units - standard gravity units 'g'

As the descriptions above noted, accelerometer measurements are measured in standardd units of g, or the gravitational force at the surface of the earth. Wikipedia describes it as "a measure of the type of acceleration that indirectly causes weight...It is a type of acceleration that can be measured with an accelerometer."

Gyroscope Units - radians/seconds

A gyroscope measures the rate of rotation in radians around each of the x, y, and z axes. 
in aviation terms these are called pitch, yaw, and roll.This is also known as angular
velocity. which wikipedia describes as "the rate of change of angular displacement and is
a vector quantity which specifies the angular speed (rotational speed) of an object and
the axis about which the object is rotating."  Again there are the same three X,Y, abd Z
axes which together describe three dimensional space.

WHAT IS JERK?

Wikipedia describes Jerk this way:

"In physics, jerk, also known as jolt, surge, or lurch, is the rate of change of acceleration; that is, the derivative of acceleration with respect to time, and as such the second derivative of velocity, or the third derivative of position."

Rotational jerk is derived from the angular velocity.  The first derivative, angular acceleration, measures the rate of change in the angular velocity.  Wikipedia explains "the angular acceleration corresponds to the quotient of the torque acting on the body and the moment of inertia of the body with respect to the momentary axis of rotation. An abrupt change of the torque results in an important angular jerk."

THE PROJECT ASSOIGMENT

The directions provided for the assignment were to create one R calledrun_analysis.R that
performed 5 steps:

	1. Merges the training and the test sets to create one data set. 
	2. Extracts only the measurements on the mean and standard deviation for each measurement. 
	3. Uses descriptive activity names to name the activities in the data set 
	4. Appropriately labels the data set with descriptive variable names. 
	5. From the data set in step 4, creates a second, independent tidy data set with 
	   the average of each variable for eac activity and each subject.
	
DESIGN CONSIDERATIONS

******* Input to the script

The script takes as input the Samsung Galaxy S smartphone data generated by the "Human
 Activity Recognition Uing Smartphones". It was downloaded as a zip data set using this
 link: 
 https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The unzipped file obtained through this link is samsung_exercise_data.zip.  When unzipped is results in the set of files described earlier.  These are contained in the directory structure /UCI HAR Dataset/test and /UCI HAR Dataset/train.
The test and train subdirectories contain the x_test.txt, y_test.txt, and subject_test.txt, and the x_train.txt, y_train.txt, and subject_train.txt files respectively.  Other files used by the script are in the paraent UCI HAR Dataset.

The script requires that the unzipped files in UCI HAR Dataset be availble from the working directory. 

******* Structure of the script

The script is organized by the 5 steps specified in the project requirements.

 **** Step 1: Merge the training and test sets

As just described, the full data set had been randomly divided by the researchers into training and test data sets. This was done as part of the effort to create a statistical model that could identify an action from the the only feature information.

 The 10299 observations of 561 variables were divided into training and test sets,
 containing 7352 and 2947 observations respectively.  These are merged into a single
 data frame containing all 10299 observation row and 561 feature attribute columns. This was namesd observations.
 
 The subject and y training and test datasets are likewise merged. Each contains the same 10299 rows as the feature measurements contained in the merged x_data dataset.

 **** Step 2: Extract obnly the measurements on the mean and standard ddeviation for each
 measurement

 The features.txt file was read into the features table. It contains the names for each of the 561 features that were captured during each experimental observation and that correspond to the columns in the merged x_test and x_train datasets.
 
 A regular expression was used with grep to extract only feature with both mean and standard deviations values.  There were 66 features that matched the regular expression. These included features that included mean() or std() in their names. Grep was run 2 times, once to obtain a vector of column numbers to extract, and once to extract the column names of the selected features. The selected features were captured in the mean_std_features_ [select|names] vectors.
 
The mean_std_features_select vector was used to subset the full observations table to just the desired mean and std set of columns.  The selected feature names were applied to the extracted column vaeriables as a starting point for providing more descriptive labels. The result was named the observations_mean_std table.

**** Step 3: Use descriptive activity names to name the activities in the data set

 The y data refers to each observational row, while the x data each column.The y data
 allows us to link a specific activity to each experimental observation row.  To begin, we
 the y_train and y_test data were merged into a single data frame. The resulting daa frame was named activty_linkage. 
 The names and number of the 6 activities wdere contained in the activity_labels.txt file, which was loaded into the activity_names data frame. 
 
 Dplyr was used to join to activity_linkage and activity_names to create a table of the activity being measured in each obserrvation trial. The resulting table, observation_activity, has 10299 rows, equal to the number of observational trials. It contains two variables, activity code and activity name.

 We now needed to merge subjects with the activities being monitored in eacb row of the
 observtional data. First, we needed to merge the subject training and testing data sets
 back into a single subjects data frame. The single column was named subject.  Each row has the number of the subject 
 tested in that experimental trial.

 We could then merge the subjects and observation_activity columns to the leftmost side of the observationss_mean_std table.	This reconstructed the original structure of the experimental observation data. Now each contains the measurements from one trial of one subject performing one activity.

*** Step 4: Appropriately label the data set with descriptive variable names

 As described earlier, we initially used the original names from the feature.txt file for the mean and std features selected by the grep pattern match.

 As a next step wee used make.names to transform the original feature.txt names to syntactically valid names. Help for makes.names says that a syantactically valid name: consists of letters, numbers and the dot or underline characters and starts with a letter or the dot not followed by a number... All invalid characters are translated to "."

 A side effect of make.names was that it generated names wih multiple periods where invalid characters were removed. We wanted to limit these to a single "." .  We used the sub() function to look for patterns of two periods  ".." or three periods "..." and replaced them with a single period.  This resulted in much cleaner variable names, that were still consistent with the original names used by the researchers.
 
 The result is that each of the 66 feature names has been rationalized and simplified,  For example, the feature named  "tBodyAcc-mean()-X"  is now "tBodyAcc.mean.X".

**** Step 5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
	
To create the second table, we first used the dplyr group_by() function to create a data frame grouped by subject and activity name.  We then used summarize_each() on the grouped table taking the average of each variable within each subject activty grouping. Finally we ordered the resulting table by activity within subject, generating the final tidy table.

Each row consists of the average value for each mean and standard deviation feature for a single subject performing a single activity. Each subject performed each of the six activities, Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, and Laying, numbered 1 to 6 respectively.  Since 30 subjects participated, this results in 30 subjects by 6 activities each, for a total of 180 rows.  Each row has 66 columns, one for he average value of all the observation for the 66 features for that subject performing that activity. Also, all the column features names have been simplified and made syntactically correct.

The resulting tidy data set was output to a text file named "sub_act_feature_avgs.txt" using write_table. 
