# **Financial Market Analysis and Prediction Project**

## **Overview**
This is my Financial Market Analysis and Prediction project simple approach atempt. This repository houses my exploration into data science and its application to financial markets. The goal of this project is to analyse historical market data and economic indicators, importing different datasets in order to identify trends, build predictive models, compare them and then using one to give a future price prediciton.

## **Project Structure**
### **1. Data Retrieval and Preprocessing**
I've used Python for fetching historical stock prices of the S&P 500 index from Yahoo Finance using the yfinance library. Additionally, economic indicators such as inflation rate, interest rate, and labor openings have been obtained from the Federal Reserve Economic Data (FRED) API using the fredapi library.

### **2. Exploratory Data Analysis (EDA)**
To gain insights into the data, I've performed Exploratory Data Analysis using popular data analysis libraries like Pandas, Matplotlib, Seaborn, and NumPy. This includes visualizations of stock prices, inflation rates, interest rates, and labor openings over time.

### **3. Correlation Analysis**
I've explored the relationships between the S&P 500 index and economic indicators by calculating and visualizing the correlation matrix. This helps identify potential dependencies that could impact market movements.

### **4. Predictive Modeling**
I've implemented three different predictive models: Linear Regression, Random Forest, and Long Short-Term Memory (LSTM) Neural Network. These models in conjunction with indicators like moving averages, standard deviations, inflation rates, interest rates, and labor openings where combined to predict future price changes.

### **5. Model Evaluation**
Each model's performance has been assessed using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), Precision, Accuracy, and Z-Score. I've also conducted fit sampling experiments to evaluate model performance under different data distribution scenarios.

### **6. Model Comparison**
A comprehensive comparison table and visualizations showcase the strengths and weaknesses of each model, allowing for an informed choice depending on specific use cases.

**7. Updating with Up-to-Date Data**
I've demonstrated how to update historical data with the latest information from Yahoo Finance and FRED API, ensuring that the analysis remains relevant and adaptable to changing market conditions.
