# Data Science for Cyber Security


Welcome to the "Data Science for Cyber Security" GitHub repository!

This repository currently contains two Python Jupyter notebook scripts:<br>

1 - <a href="https://github.com/etherpixie/data_science_for_cyber_security/blob/main/Monte%20Carlo%20for%20Cyber-Threats.ipynb">Monte Carlo for Cyber-Threats.ipynb</a> uses a Monte Carlo simulation to calculate the total cyber-value-at-risk for a portfolio of cyber threats. <br>
2 - <a href="https://github.com/etherpixie/data_science_for_cyber_security/blob/main/I%20-%20Credit%20card%20fraud%20detection%20with%20Random%20Forest.ipynb">I - Credit card fraud detection with Random Forest.ipynb</a> addresses an imbalanced dataset and uses a random forest classifier in credit card fraud detection.

<H2>MONTE CARLO FOR CYBER RISK</H2>
The script is implemented using the Pandas library for data manipulation, the NumPy library for numerical operations, the Matplotlib library for visualization and the random library for generating random numbers.

The script first defines a Pandas DataFrame with the cyber events, probability of occurrence and the impact in dollars in a upper and lower range. It then defines four functions:

<b>is_attack_successful(probability):</b> This function generates a random number between 0 and 1 and checks if it is less than or equal to the probability passed as an argument. If it is, the attack is considered successful and the function returns True. If not, it returns False.

<b>calculate_loss(lower, upper):</b> This function generates a random number between the lower and upper bounds passed as arguments and returns it.

<b>simulate_risk_portfolio(cyber_threats):</b> This function iterates over each risk in the cyber_threats DataFrame and checks if the attack is successful using the is_attack_successful function. If it is, it calculates the loss using the calculate_loss function and adds it to the total loss. It returns the total loss.

<b>monte_carlo_simulation(cyber_threats, iterations): </b> This function runs the simulation by calling the simulate_risk_portfolio function for the number of iterations passed as an argument. It stores the result of each iteration in the losses_per_year list and returns it.

The script then uses the monte_carlo_simulation function to generate a set of losses and plots these losses using the Matplotlib library. The script also generates a Loss Exceedance Curve which is a powerful tool for visualizing and understanding the risk of the cyber portfolio.

This script is intended to be a resource for anyone interested in understanding the basics of Monte Carlo simulations and how they can be applied to cyber risk analysis. 

<H2>CREDIT CARD FRAUD WITH RANDOM FOREST</H2>
The script is a demonstration of using a random forest classifier to detect credit card fraud, and comparing the performance of the model when trained on imbalanced data versus oversampled data.

The evaluation metrics used are F1 score, recall, accuracy, and precision, which are calculated using the functions from the scikit-learn library as previously explained.

The original data used for training the model has an imbalanced distribution, where the majority of the transactions are non-fraudulent. This can lead to a biased model, as it may have a high accuracy in predicting the majority class, but a low recall in detecting fraudulent transactions.

To tackle the issue of imbalanced data, the data is oversampled using the Synthetic Minority Over-sampling Technique (SMOTE) method. SMOTE generates synthetic samples of the minority class to balance the class distribution.

The code then trains the random forest classifier on both the original imbalanced data and the oversampled data, and the results are compared. The results show that the use of oversampled data leads to an improvement in the recall of fraudulent transactions, which is a crucial metric in credit card fraud detection.

I am passionate about translating complex topics into approachable language and I hope this repository helps make this topic more accessible to a wider audience.
