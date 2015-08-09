# Reproducible Research: Peer Assessment 1
Jim Pfleger  


## Loading and preprocessing the data

### Retrieve and unzip data file


```r
datafile <- 'activity.csv'
if (!file.exists(datafile)) {
  zip <- 'activity.zip'
  if (!file.exists(zip)) {
    download.file('https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2Factivity.zip', zip, method = 'libcurl')
  }
  unzip(zip)
}
```

### Tidy data


```r
library(lubridate)
steps <- read.csv(datafile)
steps$date <- ymd(steps$date)
steps$interval <- factor(steps$interval)
```


## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
