Approach to building merged dataset

1. Bind the columns of 'subject', 'y' and 'x' datasets for each of 'test' and 'train'

2. Bind the rows of each of the above resulting datasets

3. Get the vector in the 'features' file. Add two elements to the front of this vector called 'subject' and 'activity'

4. Row bind the ammended features dataset to the above combined 'test' and 'train' dataset

5. Create a join on the 'activity' (2nd) column with the a table containing the descriptive activity labels

6. Create a dataset that only includes rows that contain 'subject', 'activity' or features of the combined dataset that are mean or standard deviation values

7. Print this dataset to a text file

8. Use the above dataset to create a second dataset that is grouped by 'subject' and 'activity' and then contains an avg of each of the other columns







# read the subject for each test experiment into 'testsubject'

testsubject <- read.table('D:/Users/philcarmine/Downloads/getdata%2Fprojectfiles%2FUCI HAR Dataset/UCI HAR Dataset/test/subject_test.txt')

# read the feature values for each test experiment into the 'xtest' variable 

xtest <- read.table('D:/Users/philcarmine/Downloads/getdata%2Fprojectfiles%2FUCI HAR Dataset/UCI HAR Dataset/test/X_test.txt')

# Read the activity for each test experiment into the 'ytest' object 

ytest <- read.table('D:/Users/philcarmine/Downloads/getdata%2Fprojectfiles%2FUCI HAR Dataset/UCI HAR Dataset/test/y_test.txt')

# combine the subject, activity and feature values for each test experiment into a single dataframe

d1 <- cbind(testsubject, ytest)
test <- cbind(d1, xtest)

# read the subject for each training experiment into 'trainsubject'

trainsubject <- read.table('D:/Users/philcarmine/Downloads/getdata%2Fprojectfiles%2FUCI HAR Dataset/UCI HAR Dataset/train/subject_train.txt')

# read the feature values for each training experiment into the 'xtrain' variable 

xtrain <- read.table('D:/Users/philcarmine/Downloads/getdata%2Fprojectfiles%2FUCI HAR Dataset/UCI HAR Dataset/train/X_train.txt')

# Read the activity for each training experiment into the 'ytrain' object 

ytrain <- read.table('D:/Users/philcarmine/Downloads/getdata%2Fprojectfiles%2FUCI HAR Dataset/UCI HAR Dataset/train/y_train.txt')

# combine the subject, activity and feature values for each training experiment into a single dataframe

d1 <- cbind(trainsubject, ytrain)
train <- cbind(d1, xtrain)

# combine the training and test datasets into a single dataset

combineddataset <- rbind(test, train)

# read the features labels of the test and training datasets into a vector object

d1 <- read.table('D:/Users/philcarmine/Downloads/getdata%2Fprojectfiles%2FUCI HAR Dataset/UCI HAR Dataset/features.txt')
features <- t(d1[2])

# create a vector object with the column names for 'combineddataset' table and update 'combineddataset to contain these labels

col <- c('subject', 'activity')
header <- c(col, features)
header <- make.names(header, unique=TRUE)
colnames(combineddataset) <- header

# read the activity labels into a table called 'activities'

activities <- read.table('D:/Users/philcarmine/Downloads/getdata%2Fprojectfiles%2FUCI HAR Dataset/UCI HAR Dataset/activity_labels.txt')
colnames(activities) <- c('activity', 'activity_desc')

# install/load the dplyr package and join the activities labels to each of the experiments

install.packages('dplyr')
library(dplyr)
dataset <- left_join(combineddataset, activities)

# use a dplyr select statement to get a dataset with the subject, activity description and the mean and standard dev features only

dataset <- select(dataset, subject, activity_desc, contains("mean"), contains("std"))

# write the first tidy dataset to to a text file

write.table(dataset, file = 'D:/Users/philcarmine/Coursera/Cleaning Data/Dataset1.txt')

# create a new dataset from the first tidy dataset to show a mean of each mean and standard dev feature for each activity and subject

dataset2 <- dataset %>% group_by(activity_desc, subject) %>% summarise_all(funs(mean))

# write the second tidy dataset to a text file

write.table(dataset2, file = 'D:/Users/philcarmine/Coursera/Cleaning Data/Dataset2.txt')
