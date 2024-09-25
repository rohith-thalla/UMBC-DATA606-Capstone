# 1. Title and Author
**Project Title**: Human Activity Recognition Using Sensor Data for Fitness Tracking  
**Prepared for**: UMBC Data Science Master Degree Capstone by Dr. Chaojie (Jay) Wang  
**Author Name**: Om Sri Rohith Raj Yadav Thalla  

- **GitHub Repository**: [GitHub Repo](https://github.com/rohith-thalla/UMBC-DATA606-Capstone)  
- **LinkedIn Profile**: [LinkedIn Profile](https://www.linkedin.com/in/rohithrajthalla/)  
- **PowerPoint Presentation**: [PowerPoint Presentation](#)  
- **YouTube Video**: [YouTube Video](#)  



# 2. Background

## Fitness Tracking Industry Boom:
- The global fitness tracker market was valued at $36.34 billion in 2020 and is expected to grow at a CAGR of 15.4% from 2021 to 2028.
- There has been increasing awareness of health and fitness globally, with a significant rise in wearable devices like smartwatches, fitness bands, etc.
- These devices offer features such as heart rate monitoring, step counting, and calorie tracking, helping users stay on top of their health.

## Why Fitness Tracking is Important:
- Fitness trackers provide real-time data on calories burned, activity levels, and more.
- They store a log of health data that can be used by individuals and health professionals to monitor progress over time.
- Fitness tracking can help in goal-setting and making lifestyle improvements, leading to better health outcomes.

## What is it About?
- This project focuses on recognizing human activities (e.g., walking, running, sitting) using sensor data from fitness tracking devices, benefiting the fitness and wellness industry.

## Why Does it Matter?
- Tracking activities allows users to get personalized fitness recommendations.
- Maintaining a log of activities helps build a health profile and can extend to features like game improvements and fitness challenges.
- It enables better calorie tracking and overall well-being monitoring.

## Research Questions:
1. Can we accurately classify sports or activities using sensor data inputs from accelerometers, gyroscopes, and magnetometers?
2. What sensors provide the most predictive power in distinguishing between different activities?



# 3. Data

## Data Sources:
- **Source**: The dataset is sourced from the UCI Machine Learning Repository, titled **Daily and Sports Activities Dataset**.
- **Purpose**: This dataset contains sensor data collected from body-worn units (accelerometers, gyroscopes) while performing various activities.

## Data Size:
- The dataset is approximately **150 MB** in size.

## Data Shape:
- The dataset contains **1.14 million rows** and **46 columns**.

## Time Period:
- The data was collected during sessions where subjects performed activities for 5-minute intervals per activity.

## What Does Each Row Represent?:
- Each row represents a **5-second segment** of sensor data collected from accelerometers, gyroscopes, and magnetometers during a specific activity (e.g., walking, running).

## Data Dictionary:
### Columns:
- `T_xacc`, `T_yacc`, `T_zacc`: Accelerometer readings for the torso (x, y, z axes).
- `RA_xacc`, `RA_yacc`, `RA_zacc`: Accelerometer readings for the right arm (x, y, z axes).
- `LA_xacc`, `LA_yacc`, `LA_zacc`: Accelerometer readings for the left arm (x, y, z axes).
- `RL_xacc`, `RL_yacc`, `RL_zacc`: Accelerometer readings for the right leg (x, y, z axes).
- `LL_xacc`, `LL_yacc`, `LL_zacc`: Accelerometer readings for the left leg (x, y, z axes).
- Similar readings for gyroscopes and magnetometers for all body parts.

### Data Types:
- **Numerical**: All sensor data is in numerical format (floats), representing the accelerometer, gyroscope, and magnetometer readings.
- **Categorical**: The target activity (e.g., sitting, running, jumping, etc.).

### Definitions:
- **Accelerometer**: Measures acceleration forces in the x, y, z axes, used to capture body movement.
- **Gyroscope**: Measures angular velocity in the x, y, z axes, used to detect orientation and rotation.
- **Magnetometer**: Measures magnetic fields in the x, y, z axes, used to detect orientation in conjunction with accelerometers and gyroscopes.

## Potential Values (for Categorical Variables):
- **Activity Labels**:
  - Sitting
  - Standing
  - Walking
  - Running
  - Jumping
  - Lying down (on back or side)
  - Ascending stairs
  - Descending stairs
  - Playing basketball
  - Exercising on a stepper or cross-trainer
  - Other activities like rowing, cycling, treadmill use

## Target/Label in ML Model:
- The target/label column for the ML model is the **activity** column, indicating the specific activity being performed (e.g., sitting, walking, running).

## Features/Predictors for ML Model:
- The features/predictors for the model will be the sensor readings from the **accelerometers**, **gyroscopes**, and **magnetometers** for each body part (torso, right arm, left arm, right leg, left leg):
  - Accelerometer readings (e.g., `T_xacc`, `RA_xacc`, etc.).
  - Gyroscope readings (e.g., `T_xgyro`, `LL_ygyro`, etc.).
  - Magnetometer readings (e.g., `RA_xmag`, `LL_zmag`, etc.).
  
---

# 4. Implementing a Web App using Streamlit and Plotly

### Overview:
To provide an interactive way for users to classify their own activities based on sensor data, I will implement a web application using **Streamlit**. This app will allow users to upload their own sensor data in CSV format and will provide real-time predictions on the activity being performed. I will also include exploratory data analysis (EDA) with **Plotly** to visualize the sensor data and insights.

### App Features:
1. **File Upload**: Users can upload their own sensor data files (in CSV format).
2. **Activity Classification**: The app will use a pre-trained machine learning model to predict the activity type based on the uploaded sensor data.
3. **EDA with Plotly**: The app will provide interactive visualizations of the uploaded sensor data using Plotly. Users will be able to explore the data through time-series plots, sensor readings comparison, and activity trends.



