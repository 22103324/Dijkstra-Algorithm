## Dijkstra's Algorithm Implementation

### Overview
This implementation of Dijkstra's algorithm finds the shortest paths from a source node to all other nodes in a graph. It maintains an array of structures to store the shortest distance from the source to each node and the list of predecessor nodes that make up the shortest paths.

### Functions

#### `createPredNode`

```c
PredNode *createPredNode(Vertex v);
void freePredList(PredNode *pred);
NodeData *dijkstra(Graph g, Vertex src);
Description: Implements Dijkstra's algorithm to find the shortest paths from the source node to all other nodes in the graph.

Parameters:

Graph g: The graph on which to run Dijkstra's algorithm.
Vertex src: The source vertex from which to calculate shortest paths.
Returns:

A pointer to an array of NodeData structures containing the shortest distances and predecessor lists.
Operation:

Initialization:
Allocate memory for the NodeData array, closest.
Initialize distances and predecessor lists.
Insert all nodes into the priority queue (PQ).
Processing Nodes:
Dequeue the node with the smallest distance (findNewV).
Update distances and predecessor lists for adjacent nodes.
Update the priority queue with new distances if a shorter path is found.
Return:
Return the NodeData array with the shortest distances and predecessor lists.
freeNodeData
c
Copy code
void freeNodeData(NodeData *data, int nV);
Description: Frees all memory associated with the given NodeData array.

Parameters:

NodeData *data: A pointer to the NodeData array to be freed.
int nV: The number of vertices in the graph.
Returns:

void
Operation:

Free the predecessor list for each entry in the NodeData array.
Free the NodeData array itself.
