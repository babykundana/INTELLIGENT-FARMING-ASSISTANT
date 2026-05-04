# INTELLIGENT-FARMING-ASSISTANT-

**Project Description**

This project presents an FPGA-based approach for crop recommendation and yield prediction using environmental parameters such as temperature, rainfall, humidity, soil type, and weather conditions. The objective is to develop a real-time agricultural decision support system that assists farmers in selecting suitable crops and estimating expected yield. A Decision Tree machine learning model is used due to its rule-based structure, which can be efficiently mapped into hardware. The trained model is converted into Verilog-based RTL and implemented on FPGA to perform on-device inference.

**Dataset**
Dataset: Crop Yield Dataset (Kaggle)
Link: https://www.kaggle.com/datasets/aarongebremariam/crop-yield
Features: Temperature, Rainfall, Humidity, Soil Type, Weather Conditions
Preprocessing: Continuous values converted into LOW, MID, HIGH categories and encoded numerically

**Methodology**

The system follows a structured pipeline:

1) Data collection from publicly available agricultural datasets
2) Preprocessing by discretizing environmental parameters into categorical levels
3) Encoding categorical data into numerical values for model compatibility
4) Dataset split into training (80%) and testing (20%)
5) Training a Decision Tree model in Python
6) Extracting decision rules from the trained model
7) Converting decision rules into Verilog-based RTL
8) Designing modular components: Crop Predictor and Yield Predictor
9) Integrating modules using a top-level design
10) Simulation and functional verification using FPGA design tools

**Algorithm (Decision Tree Implementation)**
1) Input environmental parameters are encoded into numerical values
2) Decision Tree evaluates conditions based on input features
3) Data is routed through conditional branches (if-else logic)
4) Final decision nodes produce outputs (crop type and yield level)
5) Decision rules are implemented using comparator-based logic in RTL
6) Multiple conditions are evaluated in parallel in hardware
7) Output is generated based on satisfied decision conditions

**Results**
1) The system successfully predicts crop type and yield based on given inputs.
2) Simulation results show that hardware outputs match software predictions across multiple test cases.
3) The design demonstrates correct implementation of Decision Tree logic in FPGA.

**Applications**
1) Smart agriculture decision support systems
2) Crop planning and resource optimization
3) Precision farming and yield estimation
4) Rural farming environments with limited connectivity

**Tools and Technologies**
1) Python
2) Decision Tree (Scikit-learn)
3) Verilog HDL
4) Xilinx Vivado

**Future Scope**
1) Extension to continuous yield prediction
2) Integration with real-time IoT sensor data
3) Support for multiple crops and larger datasets
4) Implementation of advanced ML models with hardware optimization
