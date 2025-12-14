# Project Report

## Introduction
  Coastal fisheries play an important role in food supply and local economies. One of the main challenges in small-scale coastal fishing is predicting when fish schools will approach a specific area. Fishermen often rely on experience and manual observation, which can be inefficient and unreliable.

  With the advancement of Internet of Things (IoT) technologies, hydroacoustic (sonar) sensors and environmental monitoring systems enable continuous and automated data collection in marine environments. These sensors provide valuable information about underwater activity, water conditions, and environmental factors that influence fish behavior.

  In this project, we develop a data-driven approach to predict the short-term approach probability of coastal fish schools using IoT-based sonar data combined with environmental variables such as water temperature, tide level, and wind conditions. The proposed system aims to provide early warnings that support efficient fishing operations, reduce fuel and time costs, and contribute to sustainable fisheries management.

## Data Description
This project uses publicly available marine sensor datasets that simulate or represent coastal hydroacoustic monitoring systems. The primary data source consists of hydroacoustic (sonar) measurements collected from water-column sensors, which capture acoustic backscatter signals indicating underwater activity, including the presence of fish schools.

In addition to sonar data, environmental variables are incorporated to provide contextual information that influences fish movement and behavior. These variables include water temperature, tide level, wind speed, and time-related features such as hour of day. All data sources are time-stamped and aligned to a common temporal resolution.

The datasets are provided in tabular (CSV) format and contain both continuous numerical features and derived indicators. Prior to modeling, the data undergo preprocessing steps including missing value handling, noise filtering, normalization, and temporal aggregation to ensure consistency and reliability for machine learning analysis.

## Methodology
The proposed system follows a standard IoT data science pipeline consisting of data preprocessing, feature engineering, model training, and evaluation. First, raw sonar and environmental sensor data are loaded and synchronized based on their timestamps. Missing values are handled using forward filling or removal depending on their duration, and noise in sonar measurements is reduced using basic filtering techniques.

Feature engineering is performed to extract meaningful information from the raw data. From the sonar signals, statistical features such as average acoustic energy, variance, and temporal trends are derived. Environmental features including water temperature, tide level, wind speed, and time-of-day indicators are also incorporated to provide contextual awareness.

For modeling, the problem is formulated as a binary classification task, where the objective is to predict whether a fish school will approach the monitored coastal area within a short future time window (10–30 minutes). Baseline machine learning models such as Logistic Regression and Random Forest are used to estimate the probability of fish school approach. The dataset is split into training and testing sets while preserving temporal order.

Model performance is evaluated using standard classification metrics, including ROC-AUC, precision, recall, and F1-score. Special emphasis is placed on high-precision predictions to reduce false alarms and provide reliable early warnings.

## Results
The trained models demonstrate the ability to capture patterns in hydroacoustic and environmental data that are associated with the approach of fish schools. The Random Forest model achieves better performance compared to the baseline Logistic Regression model, particularly in terms of ROC-AUC and precision.

The results indicate that combining sonar-derived features with environmental variables improves prediction performance compared to using sonar data alone. High-probability predictions correspond to periods with increased acoustic activity and favorable environmental conditions.

The model outputs are presented as probability scores, which are visualized through an interactive dashboard. This allows users to interpret prediction confidence levels and identify high-risk periods when fish schools are likely to approach the coastal area.

## Conclusion
In this project, an IoT-based data science approach was developed to predict the short-term approach probability of coastal fish schools using hydroacoustic (sonar) sensor data and environmental variables. By integrating sonar measurements with contextual information such as water temperature, tide level, and wind conditions, the system provides a data-driven alternative to traditional experience-based fishing decisions.

The results demonstrate that machine learning models can effectively capture patterns in marine sensor data and generate reliable probability-based early warnings. Such a system has the potential to improve fishing efficiency, reduce operational costs, and support sustainable fisheries management.

Future work may include incorporating higher-resolution sonar data, extending the prediction horizon, and evaluating more advanced deep learning models. Additionally, deploying the system with real-time sensor streams could further enhance its practical applicability in real-world coastal monitoring scenarios.
