## Dijkstra's Algorithm Implementation

### Overview
This implementation of Dijkstra's algorithm finds the shortest paths from a source node to all other nodes in a graph. It maintains an array of structures to store the shortest distance from the source to each node and the list of predecessor nodes that make up the shortest paths.

### Functions
# Dijkstra API Implementation
===========================

### `createPredNode(Vertex v)`
#### Description
Creates a new `PredNode` with the given vertex `v`.
#### Returns
A pointer to the newly created `PredNode`.

### `freePredList(PredNode *pred)`
#### Description
Frees the entire predecessor list starting from the given `PredNode` `pred`.

### `dijkstra(Graph g, Vertex src)`
#### Description
Finds the shortest paths from the source node `src` to all nodes in the graph `g`.
#### Returns
An array of `NodeData` structures containing the distance and predecessor list for each node.

### `freeNodeData(NodeData *data, int nV)`
#### Description
Frees all memory associated with the given `NodeData` array `data`.
#### Parameters
* `data`: The `NodeData` array to free.
* `nV`: The number of vertices in the graph.

## Data Structures

### `PredNode`
#### Description
Represents a node in the predecessor list.

### `NodeData`
#### Description
Represents the shortest path data for a node, including distance and predecessor list.
