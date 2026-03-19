# "Required Assignment 5.1: Will the Customer Accept the Coupon?"

Anna Niu

The Jupyter Notebook for this assignment can be found [here](https://github.com/annaniu02/MLAI-Assignment-5.1/blob/main/prompt.ipynb).

The dataset used for this assignment can be found [here](https://github.com/annaniu02/MLAI-Assignment-5.1/blob/main/data/coupons.csv).

## Data Cleanup

The following operations were done to handle missing values in the data:

The "car" column was deleted as the majority of values in this column were NaN.

Other columns like "Bar", "CoffeeHouse", "CarryAway", "RestaurantLessThan20", and "Restaurant20To50" that had some missing values had these missing values replaced with the respective column's most common value.

Some structural changes were made to the column names to fix typos, match capitalization/underscore conventions, and help understanding.
- All columns had their first letter capitalized
- Additional changes made:
    - "passanger" changed to "Passenger"
    - "Y" changed to "Coupon_Accepted"
    - "maritalStatus" changed to "Marital_Status"
    - "CoffeeHouse" changed to "Coffee_House"
    - "CarryAway" changed to "Carry_Away"
    - "RestaurantLessThan20" changed to "Restaurant_LessThan20"
    - "Restaurant20To50" changed to "Restaurant_20to50"
    - "toCoupon_GEQ5min" changed to "ToCoupon_GEQ5min"
    - "toCoupon_GEQ15min" changed to "ToCoupon_GEQ15min"
    - "toCoupon_GEQ25min" changed to "ToCoupon_GEQ25min"

## Key Observations

### Key Observations Based on All Data
- 56.84% of total drivers accepted coupons.
- The distribution of acceptance rate across the different coupon categories shows that drivers have a preference for cheap restaurant and take out coupons, as these are the two categories where the acceptance rate is higher than the rejection rate. 
- Bar and more expensive restaurant coupons tend to get rejected more, while coffee house coupons have a close 50/50 split with the rejection rate being slightly higher.
- Warmer weather (80F) results in a higher coupon acceptance rate.
- Younger drivers are more likely to accept coupons.
- Drivers driving around mid-day (10AM-6PM) are more likely to accept coupons than drivers out very early or very late.
- Drivers with no urgent destination are much more likely to accept coupons.
- Drivers with friends as passengers are more likely to accept coupons.

### Key Observations For Bar Coupons
- 41% of bar coupons were accepted.
- Drivers who visit bars more frequently (more than 3 visits/month) accept the bar coupons more than drivers who visit bars less frequently (3 or less visits/month)
- Younger drivers and drivers with friends as passengers are more likely to accept bar coupons.
- Drivers who go to bars more than once a month are more likely to accept bar coupons.
- Drivers who do not have a child passenger are much more likely to accept bar coupons than drivers with a child passenger.

### Key Observations for Carry Out / Take Away Coupons (Individual Exercise)
- 73.55% of take out coupons were accepted.
- Older drivers (50 years and older) are more likely to accept takeout coupons than drivers of other ages.
- Drivers at midday (2PM) are more likely to accept takeout coupons than at other times.
- Drivers with friends as passengers are more likely to accept takeout coupons than solo drivers or drivers with other passengers.
- Drivers are more likely to accept takeout coupons when it's colder out (30F).
- Drivers are more likely to accept takeout coupons when they are driving home or to no urgent destination.
- Drivers who are going home and the coupon venue is in the same direction are much more likely to accept the takeout coupon than reject it.
- Drivers out at 2 PM who are not going anywhere urgent are also much more likely to accept the takeout coupon than reject it.

## Next Steps/Recommendations
- The different coupon types should be tailored to target demographics that have a higher acceptance rate.
- Bar coupons should be sent primarily to people who already frequent bars often, and the younger demographic.
- More coupons for takeout should be sent out around 2 PM and 6 PM, which were found to be the times with the highest acceptance rate.
    - During weekdays at 6 PM, take out coupons whose venues are in the same direction as the driver's destination should be prioritized and sent out in higher volume to target drivers heading home after leaving work.
    - During weekends at 2 PM is another peak time when more take out coupons should be distributed to target drivers out with friends.
- Additional analysis should be done for the other coupon types and features to determine additional target demographics and distribution times.