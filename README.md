# Traveling Salesman Problem using Self-Organizing Map 

This repository contains a Python implementation of solving the Traveling Salesman Problem (TSP) using a Self-Organizing Map (SOM). The SOM is a neural network-based algorithm used to cluster and optimize the order of visiting a set of cities in the TSP.

## Algorithm Used

The TSP is solved using the following algorithm:

- **Input Reading**: The algorithm reads the city locations from an input file and initializes some global variables.
- **Random Weight Initialization**: Initial weights (representing city locations) are assigned randomly within the range of the city coordinates. These weights form the basis for the SOM.
- **Clustering Step**: The algorithm uses SOM to cluster the city locations into groups. Overlapping points are removed, and each city is assigned to the nearest cluster.
- **Finding Best Permutations**: For each cluster, the algorithm finds the best order (permutation) to visit the cities within that cluster by checking all possible permutations and selecting the one with the minimum total distance.
- **Connecting Clusters**: Finally, the algorithm connects the clusters by finding the order in which to visit the clusters. This is done by connecting the starting and ending points of different clusters.
- **Visualization**: The algorithm provides visualizations of the clusters, the best permutations within clusters, and the overall TSP solution.

## Parameters

- `input_file`: The name of the input file containing the city coordinates.
- `weights_num`: The number of initial random weights (representing neurons in the SOM).
- `alpha`: A parameter controlling the learning rate during SOM training.
- `neighbor_num`: The number of neighbors considered during SOM training.
- Other parameters are set internally within the code and may not need to be modified.

## Usage

To use this algorithm, follow these steps:

1. Clone this repository to your local machine.
2. Install the required Python libraries, such as NumPy and Matplotlib.
3. Prepare an input file with the coordinates of the cities in the TSP problem.
4. Modify the parameters in the code if needed.
5. Run the code by executing the Python script.
6. The algorithm will cluster the cities, find the best permutations within clusters, and connect clusters to solve the TSP. Visualizations will also be provided.

## Example

Here's an example of how to run the algorithm:

```
alpha = 0.999
main('input_file.tsp', 29)
```
Input examples can be found in HW7.pdf file.
## Results:
The algorithm will display visualizations of the clusters, the best permutations within clusters, and the overall TSP solution. The total distance of the TSP solution will be printed as well.

Please note that the algorithm's performance may vary depending on the choice of parameters and the complexity of the TSP instance. Experiment with different parameter values to obtain the best results for your specific problem.
