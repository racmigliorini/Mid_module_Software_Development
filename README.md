# Recursive Floyd-Warshall Algorithm

## Overview

This project explores two distinct implementations of the Floyd-Warshall algorithm to determine the shortest paths within a weighted graph: an iterative approach and a recursive approach. The iterative method follows the classic algorithmic structure, systematically updating the shortest paths matrix in a series of loops. In contrast, the recursive approach capitalizes on the elegance of recursion coupled with memoization to compute the distances, potentially offering performance benefits in certain scenarios.

Both versions are designed to handle the challenges posed by negative cycles; they include checks to identify such cycles, which are pivotal in assessing the feasibility of finding a solution to the shortest path problem. The project's objective is to compare the performance and efficiency of the iterative and recursive methods, providing insight into their behavior under various graph conditions. The findings aim to inform the selection of an appropriate algorithmic strategy based on the specific requirements and characteristics of the graph in question.

## Features

- Recursive vs Iterative Implementation: Implements both recursive and iterative solutions to the shortest path problem, allowing for direct comparison of these approaches and demonstrating the unique characteristics of each.
- Efficient Memoization: Utilizes memoization in the recursive implementation to enhance computational efficiency by storing intermediate results. This optimization reduces the algorithm's time complexity by preventing redundant calculations.
- Robust Negative Cycle Detection: Equipped with a robust mechanism to detect negative cycles, a critical feature that assesses whether shortest paths can be reliably computed or if the graph contains unsolvable scenarios.
- Intuitive Visualization: Integrates a visualization component that graphically represents the initial and final state of distance matrices. This visual aid facilitates an intuitive grasp of the transformations the algorithm performs on the graph.
- Comprehensive Test Suite: Includes an extensive suite of test cases, designed to validate the algorithm's performance and correctness across diverse graph topologies and edge conditions, encompassing graphs with positive weights, negative weights, and the presence of negative cycles.

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
**pip install matplotlib numpy**

Note: Ensure you have the latest version of pip to avoid any installation issues. If you encounter any, try upgrading pip using pip install --upgrade pip and then rerun the dependency installation commands.
---------------------------------------------------

4 - Run the script to see the algorithm in action. Modify the graph in the script to test different scenarios:

---------------------------------------------------
python Floyd-Iterative.py
python Floyd-Recursive.py
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
