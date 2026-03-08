# TinyML-Based Intelligent Water Quality Monitoring Node

<p align="center">
<img src="https://c.tenor.com/sukdxuAeg_QAAAAC/water.gif" width="700" height="350">
</p>

## Project Overview

This project presents a lightweight machine learning system designed to monitor water quality and detect unsafe drinking water conditions. The goal is to build a small intelligent monitoring node inspired by TinyML concepts that can analyze environmental sensor data and identify potential contamination.

The system uses a machine learning model trained on water quality indicators such as pH, turbidity, conductivity, and dissolved solids. Based on these inputs, the model predicts whether the water is safe for human consumption. If unsafe conditions are detected, the system can trigger an alert mechanism that could notify relevant monitoring authorities.

The project aligns with **United Nations Sustainable Development Goal 6: Clean Water and Sanitation**, which focuses on ensuring availability and sustainable management of water resources.

---

## Problem Statement

Access to safe drinking water remains a major challenge in many regions around the world. Contaminated water can lead to the spread of diseases such as cholera, typhoid, dysentery, and hepatitis A. Traditional water quality monitoring systems often require expensive infrastructure and manual testing processes, making continuous monitoring difficult in remote or resource-limited areas.

This project explores how machine learning can assist in building an intelligent monitoring system capable of detecting unsafe water conditions automatically using sensor data.

---

## Project Objective

The main objectives of this project are:

- Develop a machine learning model capable of predicting water potability.
- Simulate a lightweight intelligent monitoring node inspired by TinyML concepts.
- Analyze environmental water quality parameters.
- Detect unsafe water conditions automatically.
- Demonstrate a scalable system that could be integrated with real-time monitoring infrastructure.

---

## System Architecture

The proposed system follows a simple pipeline that processes environmental data and produces an alert when contamination is detected.

```
Water Sensor Data
(pH, turbidity, conductivity, solids)

        ↓

Data Preprocessing
Handling missing values and preparing features

        ↓

Machine Learning Model
Random Forest Classifier

        ↓

Water Quality Prediction
Safe / Unsafe classification

        ↓

Detection Logic
Identify contamination events

        ↓

Alert System
Email / Webhook / Monitoring dashboard
```

---

## Dataset

The project uses the **Water Potability Dataset**, which contains water quality metrics for multiple water samples.

Dataset Source  
https://www.kaggle.com/datasets/adityakadiwal/water-potability

The dataset includes **3276 water samples** and several features that describe chemical and physical properties of water.

### Features

| Feature | Description |
|------|------|
| pH | Acidity level of water |
| Hardness | Mineral content present in water |
| Solids | Total dissolved solids |
| Chloramines | Amount of chloramines used for disinfection |
| Sulfate | Sulfate concentration |
| Conductivity | Electrical conductivity of water |
| Organic Carbon | Organic matter present in water |
| Trihalomethanes | Chemical compounds formed during water treatment |
| Turbidity | Clarity of water |
| Potability | Indicates if water is safe (1) or unsafe (0) |

---

## Machine Learning Model

The model used for prediction in this project is the **Random Forest Classifier**.

Random Forest was selected because it performs well on structured datasets and can capture nonlinear relationships between features. It also provides insights into feature importance, which helps identify which water quality parameters influence predictions the most.

The model is trained on historical water quality data and learns to classify whether a water sample is safe for drinking.

---

## Model Pipeline

The workflow followed in the notebook includes the following steps:

```
Dataset Loading
        ↓
Data Cleaning
        ↓
Handling Missing Values
        ↓
Feature Selection
        ↓
Train/Test Split
        ↓
Random Forest Model Training
        ↓
Prediction and Evaluation
```

---

## Model Performance

The trained model achieves an approximate accuracy of:

```
~67% accuracy
```

While the dataset contains several missing values and imbalanced samples, the results demonstrate that lightweight machine learning models can still provide useful predictions for environmental monitoring tasks.

---

## Intelligent Alert System

The project includes a simple simulation of an intelligent monitoring node. When the model detects unsafe water conditions, the system triggers a contamination alert.

Example output:

```
Alert: Contaminated water detected
Notification sent to monitoring authority
```

In a real-world deployment, this alert system could be connected to:

- Email notification services
- Webhook automation platforms
- Environmental monitoring dashboards
- IoT-based water quality sensors

---

## Technologies Used

- Python  
- Google Colab  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  

These tools were used for data preprocessing, model training, visualization, and evaluation.

---

## SDG Impact

This project contributes to **Sustainable Development Goal 6: Clean Water and Sanitation** by demonstrating how machine learning can support water quality monitoring systems.

Intelligent monitoring solutions can help improve access to safe drinking water by enabling faster detection of contamination events and supporting better water management practices.

---

## Future Improvements

Several improvements could enhance this project in future iterations:

- Integration with real-time IoT water quality sensors
- Deployment of the model on edge devices using TinyML frameworks
- Implementation of automated alert systems through email or messaging services
- Development of a live monitoring dashboard for water quality analysis

---

## Author

Aditya Kumar  
IBM GenAI Internship Bootcamp Project
