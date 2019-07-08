# Thesis

## Agent-based modeling and simulation of public transport to identify effects of network changes on passenger flows
This research looks at the application of an agent-based model to assess the effects of changes in public transport on passenger flows. Data from public transport company GVB was provided by the municipality of Amsterdam. A baseline model was created based on domain knowledge, literature and data. This model was used to simulate a baseline scenario and a scenario with a malfunctioning tram line. The simulations show that the malfunctions result in different occupancy levels of several lines and cause an increase in waiting time for a lot of people. Future research should be aimed at implementing the model for the complete transport network in Amsterdam and expanding the behaviour of the different agent types.

## Code
The code is based on the Transport Network Analysis module of TU Delft. All code can be found in a seperate branch there: https://github.com/TUDelft-CITG/Transport-Network-Analysis/tree/Afstuderen_SophieEnsing/notebooks

### Notebooks
* Preprocessing data.ipynb: this notebook handles all preprocessing of the GVB data. It handles the date ranges and all stops that were used in this research. The stops had to be altered and the trip statistics normalized since not all transport lines were used. 
* Basic Simulation.ipynb: used GVB data and csv files to create a population and transport network. For all lines vehicles are created with the appropriate schedule. People are generated based on the probability distributions. All people get an origin and destination. All routes are calculated and based on their preferances a route is chosen. All results are stored for further data analysis.
* Data Analysis - Occupancy.ipynb: this notebook is used to analyse the occupation of all different vehicles in the simulation.
* Data Analysis - Sub-trip.ipynb: this notebook is used to compare the sub-trips in the simulation with all sub-trips in the GVB data.
* Data Analysis - Trip.ipynb: this notebook is used to compare the origin and destinations between the simulation and GVB data.
* Example 14 - Pick up variable load.ipynb: this notebook was provides by TU Delft as a basis for this thesis project.

### Data folder
* lines.csv: all lines that were used with their numbers, directions, routes, frequency and durations.
* linesdelay.csv: all lines, but times are altered to simulate a situation with delays in tram 12.
* stations.csv: all stations used in the network with name and coordinates. Capacity is an extra column that can be used in future iterations.
* destination csv files: all possible destinations with probabilities for all days.
* origin csv files: all possible origins with probabilities for all days.

## Future research
1. Implement this method for the complete network. This research should be focused on the heuristics of route calculation. Since there will be a lot more options and overlapping lines, the route calculation needs to be improved. By using heuristics and implementing new rules, it can be tested how well the model performs as a baseline for the complete network.
2. Further research needs to be done regarding passenger behaviour. For now, only three classes exist and they are distributed evenly over the complete population. More qualitative research about passenger preferences and behaviour is necessary to improve the model.
