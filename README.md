# Hotel-Cancellation_Prediction_Supervised-Learning_Classification
## Summary
<p align="justify"> A chain of hotels is having issues with booking cancellations leading to loss of revenue. This notebook explores customer booking data to evaluate which factors have a strong influence on booking cancellations. Classification models based on logistic regression and decision trees are developed to predict which bookings will be cancelled in advance. A confusion matrix is constructed to evaluate which performance metric (precision, recall and/or f1 score) needs to be prioritized in the ML prediction model.</p>

<p align="justify">Threshold for the Logistic Regression models are optimized using AUC-ROC curve and the precision-recall curve. Decision Tree models are improved using grid search for hyperparameter tuning and pruning techniques particularly cost-complexity pruning. A final ML model is selected that generalizes well and provides a decent balance between the different performance metrics. Business recommendations are provided based on the insights from EDA and ML solutions that can help formulate profitable policies for cancellations and refunds for the hotel chain.</p>

## Context

A significant number of hotel bookings are called-off due to cancellations or no-shows. The typical reasons for cancellations include change of plans, scheduling conflicts, etc. This is often made easier by the option to do so free of charge or preferably at a low cost which is beneficial to hotel guests but it is a less desirable and possibly revenue-diminishing factor for hotels to deal with. Such losses are particularly high on last-minute cancellations. 

The new technologies involving online booking channels have dramatically changed customers’ booking possibilities and behavior. This adds a further dimension to the challenge of how hotels handle cancellations, which are no longer limited to traditional booking and guest characteristics. 

The cancellation of bookings impact a hotel on various fronts:
* Loss of resources (revenue) when the hotel cannot resell the room.
* Additional costs of distribution channels by increasing commissions or paying for publicity to help sell these rooms.
* Lowering prices last minute, so the hotel can resell a room, resulting in reducing the profit margin.
* Human resources to make arrangements for the guests.

## Objective
A Hotel group that has a chain of hotels in Portugal, are facing problems with a high number of booking cancellations. The goal of this project is to analyze customer booking data to identify which factors have a high influence on booking cancellations, build a predictive model that can predict which booking is going to be canceled in advance, and help to formulating profitable policies for cancellations and refunds.

## Data Description
The data contains the different attributes of customers' booking details. The detailed data dictionary is given below.


**Data Dictionary**

* Booking_ID: unique identifier of each booking
* no_of_adults: Number of adults
* no_of_children: Number of Children
* no_of_weekend_nights: Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel
* no_of_week_nights: Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel
* type_of_meal_plan: Type of meal plan booked by the customer:
    * Not Selected – No meal plan selected
    * Meal Plan 1 – Breakfast
    * Meal Plan 2 – Half board (breakfast and one other meal)
    * Meal Plan 3 – Full board (breakfast, lunch, and dinner)
* required_car_parking_space: Does the customer require a car parking space? (0 - No, 1- Yes)
* room_type_reserved: Type of room reserved by the customer. The values are ciphered (encoded) by INN Hotels.
* lead_time: Number of days between the date of booking and the arrival date
* arrival_year: Year of arrival date
* arrival_month: Month of arrival date
* arrival_date: Date of the month
* market_segment_type: Market segment designation.
* repeated_guest: Is the customer a repeated guest? (0 - No, 1- Yes)
* no_of_previous_cancellations: Number of previous bookings that were canceled by the customer prior to the current booking
* no_of_previous_bookings_not_canceled: Number of previous bookings not canceled by the customer prior to the current booking
* avg_price_per_room: Average price per day of the reservation; prices of the rooms are dynamic. (in euros)
* no_of_special_requests: Total number of special requests made by the customer (e.g. high floor, view from the room, etc)
* booking_status: Flag indicating if the booking was canceled or not.
