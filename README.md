# Linear_Regression_Taxi_Driver_Fare


  1. Project Overview:-
     - This project implements a Linear Regression model using TensorFlow/Keras to predict the taxi fare (FARE) for Chicago             taxi trips.
     - The model uses simple, highly correlated features like trip distance and duration to estimate the cost of a ride.
    
  2. Goal:-
     The primary objective is to build and train a linear regression model that can accurately predict the FARE of a taxi           trip based on the available trip features.

  3. Dataset:-
     The model is trained on a subset of the Chicago Taxi Trip Data.
      - Source: https://download.mlcc.google.com/mledu-datasets/chicago_taxi_train.csv
      - Target Variable (Label): FARE
      - Key Features Used: TRIP_MILES (distance traveled) and TRIP_SECONDS (trip duration)

  4. Data Exploration and Key Findings:- 
     - Initial data analysis was performed on a processed dataframe (train_df), revealing the following:
       - Maximum Fare: $159.25
       - Mean Distance: 8.2895 miles
       - Cab Companies: The dataset contains 31 unique cab companies
       - Most Frequent Payment Type: Credit Card
       - Data Quality: The final train_df used for modeling had no missing values.

     - The scatter matrix visualization confirmed strong relationships (high correlation) between the target variable (FARE)          and the selected input features (TRIP_MILES and TRIP_SECONDS).
    

  5. Model Training and Results:-
     
     (i) Model:
        - A simple Linear Regression model was implemented using the TensorFlow/Keras framework, configured for a regression            task.
        - Training Time: 20 epochs.
        - Loss Metric: Mean Squared Error (MSE) (implied by the training output showing loss and rmse).
        - Evaluation Metric: Root Mean Square Error (RMSE).
    
      (ii) Performance:
         - The model training successfully reduced the prediction error.
          Metric                                 Final
          ValueRoot Mean Square Error (RMSE)   ~3.61 (at epoch 20)

   6. Conclusion
       Based on a random sample of predictions, the model is described as performing "pretty well" at predicting the taxi            fare, with predicted values not varying significantly from the observed values, as indicated by the low L1_LOSS               (absolute difference) for most examples.


   7. Prerequisites
       To run the notebook, you need a Python environment with the following libraries installed:

         Bash

         pip install google-ml-edu==0.1.3 \
           keras~=3.8.0 \
           matplotlib~=3.10.0 \
           numpy~=2.0.0 \
           pandas~=2.2.0 \
           tensorflow~=2.18.0 \
           plotly


   8. Usage
    (i) Clone the Repository (Hypothetical):

         Bash

         git clone ["https://download.mlcc.google.com/mledu-datasets/chicago_taxi_train.csv"]
         cd linear_regression_taxi_driver_fare
        
   (ii) Open the Notebook: Open the LinearRegression_Taxi_.ipynb file in a Jupyter environment (such as Google Colab or                Jupyter Notebook/Lab).

  (iii) Run Cells: Execute all cells in sequential order to:
      - Install dependencies.
      - Load and explore the data.
      - Train the linear regression model.
      - View the final model evaluation and sample predictions.


     
