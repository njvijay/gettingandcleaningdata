
### Data Set:

- [source](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) 
- [description](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)


### Steps to be performed on Data Transformation

Following data transformations are carried out by the run_analysis.R script.

1. For each of the training and test datasets, 
    1. First,read the X values
    2. Grep to subset columns which are representing only the mean and standard deviation values. 
    3. Associate additional columns to represent activity IDs and subject IDs read from y_<dataset>.txt and subject_<dataset>.txt files respectively.
    4. Assign column names by manipulating the measurement names in features.txt.
2. Merge the training and the test sets.
3. Associate an additional column with descriptive activity names as specified in activity_labels.txt.
4. Melt the dataset by specifying activity ID, name and subject ID as the only ID variables.
5. Re cast the melted dataset with activity name and subject id as the only IDs and mean as the aggregator function.
6. Save the result in re-casted dataset as tidy_data_mean.txt


### Variable Descriptions

The data for this data set was derived from sources mentioned in the "Data Set" section of this document. 

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz.

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag).

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals).

These signals were used to estimate variables of the feature vector for each pattern: '-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

The set of variables that were estimated from these signals are:
- mean: Mean value
- std: Standard deviation

#### Data Columns

Total 82 columns available with tidy data set.

subject - lists the subjects assigned number in the original experiment

activityName is a factor indicating the activity type

activityID - A ID number assigned to each activity Name

activityID and activityName listed below

1 WALKING
2 WALKING_UPSTAIRS
3 WALKING_DOWNSTAIRS
4 SITTING
5 STANDING
6 LAYING

The rest of the variables are the same as in the original data set which represents mean and standard deviation,  and the second processed data set lists averages over all observations in a group:

Here is the list of all available columns

1	subject
2	tBodyAcc-mean()-X
3	tBodyAcc-mean()-Y
4	tBodyAcc-mean()-Z
5	tBodyAcc-std()-X
6	tBodyAcc-std()-Y
7	tBodyAcc-std()-Z
8	tGravityAcc-mean()-X
9	tGravityAcc-mean()-Y
10	tGravityAcc-mean()-Z
11	tGravityAcc-std()-X
12	tGravityAcc-std()-Y
13	tGravityAcc-std()-Z
14	tBodyAccJerk-mean()-X
15	tBodyAccJerk-mean()-Y
16	tBodyAccJerk-mean()-Z
17	tBodyAccJerk-std()-X
18	tBodyAccJerk-std()-Y
19	tBodyAccJerk-std()-Z
20	tBodyGyro-mean()-X
21	tBodyGyro-mean()-Y
22	tBodyGyro-mean()-Z
23	tBodyGyro-std()-X
24	tBodyGyro-std()-Y
25	tBodyGyro-std()-Z
26	tBodyGyroJerk-mean()-X
27	tBodyGyroJerk-mean()-Y
28	tBodyGyroJerk-mean()-Z
29	tBodyGyroJerk-std()-X
30	tBodyGyroJerk-std()-Y
31	tBodyGyroJerk-std()-Z
32	tBodyAccMag-mean()
33	tBodyAccMag-std()
34	tGravityAccMag-mean()
35	tGravityAccMag-std()
36	tBodyAccJerkMag-mean()
37	tBodyAccJerkMag-std()
38	tBodyGyroMag-mean()
39	tBodyGyroMag-std()
40	tBodyGyroJerkMag-mean()
41	tBodyGyroJerkMag-std()
42	fBodyAcc-mean()-X
43	fBodyAcc-mean()-Y
44	fBodyAcc-mean()-Z
45	fBodyAcc-std()-X
46	fBodyAcc-std()-Y
47	fBodyAcc-std()-Z
48	fBodyAcc-meanFreq()-X
49	fBodyAcc-meanFreq()-Y
50	fBodyAcc-meanFreq()-Z
51	fBodyAccJerk-mean()-X
52	fBodyAccJerk-mean()-Y
53	fBodyAccJerk-mean()-Z
54	fBodyAccJerk-std()-X
55	fBodyAccJerk-std()-Y
56	fBodyAccJerk-std()-Z
57	fBodyAccJerk-meanFreq()-X
58	fBodyAccJerk-meanFreq()-Y
59	fBodyAccJerk-meanFreq()-Z
60	fBodyGyro-mean()-X
61	fBodyGyro-mean()-Y
62	fBodyGyro-mean()-Z
63	fBodyGyro-std()-X
64	fBodyGyro-std()-Y
65	fBodyGyro-std()-Z
66	fBodyGyro-meanFreq()-X
67	fBodyGyro-meanFreq()-Y
68	fBodyGyro-meanFreq()-Z
69	fBodyAccMag-mean()
70	fBodyAccMag-std()
71	fBodyAccMag-meanFreq()
72	fBodyBodyAccJerkMag-mean()
73	fBodyBodyAccJerkMag-std()
74	fBodyBodyAccJerkMag-meanFreq()
75	fBodyBodyGyroMag-mean()
76	fBodyBodyGyroMag-std()
77	fBodyBodyGyroMag-meanFreq()
78	fBodyBodyGyroJerkMag-mean()
79	fBodyBodyGyroJerkMag-std()
80	fBodyBodyGyroJerkMag-meanFreq()
81	activityID
82	activityName

