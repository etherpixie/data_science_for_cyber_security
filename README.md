# Data Science for Cyber Security


Welcome to the "Data Science for Cyber Security" GitHub repository!

This repository currently contains a Python Jupyter notebook script that uses a Monte Carlo simulation to calculate the total cyber-value-at-risk for a portfolio of cyber threats. The script is implemented using the Pandas library for data manipulation, the NumPy library for numerical operations, the Matplotlib library for visualization and the random library for generating random numbers.

The script first defines a Pandas DataFrame with the cyber events, probability of occurrence and the impact in dollars in a upper and lower range. It then defines four functions:

<b>is_attack_successful(probability):</b> This function generates a random number between 0 and 1 and checks if it is less than or equal to the probability passed as an argument. If it is, the attack is considered successful and the function returns True. If not, it returns False.

<b>calculate_loss(lower, upper):</b> This function generates a random number between the lower and upper bounds passed as arguments and returns it.

<b>simulate_risk_portfolio(cyber_threats):</b> This function iterates over each risk in the cyber_threats DataFrame and checks if the attack is successful using the is_attack_successful function. If it is, it calculates the loss using the calculate_loss function and adds it to the total loss. It returns the total loss.

<b>monte_carlo_simulation(cyber_threats, iterations): </b> This function runs the simulation by calling the simulate_risk_portfolio function for the number of iterations passed as an argument. It stores the result of each iteration in the losses_per_year list and returns it.

The script then uses the monte_carlo_simulation function to generate a set of losses and plots these losses using the Matplotlib library. The script also generates a Loss Exceedance Curve which is a powerful tool for visualizing and understanding the risk of the cyber portfolio.

This repository is intended to be a resource for anyone interested in understanding the basics of Monte Carlo simulations and how they can be applied to cyber risk analysis. 

I am passionate about translating complex topics like Monte Carlo into approachable language and I hope this repository helps make this topic more accessible to a wider audience.
