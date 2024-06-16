# Zindi
Work contains code for AirQo African Air Quality Prediction Challenge on platform Zindi

# PM2.5 Prediction with LightGBM and Optuna

## Project Structure

Zindi/
│
├── data/
│ ├── test.csv
│ ├── train.csv
│
├── result/
│
├── transform/
│ ├── test.csv
│ ├── train.csv
│
├── .gitignore
├── LICENSE
├── models.ipynb
├── README.md
├── see_differences.ipynb
├── transform_train_test.ipynb


## Setup Instructions

1. **Clone the repository:**
    ```bash
    git clone https://github.com/HubertKlosowski/Zindi.git
    cd Zindi
    ```

2. **Folder Structure:**
   - **data/**: Place your `train.csv` and `test.csv` files here.
   - **result/**: The directory where results such as model outputs will be saved.
   - **transform/**: Contains transformed versions of the `train.csv` and `test.csv` after preprocessing.

## Order of Execution

1. **Transform Train and Test Data:**
    - Run `transform_train_test.ipynb` to preprocess and transform the train and test datasets. The transformed files will be saved in the `transform/` directory.

2. **Analyze Differences:**
    - Run `see_differences.ipynb` to analyze and visualize differences between the train and test datasets. This step helps in understanding how different the datasets are.

3. **Model Training:**
    - Run `models.ipynb` to train the LightGBM model using Optuna for hyperparameter tuning. This notebook will load the transformed data, perform training, and save the model and results in the `result/` directory.

## Preprocessing steps taken

- delete columns, that 90% of values are NaNs
- delete top 1% of values from pm2_5 (outliers)
- data standardization

## Post-Preprocessing

multiply the best output with random number
