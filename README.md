Dataset information
--------------------
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. 

Check the README.txt file for further details about this dataset.
source: [http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones] 



Feature names
-------------
In the tidy dataset, there are feature names(variable names), subject and activity names, also contains data part( xtrain, xtest). Features.txt contains 68 variables names that contains symbol"()-" , "-std", "-mean", and other names that need to replaced or renamed or even deleted. Those variables names are transformed to a cleaned named in tidy data.
See as below:

|raw data variable names     |    tidy data variable names   |
|---------------------------:|:-----------------------------:|
| tBodyAcc-mean()-X          |     tBodyAccMeanX             |
 tBodyAcc-mean()-Y           |     tBodyAccMeanY             |
 tBodyAcc-mean()-Z           |     tBodyAccMeanZ            |
 tBodyAcc-std()-X            |     tBodyAccStdX             |
 tBodyAcc-std()-Y            |     tBodyAccStdY             |
 tBodyAcc-std()-Z            |     tBodyAccStdZ             |
 tGravityAcc-mean()-X        |     tGravityAccMeanX         |
 tGravityAcc-mean()-Y        |     tGravityAccMeanY         |
 tGravityAcc-mean()-Z        |     tGravityAccMeanZ
 tGravityAcc-std()-X         |     tGravityAccStdX
 tGravityAcc-std()-Y         |      tGravityAccStdY
 tGravityAcc-std()-Z         |      tGravityAccStdZ
 tBodyAccJerk-mean()-X       |      tBodyAccJerkMeanX
 tBodyAccJerk-mean()-Y       |      tBodyAccJerkMeanY
 tBodyAccJerk-mean()-Z      |      tBodyAccJerkMeanZ
 tBodyAccJerk-std()-X       |      tBodyAccJerkStdX
 tBodyAccJerk-std()-Y       |      tBodyAccJerkStdY
 tBodyAccJerk-std()-Z       |      tBodyAccJerkStdZ
 tBodyGyro-mean()-X         |      tBodyGyroMeanX
 tBodyGyro-mean()-Y         |      tBodyGyroMeanY
 tBodyGyro-mean()-Z         |      tBodyGyroMeanZ
 tBodyGyro-std()-X          |      tBodyGyroStdX
 tBodyGyro-std()-Y          |      tBodyGyroStdY
 tBodyGyro-std()-Z          |      tBodyGyroStdZ
 tBodyGyroJerk-mean()-X     |      tBodyGyroJerkMeanX
 tBodyGyroJerk-mean()-Y     |      tBodyGyroJerkMeanY
 tBodyGyroJerk-mean()-Z     |      tBodyGyroJerkMeanZ
 tBodyGyroJerk-std()-X      |      tBodyGyroJerkStdX
 tBodyGyroJerk-std()-Y      |      tBodyGyroJerkStdY
 tBodyGyroJerk-std()-Z      |      tBodyGyroJerkStdZ
 tBodyAccMag-mean()         |      tBodyAccMagnitudeMean 
 tBodyAccMag-std()          |      tBodyAccMagnitudeStd
 tGravityAccMag-mean()      |      tGravityAccMagnitudeMean
 tGravityAccMag-std()       |      tGravityAccMagnitudeStd
 tBodyAccJerkMag-mean()     |     tBodyAccJerkMagnitudeMean
 tBodyAccJerkMag-std()      |     tBodyAccJerkMagnitudeStd
 tBodyGyroMag-mean()        |      tBodyGyroMagnitudeMean
 tBodyGyroMag-std()         |      tBodyGyroMagnitudeStd
 tBodyGyroJerkMag-mean()    |      tBodyGyroJerkMagnitudeMean
 tBodyGyroJerkMag-std()     |      tBodyGyroJerkMagnitudeStd
 fBodyAcc-mean()-X          |      fBodyAccMeanX
 fBodyAcc-mean()-Y          |      fBodyAccMeanY
 fBodyAcc-mean()-Z          |      fBodyAccMeanZ
 fBodyAcc-std()-X           |      fBodyAccMeanX
 fBodyAcc-std()-Y           |      fBodyAccMeanY
 fBodyAcc-std()-Z           |      fBodyAccMeanZ
 fBodyAccJerk-mean()-X      |      fGravityAccMeanX  
 fBodyAccJerk-mean()-Y      |      fGravityAccMeanY
 fBodyAccJerk-mean()-Z      |      fGravityAccMeanZ
 fBodyAccJerk-std()-X       |      fGravityAccMeanX
 fBodyAccJerk-std()-Y       |      fGravityAccMeanY
 fBodyAccJerk-std()-Z       |      fGravityAccMeanZ
 fBodyGyro-mean()-X         |     ftBodyGyroMeanX  
 fBodyGyro-mean()-Y         |      fBodyGyroMeanX
 fBodyGyro-mean()-Z         |     fBodyGyroMeanX
 fBodyGyro-std()-X          |      fBodyGyroStdX
 fBodyGyro-std()-Y          |     fBodyGyroStdX   
 fBodyGyro-std()-Z          |     fBodyGyroStdX
 fBodyAccMag-mean()         |      fBodyAccMagnitudeMean
 fBodyAccMag-std()          |      fBodyAccMagnitudeStd
 fBodyAccJerkMag-mean()     |     fBodyAccJerkMagMean
 fBodyAccJerkMag-std()      |      fBodyAccJerkMagStd
 fBodyGyroMag-mean()        |      fBodyGyroMagnitudeMean
 fBodyGyroMag-std()         |      fBodyGyroMagnitudeStd
 fBodyGyroJerkMag-mean()    |      fBodyGyroJerkMagnitudeMean 
 fBodyGyroJerkMag-std()     |      fBodyGyroJerkMagnitudeStd


Transformation method: 
* replace "-std" with "Std" : Upper case is needed.
* remove "()-": means : making names better to look at same time shorter.
* replace "-mean" with "Mean": means we use Upper case if needed.
* replace "Mag" with "Magnitude": means replace it with whole names will be clearer to understand.


Activity names
----------
There are 6 numbers to stand the 6 activities names. They can be seen below:

|    number     |   names           |
|--------------:|------------------:|
|       1       | walking           |
|       2       | walking_upstairs  |
|       3       | walking_downstairs|
|       4       | sitting           |
|       5       | standing          | 
|       6       | laying            |


Summary of scripts 
----------------------
* In the repository there are run_analysis.R, README.md, tidyMeans data.txt, and the code book.txt.
* Created and run the "run_analysis.R" , first it unzip files from website given:https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

* Then it read in data use read.table and assign them with names by using read.table() command.
* Combine data and divide them into 3 parts and assign names to those three parts by using cbind and rbind command.
* extract only measurements on the mean and standard deviation for each measurement.
* use descriptive activity names to name the activities in the data set.
* clean data and combine them into one set.
* clean variable names by using gsub() command, then saved as tidy data.txt.
* Then save a dataset called cleaned_data then exclude columns of activity and subject. That way we 
* create a second, independent tidy data set with average of each variable for each activity and each subject.
* Got a tidy data set with avergae of each variable for each activity and subject, called tidyMeans data.txt 


