# Tidy Data from the Human Activity Recognition Using Smartphones Dataset

A few steps were taken to transform the initial data set:
  1. Merges the training and the test sets to create one data set.
  2. Extracts only the measurements on the mean and standard deviation for each measurement.
  3. Uses descriptive activity names to name the activities in the data set.
  4. Appropriately labels the data set with descriptive variable names.
  5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

There is a single row for each subject/activity pair, and a single column for each measurement.

The final data set can be found in the `tidyData.txt` file, which can be read into R with `read.table("tidyData.txt", header = TRUE)`. 

A detailed description of the variables can be found in `CodeBook.md`. The basic naming convention is:

  {MeanOrSD}{TimeOrFreq}{Measurement}{XYZ}

where
- `MeanOrStd` is either Mean or Standard Deviation, indicating whether the measurement was a mean or standard deviation variable.
- `TimeOrFreq` is either Time or Frequency, indicating whether the measurement is either the the time or frequency domain.
- `Measurement` is one of the original measurement features. 
- `XYZ` is X, Y, or Z, indicating the axis along which the measurement was taken, or nothing, for magnitude measurements.