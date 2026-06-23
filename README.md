# Traffic Network Analysis Using Graph Theory, Centrality Measures and Network Robustness Analysis

# Traffic Network Analysis Using Graph Theory, Centrality Measures and Network Robustness Analysis

![Traffic Network](figures/betweenness_network.png)

## Project Overview

This project models a transportation network as a weighted graph and applies graph-theoretic techniques to analyze traffic flow, identify critical intersections, optimize routes, and evaluate network resilience.

Using Python and NetworkX, the project investigates:

- Degree Centrality
- Closeness Centrality
- Betweenness Centrality
- Dijkstra's Shortest Path Algorithm
- Articulation Point Detection
- Bridge Detection
- Network Robustness Analysis

## Objectives

- Model a traffic network as a weighted graph.
- Identify influential intersections using centrality measures.
- Determine optimal routes using Dijkstra's algorithm.
- Detect critical infrastructure using articulation point and bridge analysis.
- Evaluate network resilience through targeted node removal.

## Methodology

### 1. Network Construction

A weighted transportation network consisting of 15 intersections (nodes) and 22 roads (edges) was created using NetworkX. Edge weights represent travel costs between intersections.

### 2. Centrality Analysis

The following centrality measures were computed:

- Degree Centrality
- Closeness Centrality
- Betweenness Centrality

These metrics were used to identify influential and high-impact intersections within the network.

### 3. Shortest Path Analysis

Dijkstra's algorithm was applied to determine the optimal route between selected locations in the transportation network.

### 4. Structural Analysis

The network was analyzed for:

- Articulation Points
- Bridges

to identify critical infrastructure components whose failure could disconnect the network.

### 5. Robustness Analysis

The node with the highest betweenness centrality was removed to evaluate network resilience. Changes in connectivity and average shortest path length were measured.

## Results

### Network Statistics

| Metric | Value |
|----------|---------:|
| Nodes | 15 |
| Edges | 22 |
| Density | 0.2095 |

### Top Betweenness Centrality Nodes

| Rank | Node | Betweenness |
|------|------|------------:|
| 1 | H | 0.3077 |
| 2 | E | 0.2505 |
| 3 | K | 0.2505 |
| 4 | G | 0.1681 |
| 5 | I | 0.1681 |

### Shortest Path Analysis

Optimal route from A to O:

A → D → E → H → I → L → O

Total travel cost:

15

### Structural Analysis

Articulation Points:

None

Bridges:

None

### Robustness Analysis

Average shortest path length before removing H:

7.1238

Average shortest path length after removing H:

9.7473

Percentage increase:

36.8%

The network remained connected after removal of the highest-betweenness node, although routing efficiency decreased significantly.

## Conclusion

The traffic network was modeled as a weighted graph and analyzed using graph-theoretic techniques. Centrality analysis identified node H as the most influential intersection in the network. Dijkstra's algorithm successfully determined optimal routes between locations. Structural analysis revealed no articulation points or bridges, indicating a resilient network design. Robustness testing demonstrated that the network remained connected after removal of the highest-betweenness node, although average routing efficiency decreased by approximately 36.8%.

These results highlight how graph theory can be applied to transportation planning, route optimization, and infrastructure resilience assessment.

## Project Structure

traffic-network-analysis/

├── notebook/

│ └── traffic_network_analysis.ipynb

├── figures/

│ └── betweenness_network.png

├── README.md

└── requirements.txt

## Technologies Used

- Python
- NetworkX
- Matplotlib
- NumPy
- Google Colab
- Graph Theory