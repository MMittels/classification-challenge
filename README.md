# Classification Challenge

## Project Description
   The objective of this project is to improve the email filtering system for customers of an Internet Service Provider. The provided dataset contains information about emails along with a classification of spam and not spam. A supervised machine learning (ML) model was developed utilizing two approaches: Logistic Regression Model and Random Forest Classifier. Accuracy of both were compared to determine the best performance.

## Initial Expectation
   Prior to exploring the data and models I predicted that the Random Forest Classifier would perform better because it is an ensemble approach, which generally improves accuracy and robustness while decreasing variance.

## Data Preparation
   The provided dataset was read into a Pandas DataFrame. A y (predicted column) was defined from the "spam" column in the data and the remaining columns were placed in a DataFrame named X. The data was then split into training and testing datasets by using train_test_split.  Then the features were scaled using StandardScaler fit with the training data.  Both the training and testing features Dataframes were scaled using the transform function.

## Logistic Regression
   The Logistic Regression was set up following create model, fit model, and make predictions.
   - Create Model - The model was created using LogisticRegression()
   - Fit Model - The model was fit using the scaled training data (X_train_scaled and y_train) with random_state set equal to 1.
   - Make Predictions - Predictions were saved by using the testing feature data (X_test_scaled) and the fitted model.
   The accuracy score was .9314 for the Logistic Regression.

## Random Forest Classifier
   The Random Forest Classifier also used create model, fit model and make predictions.
   - Create Model - The model was created using RandomForestClassifer with n_esitmators = 500 and random_state = 1.
   - Fit Model - The model was fit using the scaled training data (X_train_scaled and y_train).
   - Make Predictions - Predictions were saved by using the testing feature data (X_test_scaled) and the fitted model
   The accuracy score was .9557 for the Random Forest Classifier. 

## Comparison of Results
   The Random Forest Classifier performed better, which is in line with my expectations at the beginning of the challenge.