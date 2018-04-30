This Code Book describes the columns and variables used in Dataset1 and Dataset2. Dataset1 is a tidy data set that shows a single row per experiment, and each of the values for each of these variables will reflect an observation or a calculated value from an observed value for each experiment. Dataset2 aggregates the rows for each subject and activity and shows the mean value for each of the remaining variables across all of the experiments for each of the activities that each test subject performed



subject
	Integer representing unique participant in experiment
 
activity_desc
	String description of activity being performed in experiment
		WALKING
		WALKING_UPSTAIRS
		WALKING_DOWNSTAIRS
		SITTING
		STANDING
		LAYING
 
tBodyAcc.mean...X 
	Numeric. Mean body acceleration in X axis

tBodyAcc.mean...Y 
	Numeric. Mean body acceleration in Y axis

tBodyAcc.mean...Z 
	Numeric. Mean body acceleration in Z axis

tGravityAcc.mean...X 
	Numeric. Mean gravity acceleration in X axis

tGravityAcc.mean...Y
	Numeric. Mean gravity acceleration in Y axis
 
tGravityAcc.mean...Z 
	Numeric. Mean gravity acceleration in Z axis

tBodyAccJerk.mean...X 
	Numeric. Mean body linear acceleration in X axis

tBodyAccJerk.mean...Y 
	Numeric. Mean body linear acceleration in Y axis

tBodyAccJerk.mean...Z 
	Numeric. Mean body linear acceleration in X axis

tBodyGyro.mean...X 
	Numeric. Mean body velocity in X axis

tBodyGyro.mean...Y 
	Numeric. Mean body velocity in Y axis

tBodyGyro.mean...Z 
	Numeric. Mean body velocity in Z axis

tBodyGyroJerk.mean...X 
	Numeric. Mean body angular velocity in X axis

tBodyGyroJerk.mean...Y 
	Numeric. Mean body angular velocity in Y axis

tBodyGyroJerk.mean...Z 
	Numeric. Mean body angular velocity in Z axis

tBodyAccMag.mean.. 
	Numeric. Mean body acceleration magnitude across three dimensional body acceleration vector

tGravityAccMag.mean.. 
	Numeric. Mean gravity acceleration magnitude across three dimensional gravity acceleration vector

tBodyAccJerkMag.mean.. 
	Numeric. Mean body linear acceleration magnitude across three dimensional body linear acceleration vector

tBodyGyroMag.mean.. 
	Numeric. Mean body velocity magnitude across three dimensional body gyroscopic velocity

tBodyGyroJerkMag.mean.. 
	Numeric. Mean body angular velocity magnitude across three dimensional body gyroscopic angular velocity

fBodyAcc.mean...X 
	Numeric. Fast fourier transform of tBodyAcc.mean...X

fBodyAcc.mean...Y 
	Numeric. Fast fourier transform of tBodyAcc.mean...Y

fBodyAcc.mean...Z 
	Numeric. Fast fourier transform of tBodyAcc.mean...Z

fBodyAccJerk.mean...X 
	Numeric. Fast fourier transform of tBodyAccJerk.mean...X 

fBodyAccJerk.mean...Y 
	Numeric. Fast fourier transform of tBodyAccJerk.mean...Y 

fBodyAccJerk.mean...Z 
	Numeric. Fast fourier transform of tBodyAccJerk.mean...Z

fBodyGyro.mean...X 
	Numeric. Fast fourier transform of tBodyGyro.mean...X 

fBodyGyro.mean...Y 
	Numeric. Fast fourier transform of tBodyGyro.mean...Y 

fBodyGyro.mean...Z 
	Numeric. Fast fourier transform of tBodyGyro.mean...Z

fBodyAccMag.mean.. 
	Numeric. Fast fourier transform of tBodyAccMag.mean..  
 
fBodyBodyAccJerkMag.mean.. 
	Numeric. Fast fourier transform of tBodyAccJerkMag.mean.. 

fBodyBodyGyroMag.mean..  
	Numeric. Fast fourier transform of tBodyGyroMag.mean..

fBodyBodyGyroJerkMag.mean.. 
	Numeric. Fast fourier transform of tBodyGyroJerkMag.mean.. 

angle.tBodyAccMean.gravity. 
	Numeric. Angle estimated from tBodyAccMean.gravity

