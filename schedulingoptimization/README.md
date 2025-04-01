
# LHS Scheduling Optimization Demo

This repository contains a notebook file (`LHS_Scheduling_Optimization_Demo.ipynb`) that implements a scheduling optimization approach using linear programming with the PuLP library. This code can be run chunk by chunk to better understand the related paper published in Learning Health Systems Open Access journal. It will walk you through an example of how to optimize the scheduling of multiple appointments across various visit types and departments over a 14-day period, considering several constraints such as capacity, travel time, and user preferences.

## Getting Started

### Prerequisites

Make sure you have Python installed on your system. You will need the following libraries:

- NumPy
- PuLP
- Matplotlib (for visualization)

This demo was run using Python 3.10.12, NumPy 1.23.5, PuLP 2.7.0., and Matplotlib 3.7.1.


### Usage

1. Open the notebook file `LHS_Scheduling_Optimization_Demo.ipynb` in Google Colab.
2. Run each code cell in the notebook to execute the code and visualize the results.
3. Adjust the input parameters, such as visit types, job lengths, capacities, constraints, and preferences, to explore different scenarios.

## Creating an Instance of the Scheduler Class

In the notebook, an instance of the `Scheduler` class is created with the following main parameters:

- `N_VT`: Number of visit types.
- `N_DEP`: Number of departments.
- `VT_DEP`: Dictionary mapping visit types to the applicable departments.
- `JOB_LEN`: Array containing job lengths for different visit types (minutes).
- `DIS`: Matrix representing travel time between each pair of departments (minutes).
- `T_VT`: List of appointment window lengths for different visit types (minutes).
- `ST_DEP`: Start time of business hours for each department.
- `ED_DEP`: End time of business hours for each department.
- `Cap_14d`: Dictionary storing capacity of each department for each visit type and window unit.

## Running the Demo

1. After setting the required parameters, execute the notebook cells to run the optimization and obtain scheduling solutions.
2. Visualizations are provided to showcase the distribution of scheduled appointments and the optimized schedules for different scenarios.

## Additional Constraints and Preferences

This demo also supports additional constraints and preferences:

- `order_pref`: Matrix defining order constraints for visit types.
- `same_date`: Matrix defining same-day constraints for visit types.

To incorporate these constraints, modify the `_input` method calls in the notebook accordingly.
