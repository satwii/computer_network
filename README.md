# Network Visualization and Shortest Path Algorithms

This project is a Python-based implementation for visualizing a computer network and calculating shortest paths using Dijkstra's and Bellman-Ford algorithms. The program also simulates congestion scenarios in the network and provides updated shortest path calculations.

## Features

1. **Network Visualization**:
   - Nodes represent devices such as PCs, switches, and routers.
   - Edges between nodes represent connections with weights.
   - Networks are visualized using the PyVis library.

2. **Shortest Path Algorithms**:
   - **Dijkstra's Algorithm**: Calculates the shortest path between two nodes.
   - **Bellman-Ford Algorithm**: Handles negative weights and detects negative-weight cycles.

3. **Congestion Simulation**:
   - Applies congestion scenarios to increase edge weights dynamically.
   - Updates the network to reflect these changes.

4. **Edge List and Adjacency Matrix Conversions**:
   - Converts between adjacency matrices and edge lists for easy manipulation.

## Requirements

- Python 3.x
- Libraries:
  - `pyvis`
  - `numpy`
  - `heapq`

Install the required libraries using:
```bash
pip install pyvis numpy
```

## File Structure

- `main.py`: Contains the implementation of the network visualization, shortest path calculations, and congestion simulations.

## Usage

### 1. Clone the Repository
Clone the repository from GitHub:
```bash
git clone https://github.com/your-repo-name/network-visualization.git
cd network-visualization
```

### 2. Run the Program
Run the program using Python:
```bash
python main.py
```

### 3. Output
- The program generates HTML files for visualizing the networks before and after applying congestion:
  - `node.html`: Original network visualization.
  - `node1.html`: Network after congestion scenario 1.
  - `node2.html`: Network after congestion scenario 2.
  - `node3.html`: Network after congestion scenario 3.
- Shortest paths and distances for each scenario are displayed in the console.

## Functions

### 1. `create_network()`
Creates a network with PCs, switches, and routers. Adds edges with default weights.

### 2. `create_adjacency_matrix(edges, num_nodes)`
Converts an edge list to an adjacency matrix.

### 3. `adjacency_matrix_to_edge_list(adjacency_matrix)`
Converts an adjacency matrix back to an edge list.

### 4. Shortest Path Algorithms:
- **`dijkstra(adjacency_matrix, start, end, num_nodes)`**:
  - Finds the shortest path using Dijkstra's algorithm.
- **`bellman_ford(adjacency_matrix, num_nodes, start, end)`**:
  - Finds the shortest path using Bellman-Ford algorithm and detects negative-weight cycles.

### 5. Congestion Simulation:
- **`apply_congestion_1(adjacency_matrix, n1, n2, n3)`**:
  - Increases edge weights for specific nodes to simulate congestion.
- **`apply_congestion_2(adjacency_matrix, n1, n2, n3)`**:
  - Simulates a different congestion pattern.
- **`apply_congestion_3(adjacency_matrix, n1, n2, n3)`**:
  - Simulates another congestion scenario.

### 6. Visualization:
- Uses `pyvis.Network` to create interactive network visualizations.

## Example Output

The program prints the following to the console:
- Generated edges and adjacency matrices.
- Shortest paths and distances before and after applying congestion.


If you have any issues or suggestions, feel free to open an issue on the GitHub repository.

