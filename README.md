# Investigate Hotel Business using Data Visualization
It is very important for a company to always analyze its business performance. On this occasion, we will go deeper into the business in the hospitality sector. The focus we are aiming for is to find out how our customers behave in making hotel bookings, and their relationship to the level of cancellation of hotel bookings. The results of the insights we find will be presented in the form of visualization data to make it easier to understand and more persuasive.

## Dataset
---
Download dataset [here](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand)

## Preprocessing
---
### Handling Missing Value
There are 4 columns that have Null/NaN values, namely `children`, `city`, `agent`, and `company`. The column is filled based on the description of each column.
1. The `children` column is filled with 0 which indicates that you are not bringing children.
2. The `city` column is filled with unknown which indicates that it is not defined.
3. The `agent` column is filled with 0 which indicates that the hotel reservation was not made through an agent.
4. The `company` column is filled with 0 which indicates that the hotel booking is not from the company.

There is an inappropriate value in the `meal` column, namely 'Undefined', so replace that value with 'No meal'.

### Handling Duplicated Data
There are 33,261 duplicate data which will be dropped later.

### Handling Invalid Values
Data deletion is performed based on the following conditions:
1. Rows where `adr` (average daily rate) is negative.
2. Rows with a cumulative sum of `adults` + `children` + `babies` = 0.
3. Rows with a `adults` = 0.
4. Rows with a cumulative sum between `stay_in_weekend_nights` + `stay_in_weekday_nights` = 0.


## Monthly Hotel Booking Analysis Based on Hotel Type
---
![Google Drive Image](https://drive.google.com/uc?export=view&id=1GPiC7gb2Eld3lxgryVKoNUvZKrWYgLfm)
Both types of hotels experience fluctuations in bookings every month. In the middle of the year, June and July, total bookings have increased. Likewise at the end of the year, November and December, experienced an increase, although not as high as in mid-year. This is due to the holiday season such as school holidays, commemorations of holidays, and New Year.

## Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates
---
![Google Drive Image](https://drive.google.com/uc?export=view&id=1PD16zw28XcxrzqYEk_S2WzmZJLRde-pa)
The largest percentage of canceled bookings for City Hotel was for stays of more than 4 weeks or 1 month. This situation is different from Resort Hotel, where the largest percentage of canceled bookings is for a stay duration of 3-4 weeks.

## Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate
---
![Google Drive Image](https://drive.google.com/uc?export=view&id=1ZDmchirH5aU2NQWtlHA0sptpa4iZOaWs)
The largest percentage of canceled bookings for City Hotel at intervals of more than 2 months. This situation is the same as for Resort Hotel, where the largest percentage of canceled bookings is at a time interval of more than 2 months as well.