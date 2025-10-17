# 🧠 Building a Deep Learning Model for Office Energy Consumption Prediction

This project focuses on developing a **Deep Learning regression model** using **Artificial Neural Networks (ANNs)** to predict **office building energy consumption** based on environmental and operational factors such as temperature, humidity, occupancy, and renewable energy use.  
The goal is to leverage neural networks to improve energy efficiency insights and support sustainable facility management.

---

## 📘 Overview

Efficient energy management is crucial for reducing operational costs and promoting sustainability.  
This project explores multiple ANN architectures using both **Sequential** and **Functional API** approaches in TensorFlow/Keras.  
By comparing baseline and optimized models, the study identifies the most effective network configuration for energy consumption prediction.

---

## 📊 Dataset Overview

| Feature | Description |
|----------|-------------|
| **Month, Hour, DayOfWeek, Holiday** | Temporal and categorical indicators |
| **Temperature, Humidity** | Environmental conditions |
| **SquareFootage, Occupancy** | Building and operational factors |
| **HVACUsage, LightingUsage, RenewableEnergy** | Energy-related operational features |
| **EnergyConsumption** | Target variable (kWh) |

The dataset was split into **Train (70%)**, **Validation (10%)**, and **Test (20%)** to ensure robust model evaluation.

---

## ⚙️ Methodology

### 1. Data Preprocessing
- Performed exploratory data analysis (EDA) to identify missing values and data inconsistencies.  
- Encoded categorical features (e.g., *HVACUsage*, *LightingUsage*, *Holiday*) and scaled numerical values using **StandardScaler**.  
- Split data into training, validation, and test sets with a **70:10:20** ratio.

### 2. Model Development
Developed and compared four ANN models:
- **Baseline Sequential Model**  
- **Baseline Functional Model**  
- **Modified Sequential Model** (Leaky ReLU, Batch Normalization, Dropout)  
- **Modified Functional Model** (enhanced architecture with activation tuning)

### 3. Training
- All models trained for a minimum of **10 epochs** using the **Adam optimizer**.  
- Implemented **early stopping** and **learning rate tuning** for model stability.

---

## 📈 Model Evaluation

Models were evaluated using three key regression metrics:

| Model | MSE | MAE | R² | Summary |
|--------|------|------|------|----------|
| **Baseline Sequential** | 61.86 | 6.25 | 0.175 | High error, limited variance explanation |
| **Baseline Functional** | 62.45 | 6.27 | 0.168 | Similar to baseline Sequential |
| **Modified Sequential** | 57.57 | 5.99 | 0.233 | Best performance, reduced error and improved fit |
| **Modified Functional** | 57.59 | 5.96 | 0.232 | Comparable to Modified Sequential |

### 🔍 Insights
- Incorporating **Leaky ReLU**, **Batch Normalization**, and **Dropout** layers improved model performance significantly.  
- The **Modified Sequential Model** achieved the **lowest MSE (57.57)** and **highest R² (0.233)**, making it the best-performing model.

---

## 🧾 Conclusion
- Deep learning models effectively captured non-linear relationships between environmental and operational features in energy usage.  
- The optimized ANN architecture enhanced prediction accuracy and reduced overfitting.  
- This experiment demonstrates how ANN-based regression can be a powerful tool for **smart building energy management**.