angle.tBodyAccJerkMean..gravityMean. 
	Numeric. Angle estimated from tBodyAccJerkMean..gravityMean.

angle.tBodyGyroMean.gravityMean. 
	Numeric. Angle estimated from tBodyGyroMean.gravityMean.

angle.tBodyGyroJerkMean.gravityMean. 
	Numeric. Angle estimated from tBodyGyroJerkMean.gravityMean.

angle.X.gravityMean. 
	Numeric. Angle estimated from gravity mean in X axis

angle.Y.gravityMean. 
	Numeric. Angle estimated from gravity mean in Y axis

angle.Z.gravityMean. 
	Numeric. Angle estimated from gravity mean in Z axis

tBodyAcc.std...X 
	Numeric. Standard deviation of body acceleration in X axis

tBodyAcc.std...Y 
	Numeric. Standard deviation of body acceleration in Y axis

tBodyAcc.std...Z 
	Numeric. Standard deviation of body acceleration in Z axis

tGravityAcc.std...X 
	Numeric. Standard deviation of gravity acceleration in X axis

tGravityAcc.std...Y 
	Numeric. Standard deviation of gravity acceleration in Y axis

tGravityAcc.std...Z 
	Numeric. Standard deviation of gravity acceleration in Z axis

tBodyAccJerk.std...X 
	Numeric. Standard deviation of body linear acceleration in X axis

tBodyAccJerk.std...Y 
	Numeric. Standard deviation of body linear acceleration in Y axis

tBodyAccJerk.std...Z 
	Numeric. Standard deviation of body linear acceleration in Z axis

tBodyGyro.std...X 
	Numeric. Standard deviation of body velocity in X axis

tBodyGyro.std...Y 
	Numeric. Standard deviation of body velocity in Y axis

tBodyGyro.std...Z 
	Numeric. Standard deviation of body velocity in Z axis

tBodyGyroJerk.std...X 
	Numeric. Standard deviation of body angular velocity in X axis

tBodyGyroJerk.std...Y 
	Numeric. Standard deviation of body angular velocity in Y axis

tBodyGyroJerk.std...Z 
	Numeric. Standard deviation of body angular velocity in Z axis

tBodyAccMag.std.. 
	Numeric. Standard deviation of body acceleration magnitude across three dimensional body acceleration vector

tGravityAccMag.std.. 
	Numeric. Standard deviation of gravity acceleration magnitude across three dimensional gravity acceleration vector

tBodyAccJerkMag.std.. 
	Numeric. Standard deviation of body linear acceleration magnitude across three dimensional body linear acceleration vector

tBodyGyroMag.std.. 
	Numeric. Standard deviation of body velocity magnitude across three dimensional body gyroscopic velocity

tBodyGyroJerkMag.std.. 
	Numeric. Standard deviation of body angular velocity magnitude across three dimensional body gyroscopic angular velocity

fBodyAcc.std...X 
	Numeric. Fast fourier transform of tBodyAcc.std...X

fBodyAcc.std...Y 
	Numeric. Fast fourier transform of tBodyAcc.std...Y

fBodyAcc.std...Z 
	Numeric. Fast fourier transform of tBodyAcc.std...Z

fBodyAccJerk.std...X 
	Numeric. Fast fourier transform of tBodyAccJerk.std...X 

fBodyAccJerk.std...Y 
	Numeric. Fast fourier transform of tBodyAccJerk.std...Y

fBodyAccJerk.std...Z 
	Numeric. Fast fourier transform of tBodyAccJerk.std...Z

fBodyGyro.std...X 
	Numeric. Fast fourier transform of tBodyGyro.std...X

fBodyGyro.std...Y 
	Numeric. Fast fourier transform of tBodyGyro.std...Y

fBodyGyro.std...Z 
	Numeric. Fast fourier transform of tBodyGyro.std...Z

fBodyAccMag.std.. 
	Numeric. Fast fourier transform of tBodyAccMag.std..  
 
fBodyBodyAccJerkMag.std.. 
	Numeric. Fast fourier transform of tBodyAccJerkMag.std.. 

fBodyBodyGyroMag.std..  
	Numeric. Fast fourier transform of tBodyGyroMag.std..

fBodyBodyGyroJerkMag.std.. 
	Numeric. Fast fourier transform of tBodyGyroJerkMag.std.. 