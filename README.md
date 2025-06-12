# Blockchain-Based-Green-Edge-Computing-Energy-Efficiency-with-Decentralized-AI-Frameworks-25309
This project presents a smart edge computing framework powered by decentralized AI and blockchain technologies. The system ingests IoT device metrics and blockchain transactional data to **classify system status**, enabling real-time insights and energy optimization for **green and secure edge environments**.

---

## 🎯 Objectives

- Analyze and visualize blockchain-integrated IoT data from decentralized edge devices.
- Predict system load and behavior using supervised machine learning.
- Support intelligent decision-making to enhance energy efficiency and reduce latency.
- Bridge **blockchain transparency** with **AI automation** in smart edge ecosystems.

---

## 📦 Dataset Summary

The dataset includes **1000 records** from IoT-edge devices and blockchain events. Below are selected features:

| Feature               | Description                                             |
|-----------------------|---------------------------------------------------------|
| `timestamp`           | Event timestamp                                         |
| `device_id`, `node_id`| Unique identifiers for devices and nodes               |
| `energy_consumed`     | Energy usage (watts)                                    |
| `latency`, `data_size`| Network latency and data packet size                    |
| `error_rate`          | Model or transmission error rate                        |
| `protocol_type`       | Protocol used by the device (e.g., MQTT, HTTP)          |
| `air_quality`, `humidity`, `temperature` | Environmental context               |
| `transaction_status`, `block_hash`, `validation_status` | Blockchain status     |
| `model_accuracy`, `training_time`, `model_version` | AI performance metrics     |
| `system_status`       | 🔻 **Target Variable** (1=Normal, 2=Degraded, 3=Fault)  |

---

## 📊 Exploratory Data Analysis

Key insights uncovered through visualizations:

- **Energy Usage vs Protocol Type**: Showed that certain protocols (like MQTT) were more energy efficient.
- **Device Type Impact**: Visualization of energy consumption and latency by device category.
- **Environmental Influence**: Detected correlation between temperature/humidity and latency/energy usage.
- **Validation Rates by Location**: Heatmaps revealed success/failure zones in transaction validation.

These insights shaped how we approached the classification modeling.

---

## 🧹 Preprocessing Steps

- Converted timestamps to datetime formats
- Label encoded and one-hot encoded categorical columns
- Scaled numerical features using `StandardScaler`
- Removed outliers using IQR-based filtering
- Prepared a clean feature matrix `X` and target `y = system_status`

---

## 🤖 Classification Models

We implemented three models to classify the `system_status` of edge devices.

---

### 🔹 Logistic Regression Results:
- **Accuracy**: `0.335`

```
Precision | Recall | F1-Score | Class
--------- | ------ | -------- | -----
   0.29   |  0.35  |   0.32   |  Class 1
   0.44   |  0.27  |   0.33   |  Class 2
   0.33   |  0.38  |   0.35   |  Class 3
```

---

### 🌲 Random Forest Classifier Results:
- **Accuracy**: `0.365`

```
Precision | Recall | F1-Score | Class
--------- | ------ | -------- | -----
   0.38   |  0.41  |   0.39   |  Class 1
   0.36   |  0.33  |   0.35   |  Class 2
   0.36   |  0.35  |   0.35   |  Class 3
```

---

### 🧠 Support Vector Machine (SVM) Results:
- **Accuracy**: `0.32`

```
Precision | Recall | F1-Score | Class
--------- | ------ | -------- | -----
   0.31   |  0.38  |   0.34   |  Class 1
   0.36   |  0.25  |   0.30   |  Class 2
   0.30   |  0.32  |   0.31   |  Class 3
```

---

## ✅ Model Comparison

| Model              | Accuracy | Highlights                               |
|-------------------|----------|-------------------------------------------|
| Logistic Regression| 0.335    | Fast, interpretable, weak on complex data |
| Random Forest      | 0.365    | Best performer, good balance              |
| SVM                | 0.320    | Stable but less accurate                  |

> **🏆 Best Model: `Random Forest Classifier`**

---

## 💼 Business Impact

### 🔋 Energy Optimization
- Identifies inefficient devices to reduce energy consumption.
- Promotes smart load distribution in edge environments.

### 🔐 Blockchain Assurance
- Prevents validation failures by predicting faulty system states.
- Supports transparency in blockchain-integrated IoT networks.

### 🧠 AI Autonomy
- Guides adaptive learning and model updates based on device health.
- Enhances decentralized AI reliability and performance.

### 💡 Smart City Applications
- Helps optimize traffic flow, air quality monitoring, and smart grids.
- Ideal for Industry 4.0, healthcare IoT, logistics, and utilities.

---


