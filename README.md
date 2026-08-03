# ⚡ Electricity Consumption Prediction Using XGBoost

## 📌 Project Overview

This project predicts electricity consumption using the **XGBoost Regression algorithm**. The model is trained on a smart meter electricity consumption dataset containing information such as temperature, humidity, wind speed, historical electricity consumption, and timestamp-based features.

The project demonstrates how machine learning can be used to analyze electricity usage patterns and predict future electricity consumption based on environmental conditions, previous consumption, and time-related factors.

---

## 🎯 Objective

The main objective of this project is to build a machine learning model that can predict **electricity consumption in kWh** using historical smart meter data and other relevant features.

---

## 📊 Dataset

The project uses the **Smart Meter Electricity Consumption Dataset** obtained from Kaggle.

The dataset contains **5,000 records** collected at 30-minute intervals.

### Dataset Features

| Feature                | Description                                     |
| ---------------------- | ----------------------------------------------- |
| `Timestamp`            | Date and time of the electricity measurement    |
| `Electricity_Consumed` | Electricity consumed in kWh — target variable   |
| `Temperature`          | Temperature recorded at the time of measurement |
| `Humidity`             | Humidity level                                  |
| `Wind_Speed`           | Wind speed                                      |
| `Avg_Past_Consumption` | Average historical electricity consumption      |
| `Anomaly_Label`        | Indicates whether the observation is anomalous  |

The `Anomaly_Label` column is not used for the electricity consumption prediction model.

---

## ⚙️ How the Program Works

The program first loads the smart meter dataset and checks its structure and missing values. The `Timestamp` column is converted into a datetime format, from which additional features such as year, month, day, hour, minute, and day of the week are extracted. The data is then divided chronologically into training and testing sets to preserve the time-series nature of the data. An **XGBoost Regressor** is trained using environmental, historical consumption, and time-based features. The trained model predicts electricity consumption for the test data, and its performance is evaluated using MAE, MSE, RMSE, and R² score. The project also displays actual versus predicted consumption, feature importance, and allows the user to enter new values to obtain an electricity consumption prediction.

---

## 🤖 Machine Learning Algorithm

### XGBoost Regressor

**XGBoost (Extreme Gradient Boosting)** is a gradient boosting machine learning algorithm based on decision trees. It builds multiple decision trees sequentially, where each new tree attempts to correct the errors made by previous trees.

In this project, `XGBRegressor` is used because the target variable, `Electricity_Consumed`, is a continuous numerical value.

---

## 🔧 Features Used for Prediction

The model uses the following features:

* Temperature
* Humidity
* Wind Speed
* Average Past Consumption
* Year
* Month
* Day
* Hour
* Minute
* Day of Week

### Target Variable

```text
Electricity_Consumed
```

---

## 📈 Model Evaluation

The following regression metrics are used to evaluate the model:

### Mean Absolute Error (MAE)

Measures the average absolute difference between actual and predicted consumption.

### Mean Squared Error (MSE)

Measures the average squared difference between actual and predicted values.

### Root Mean Squared Error (RMSE)

Provides the square root of MSE and measures prediction error in the same unit as electricity consumption.

### R² Score

Measures how well the model explains the variation in electricity consumption.

---

## 📊 Visualizations

The project generates the following visualizations:

### 1. Actual vs Predicted Consumption

Compares the actual electricity consumption with the values predicted by the XGBoost model.

### 2. Feature Importance

Displays which features contributed most to the model's predictions.

---

## 🧪 Sample Prediction

The program allows users to enter new values such as:

```text
Temperature: 32.4
Humidity: 72
Wind Speed: 8.5
Average Past Consumption: 3.10
Year: 2024
Month: 8
Day: 10
Hour: 20
Minute: 30
Day of Week: 5
```

The trained XGBoost model then predicts the expected electricity consumption in kWh.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** — data loading and preprocessing
* **NumPy** — numerical operations
* **Scikit-learn** — model evaluation
* **XGBoost** — machine learning model
* **Matplotlib** — data visualization

---

## 📁 Project Structure

```text
Electricity Consumption Prediction/
│
├── smart_meter_data.csv
├── Electricity_prediction.py
├── README.md
├── requirements.txt
└── .gitignore
```

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-github-repository-link>
```

### 2. Open the Project

Open the project folder in **VS Code**.

### 3. Install Dependencies

Run:

```bash
pip install -r requirements.txt
```

### 4. Run the Program

```bash
python Electricity_prediction.py
```

The program will train the XGBoost model, display its performance, generate the charts, and ask for input values for a new electricity consumption prediction.

---

## 📦 Requirements

The required Python libraries are listed in `requirements.txt`.

Install them using:

```bash
pip install -r requirements.txt
```

---

## 🔍 Key Features

* Smart meter electricity consumption prediction
* XGBoost regression model
* Timestamp-based feature engineering
* Chronological train-test split
* Multiple regression evaluation metrics
* Actual vs predicted consumption visualization
* Feature importance analysis
* Interactive user-input prediction
* Simple and beginner-friendly implementation

---

## 🎓 Learning Outcomes

Through this project, I learned how to:

* Work with real-world electricity consumption data
* Perform data preprocessing using Pandas
* Extract useful features from timestamps
* Handle time-series data for machine learning
* Apply the XGBoost regression algorithm
* Evaluate regression models
* Analyze feature importance
* Create data visualizations using Matplotlib
* Make predictions using a trained machine learning model

---

## 👨‍💻 Author

**Danish Solkar**

---

## ⭐ Support

⭐ If you found this project helpful, consider giving it a star!
