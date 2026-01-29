# GAC-Filter-Bed-Health
Explanation of the Hidden Markov Model (HMM) Carbon Filter Health Program
Assignment 4

Overview/What Problem This Program Solves
My company, Calgon Carbon, supplies/exchanges Granular Activated Carbon (GAC) to water treatment plants across the country. GAC filters play a critical role in water treatment systems by removing contaminants. Over time, the carbon becomes saturated, leading to a condition known as “breakthrough,” where the filter can no longer effectively capture impurities and contaminants begin to pass through (see images below for a visual explanation). 

The challenge is that the internal health of the filter cannot be directly observed. Operators rely solely on effluent concentration measurements, which are often noisy and inconsistent. Making decisions based on a single high or low reading can lead to costly mistakes, replacing filters too early wastes resources, while waiting too long risks regulatory non-compliance.

This program addresses that challenge by using a Hidden Markov Model (HMM) to infer the filter’s hidden health state over time. The model analyzes observed effluent concentration categories (e.g., Excellent, Good, High, Critical) and estimates the most likely underlying condition of the filter at each point, enabling smarter, data-driven maintenance decisions.
 
 


What the Model Assumes
Hidden Health States: The filter can be in one of four unobservable health states: Healthy, Mid-life, Near Breakthrough, Failed.

Observations: Effluent concentration measurements are categorized into six buckets relative to the regulatory limit.

Transition Probabilities  
Filters degrade gradually: Healthy → Mid-life → Near Breakthrough → Failed.

Emission Probabilities: Each hidden state has probabilities of producing each observation category.

What the Program Does
Step 1: Define the HMM
State labels, observation labels, transition probabilities, emission probabilities, and initial state probabilities are created.

Step 2: Simulate a Filter’s True Life  
A realistic sequence of health states and corresponding observations is generated.

Step 3: Apply the Viterbi Algorithm  
Uses dynamic programming to compute the most likely hidden sequence given all observations.

Step 4: Print Summary Outputs  
Tables show true vs estimated states, last 10 time steps, and distribution of states.

Step 5: Generate Visualizations  
Plots help illustrate the model’s reasoning and predictions.

