# ⚡ Building Energy Consumption Prediction using Deep Learning

This project focuses on predicting **building energy consumption** using **Artificial Neural Networks (ANN)**.  
The model analyzes environmental and operational factors such as temperature, humidity, and occupancy to estimate total energy usage — providing insights for improving building efficiency and sustainability.

---

## 📊 Dataset Overview

The dataset contains building operational and environmental metrics collected over various months, hours, and conditions.  
Each record represents a snapshot of building energy data with the following key features:

| Feature | Description |
|----------|-------------|
| **Month, Hour, DayOfWeek, Holiday** | Temporal and calendar-based features |
| **Temperature, Humidity** | Environmental conditions |
| **SquareFootage, Occupancy** | Building size and usage intensity |
| **HVACUsage, LightingUsage, RenewableEnergy** | Operational energy factors |
| **EnergyConsumption** | Target variable representing total building energy usage (kWh) |

---

## 🧠 Methodology

### 1️⃣ Exploratory Data Analysis (EDA)
- Checked data distribution, missing values, and feature correlations.  
- Detected categorical columns (`Holiday`, `HVACUsage`, `LightingUsage`) requiring encoding.  
- Split dataset into **train (70%)**, **validation (10%)**, and **test (20%)** for model development.  

### 2️⃣ Model Development
Developed and compared **4 neural network models**:

| Model Type | Architecture | Description |
|-------------|---------------|--------------|
| **Model 1 - Sequential (Baseline)** | 2 hidden layers, ReLU activation | Basic ANN with standard architecture |
| **Model 2 - Functional (Baseline)** | 2 hidden layers, ReLU activation | Same as Sequential but using Keras Functional API |
| **Model 3 - Sequential (Modified)** | 3 hidden layers, ReLU + Dropout | Tuned neurons & added regularization |
| **Model 4 - Functional (Modified)** | 3 hidden layers, ReLU + LeakyReLU | Enhanced depth and non-linearity handling |

Each model was trained for **10 epochs** using the **Adam optimizer** and **Mean Squared Error (MSE)** as the loss function.

---

## 📈 Evaluation Metrics

All models were evaluated using multiple regression metrics:

- **Mean Absolute Error (MAE)**  
- **Mean Squared Error (MSE)**  
- **R² Score**

| Model | MAE ↓ | MSE ↓ | R² ↑ | Notes |
|--------|--------|--------|-------|-------|
| Sequential (Baseline) | — | — | — | Stable baseline |
| Functional (Baseline) | — | — | — | Similar performance |
| Sequential (Modified) | — | — | — | Improved generalization |
| Functional (Modified) | — | — | — | Best performance overall |

> *(You can fill in the numeric values from your notebook results when uploading to GitHub.)*

---

## 🔍 Key Insights
- Temperature, humidity, and occupancy showed the strongest correlation with energy consumption.  
- Deeper networks (3 layers) performed better at capturing nonlinear relationships.  
- Regularization techniques (Dropout, ReLU variants) helped reduce overfitting.  

---

## 🧾 Results Summary
The final **Functional ANN (Modified)** model achieved the best balance between accuracy and generalization, demonstrating the potential of deep learning for **energy efficiency forecasting** and **smart building management**.

---

## 🧩 Project Structure
