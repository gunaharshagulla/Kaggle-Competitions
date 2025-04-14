# Car Price Prediction Model

This repository contains a machine learning model for predicting car prices based on various features such as the car's company, city, distance covered, and fuel type. The model has been implemented using TensorFlow and trained on a dataset provided in the repository.

## Dataset

The dataset used to train this model is available in the `train.csv` file. It contains information about car features, including the model year, distance covered, fuel type, and other relevant attributes.

## Usage

To use the car price prediction model, follow the steps below:

1. Clone this repository to your local machine:
   git clone https://github.com/gunaharshagulla/Car-Price-Prediction/
   
2. Ensure that you have downloaded the `train.csv` file and placed it in the project directory.

3. Open the Jupyter notebook or Python script that contains the model code.

4. Execute the code blocks to load the dataset, preprocess the data, and train the car price prediction model.

5. Once the model is trained, you can use it to make predictions on new car data. Modify the code accordingly, providing the necessary input features such as the car's company, city, distance covered, and fuel type.

6. Run the prediction code to obtain the predicted car price.

## Functionality of the Model

1. The code starts by importing the necessary libraries and dependencies, such as TensorFlow, pandas, scikit-learn, and matplotlib.

2. The dataset is loaded using `pd.read_csv()` function from the `train.csv` file. The dataset contains information about car features, and it is stored in the `raw_data` DataFrame.

3. The `training_data` DataFrame is created by dropping the 'price' column from the `raw_data`, while the `training_labels` DataFrame contains only the 'price' column.

4. Next, the code performs data preprocessing steps on the `training_data` DataFrame. It uses one-hot encoding with `pd.get_dummies()` to convert categorical features into binary columns. The 'pre_owner_4th Owner' and 'car ID' columns are dropped to remove unnecessary features.

5. The data is split into training and validation sets using `train_test_split()` function from scikit-learn. It assigns 90% of the data to the training set (`train_data` and `train_labels`) and 10% to the validation set (`validation_data` and `validation_labels`).

6. The code applies feature normalization using `MinMaxScaler()` from scikit-learn on the 'model_year' and 'distance_covered (km)' columns of the training and validation sets. This ensures that all features are scaled to a similar range and prevents any single feature from dominating the model.

7. Additional data preprocessing is done by dropping the 'model_year' and 'distance_covered (km)' columns from `train_data` and `validation_data`.

8. The TensorFlow model is defined using the `Sequential` API. It consists of several dense layers with varying numbers of neurons and activation functions. Dropout layers are also added to prevent overfitting.

9. The model is compiled with the Mean Squared Logarithmic Error loss function and the Adam optimizer with a learning rate of 0.0001.

10. The model is trained using the `fit()` method on the training data. The `batch_size`, `steps_per_epoch`, and `epochs` parameters determine the training process.

11. After training, the model is evaluated on the validation data using the `evaluate()` method. The evaluation provides a measure of the model's performance.

12. The README file provides instructions on how to use the model, including cloning the repository, installing dependencies, and running the code to make predictions on new car data.

Feel free to modify or customize the logic and code based on your specific needs and requirements.
