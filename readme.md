# Simulation-Based Data Generation and Machine Learning Modeling using SimPy

This repository presents a simulation-driven approach to data generation and machine learning modeling. A discrete-event simulation is first developed using SimPy to model a service-based system. The synthetic data generated from the simulation is then used to train and evaluate multiple machine learning regression models to predict system performance.

The project demonstrates how simulation and machine learning can be combined to analyze complex systems and identify the most suitable predictive models.

---

## Simulation Framework

### SimPy (Discrete-Event Simulation in Python)

SimPy is a Python-based, process-oriented discrete-event simulation library used for modeling real-world systems such as queues, service centers, and networked systems. In this project, SimPy is used to simulate a service process and generate performance data under varying system configurations.

---

## Project Objective

The objectives of this project are:
- To design a simulation-based system model using SimPy
- To generate synthetic system performance data
- To apply and compare multiple machine learning regression algorithms
- To evaluate model performance using standard error metrics
- To identify the best-performing regression model

---

## Installation

To install the required simulation library, run:

pip install simpy

Additional dependencies include:
- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## System Model Description

### Simulated Service Process

The simulated system represents a basic service model where:
- Requests arrive at a defined arrival rate
- Each request requires a randomly distributed service time
- The system processes requests sequentially

The performance of the system is measured in terms of average service time, which varies based on the input parameters.

---

## Parameter Configuration

Two key system parameters are considered:

Parameter: Arrival Rate  
Description: Number of incoming requests per unit time  
Range: 1 to 10  

Parameter: Service Rate  
Description: Processing speed of the system  
Range: 5 to 20  

---

## Data Generation Process

- 1000 random combinations of arrival and service rates are generated using uniform sampling
- Each parameter combination is simulated independently
- A new SimPy environment is created for each simulation run
- The simulation is executed for a fixed duration
- The average service time is recorded as the output

This creates a dataset mapping system parameters to performance metrics.

---

## Dataset Details

Total simulations executed: 1000

Input Features:
- ArrivalRate
- ServiceRate

Target Variable:
- AvgServiceTime

---

## Machine Learning Models Implemented

The following regression models are trained and evaluated:
- Linear Regression
- K-Nearest Neighbors Regressor
- Support Vector Regressor
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor

---

## Evaluation Metrics

Model performance is evaluated using:
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score (Coefficient of Determination)

---

## Results

Model: Linear Regression  
RMSE: 0.02065  
MAE: 0.01528  
R² Score: 0.71395  

Model: KNN Regressor  
RMSE: 0.01806  
MAE: 0.01210  
R² Score: 0.78110  

Model: Support Vector Regressor  
RMSE: 0.06189  
MAE: 0.05762  
R² Score: -1.56953  

Model: Decision Tree Regressor  
RMSE: 0.02392  
MAE: 0.01625  
R² Score: 0.61627  

Model: Random Forest Regressor  
RMSE: 0.01798  
MAE: 0.01199  
R² Score: 0.78317  

Model: Gradient Boosting Regressor  
RMSE: 0.01698  
MAE: 0.01148  
R² Score: 0.80648  

---

## Visualization

A comparative RMSE plot is used to visualize the performance of different regression models. Lower RMSE values indicate better predictive accuracy. The visualization highlights the superior performance of ensemble-based models.

---

## Best Performing Model

Gradient Boosting Regressor achieved the best overall performance with the lowest error values and highest R² score. This demonstrates its ability to capture complex relationships in simulation-generated data.

---

## Conclusion

This project illustrates the effectiveness of combining discrete-event simulation with machine learning. Simulation-based data generation provides flexibility in exploring system behavior, while machine learning models enable accurate performance prediction. Ensemble regression techniques proved to be the most reliable for this task.

---

## Author

Vijayshree 

---

## License

This project is intended for academic and educational use.
