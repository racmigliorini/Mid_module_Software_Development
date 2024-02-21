# Recursive Floyd-Warshall Algorithm

## Overview

This project implements a recursive version of the Floyd-Warshall algorithm for finding the shortest paths in a weighted graph. This approach contrasts with the traditional iterative method, leveraging recursion and memoization to efficiently compute the shortest distances between all pairs of vertices in the graph. Additionally, it incorporates a mechanism to detect negative cycles, which are crucial since they render the shortest path problem unsolvable.

## Features

- Recursive Implementation: Showcases a unique recursive solution to the shortest path problem, diverging from the conventional iterative dynamic programming methods.
- Memoization: Enhances computational efficiency by caching intermediate results, thus eliminating the need for recalculating solutions for previously solved subproblems.
- Negative Cycle Detection: Capable of identifying negative cycles within the graph, an essential feature for determining the feasibility of computing shortest paths.
- Visualization: Offers a visualization tool for the initial and final distance matrices, aiding in the intuitive understanding of the algorithm's results.
- Test Cases: Comes with a variety of test scenarios to verify the algorithm's accuracy across different types of graph configurations, including graphs with positive weights, negative weights, and negative cycles.

## Requirements
The project is developed in Python and requires Python 3.x for execution.

## Getting Started
To get a local copy up and running follow these simple steps:

1 - Clone the repository:

---------------------------------------------------
git clone https://github.com/racmigliorini/Mid_module_Software_Development.git
---------------------------------------------------

2 - Navigate to the project directory:

---------------------------------------------------
cd Mid_module_Software_Development
---------------------------------------------------

3 - Install the required dependencies (assuming you have Python and pip installed):

---------------------------------------------------
pip install matplotlib numpy
---------------------------------------------------

4 - Run the script to see the algorithm in action. Modify the graph in the script to test different scenarios:

---------------------------------------------------
python floyd_warshall_recursive.py
---------------------------------------------------

## Installation
No additional installation steps are required beyond the Python environment setup and the installation of dependencies listed in the "Getting Started" section.

## Usage
Invoke the floyd_warshall_recursive(graph) function with graph being a 2D list representing the graph's adjacency matrix, where float('inf') is used to denote no direct path between two vertices, and negative weights are allowed for edges.

Example graph definition and function call:

---------------------------------------------------
graph = [
    [0, 5, float('inf'), 10],
    [float('inf'), 0, 3, float('inf')],
    [float('inf'), float('inf'), 0, 1],
    [float('inf'), float('inf'), float('inf'), 0]
]

result, has_negative_cycle = floyd_warshall_recursive(graph)
print(result)

---------------------------------------------------

## License
This project is open-source and available under the MIT License. See the LICENSE file in the repository for more details.

## Contact Information
For any queries or further discussion regarding the project, please contact:

Ricardo Migliorini - sgrmigli@liverpool.ac.uk