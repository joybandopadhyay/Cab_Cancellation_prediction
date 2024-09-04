# Cab_Cancellation_prediction
•id - booking ID
•user_id - the ID of the customer (based on mobile number)
•vehicle_model_id - vehicle model type.
•package_id - type of package (1=4hrs & 40kms, 2=8hrs & 80kms, 3=6hrs & 60kms, 4= 10hrs & 100kms, 5=5hrs & 50kms, 6=3hrs
& 30kms, 7=12hrs & 120kms)
•travel_type_id - type of travel (1=long distance, 2= point to point, 3= hourly rental).
•from_area_id - unique identifier of area. Applicable only for point-to-point travel and packages
•to_area_id - unique identifier of area. Applicable only for point-to-point travel
•from_city_id - unique identifier of city
•to_city_id - unique identifier of city (only for intercity)
•from_date - time stamp of requested trip start
•to_date - time stamp of trip end
•online_booking - if booking was done on desktop website
•mobile_site_booking - if booking was done on mobile website
•booking_created - time stamp of booking
•from_lat - latitude of from area
•from_long - longitude of from area
•to_lat - latitude of to area
•to_long - longitude of to area
•Car_Cancellation - whether the booking was cancelled (1) or not (0) due to unavailability of a car.
There are three types of travel type ids viz., 1, 2, and 3. Models like Logistic Regression, SVC, Gaussian Naive Baye Classifier, Random Forest Classifier, XGBoost Classifier have been used here. 
For travel type id = 1, the number of majority class 0 instances is 1568 and the number of minority class 1 instances is just 21, its a highly imbalanced dataset. The best result in terms of average_precision_score has been obtained through XGBoost Classifier, while through GridSearchCV, precision for the minority class improves as well as the F1 score with some drop in the average precision score.
For travel type id = 2, the number of majority class 0 instances is 31517 and the number of minority class 1 instances is just 2775, its a highly imbalanced dataset. The best result in terms of average_precision_score has been obtained through XGBoost Classifier, while through GridSearchCV there is negligible drop in the average precision score.
For travel type id = 3, the number of majority class 0 instances is 7214 and the number of minority class 1 instances is just 336, its a highly imbalanced dataset. In terms of accuracy Logistic Regression model gave the best answer compared to other models.
