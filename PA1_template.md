# Reproducible Research: Peer Assessment 1

## Loading and preprocessing the data


## What is mean total number of steps taken per day?
1. Make a histogram of the total number of steps taken each day.
![](./PA1_template_files/figure-html/unnamed-chunk-2-1.png) 
2. Calculate and report the mean and median total number of steps taken per day.
![](./PA1_template_files/figure-html/unnamed-chunk-3-1.png) 

## What is the average daily activity pattern?
1. Make a time series plot (i.e. type = "s") of the 5-minute interval (x-axis) and the average number of steps taken, averaged across all days (y-axis)
![](./PA1_template_files/figure-html/unnamed-chunk-4-1.png) 
2. Which 5-minute interval, on average across all the days in the dataset, contains the maximum number of steps?

The max number of steps per 5 minute interval\, averaged across all of the days in the dataset\,
is 206.17 steps at 08:35.

## Imputing missing values
1. Calculate and report the total number of missing values in the dataset (i.e. the total number of rows with NAs)

There are 2304 missing values in the dataset.

2. Devise a strategy for filling in all of the missing values in the dataset. The strategy does not need to be sophisticated. For example, you could use the mean/median for that day, or the mean for that 5-minute interval, etc.

Missing values will be filled in with the mean steps for the 5-minute interval and type of day of the week\, i.e. weekday\, weekend.

* First a new factor variable will be created in the dataset with two levels - "weekday" and "weekend".
* Then the mean steps for the interval and day type will be calculated.
* These values will be used to replace the NA values in the new dataset.

3. Create a new dataset that is equal to the original dataset but with the missing data filled in.


4. Make a histogram of the total number of steps taken each day and Calculate and report the mean and median total number of steps taken per day. Do these values differ from the estimates from the first part of the assignment? What is the impact of imputing missing data on the estimates of the total daily number of steps?

![](./PA1_template_files/figure-html/unnamed-chunk-8-1.png) ![](./PA1_template_files/figure-html/unnamed-chunk-8-2.png) 

The shape of the histagram has not changed.  The only difference is more data points.

The average number of steps per day has not changed, other then missing values are now filled in.

The median number of steps is now much larger for days that were missing steps.  This is because the average values used are genearlly greater than the median.  A better way to impute the missing values would have been to take a random sample of the non-na values for the same interval and day type.

## Are there differences in activity patterns between weekdays and weekends?
![](./PA1_template_files/figure-html/unnamed-chunk-9-1.png) 

The activity patterns between weekdays and weekends are different.
