# Basetech_capstone_project_1

SwiftDrop System Audit

1. ML Problem

Predicting delivery time is a Regression problem because the output is a continuous numerical value (delivery time in minutes).

Objective: Minimize the difference between predicted and actual delivery time using MAE (Mean Absolute Error).

Ground Truth: The actual delivery time recorded when the package is delivered.

2. Feature Mapping
   
Feature	                      Type

Delivery distance	           Numerical
Traffic level	               Categorical
Weather condition	           Categorical
Time of day	                 Categorical
Day of week	                 Categorical
Number of items	             Numerical
Pickup waiting time	         Numerical
Delivery partner experience  Numerical
Road congestion score	       Numerical
Vehicle type                 Categorical


3. Real-World Noise

Unexpected road construction or roadblocks, missing traffic information, incorrect timestamps, heavy rain, and delayed order-status updates, 
can increase the actual delivery time even when the recorded distance and traffic conditions look normal. 
If this is not captured in the training data, the model may underestimate delivery time and give inaccurate predictions.

4. MLflow Tracking Rules

The engineering team should stop using confusing notebook names such as delivery_model_final_v3_really_final.ipynb. 
Every ML experiment should be tracked using MLflow with a unique experiment/run ID.

For every experiment, the team must record the model type, learning rate, batch size, number of epochs, training/validation split, and other relevant hyperparameters.
The team must also track training loss, validation loss, MAE, and RMSE. The dataset version, model version, experiment ID, and final model artifact should also be recorded so that every result can be reproduced.
