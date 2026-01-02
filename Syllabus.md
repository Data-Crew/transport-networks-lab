# Transport Data Techniques and Analysis

## Lab \- Transport Networks

## Objective

This lab is designed as a hands-on session where participants will understand and execute Python-based examples. The goal is to encourage both clarity when framing a problem and autonomy when seeking solutions.

Lab is structured around the concept of transport as a "network". The intention is to introduce participants to new data structures and ways of managing them—whether libraries, file types, or techniques useful for working with transport networks.

## Classes

1. **Guided Practice #1**

* **The graph as a data structure: NetworkX**
  * **Network components:**
    * nodes and edges
    * network visualization
  * **Types of graphs**
    * directed/undirected
    * simple edges/multi-edges
    * self-loops
    * adjacency matrices
  * **Network metrics:**
    * node degree
    * average network degree
    * centrality and distance estimation
    * use of impedances/weights

2. **Guided Practice #2**
* **Python applied to transport network modeling: BA Ecobici**
  * Analysis of public bicycle transport representation using graph theory
    * **Network components**:
      * definition of network nodes and edges
    * **Network type**
      * definition of graph class
      * definition of connection limits
      * definition of edge counting (simple or parallel)
    * **Connectivity**
      * station location: coordinate assignment
      * evolution over time: network densification
      * centrality metrics: average network degree, station degree, node degree centrality, etc.
      * behavior of high-centrality nodes
      * incoming and outgoing connections
      * adjacency analysis
      * evolution over time: hourly usage patterns
      * hourly centrality metrics estimation
      * visualization of centrality metrics by hour and station (In-Out)

3. **Guided Practices #3 and #4**
* **Other libraries for working with road networks**

  **OSMNx (I):**

  1. Initial setup: settings for log and cache usage
     2. Ways to instantiate geometries from OSM Map Features or a geographic reference: geometries from place, geocode to gdf & project
     3. Ways to instantiate and visualize a graph from a street network using the OSM API
     4. Ways to instantiate and visualize a graph from different types of road networks (pedestrian, vehicular transport, etc.): graph from bounding box, graph from point, graph from polygon, graph from address & graph from place
     5. Implications of using the network distance and network type parameters in graph construction

     **OSMNx (II):**

     6. Network simplification (node identification and removal)
     7. Visualization of road network attributes: street length and one-way streets
     8. Basic statistics: nodes, edges, street length, segment count, average circuit, etc.
     9. Network coverage area and graph CRS projection
     10. Calculation and visualization of betweenness centrality for network nodes and edges
     11. Identification of the shortest path between node pairs: using nearest nodes and shortest path routing

4. **Guided Practice #5: Isochrones**
* **Spatial accessibility analysis from transport networks.**

  1. Isochrone concept and its relationship with accessibility

     2. Building road networks for isochrone analysis

     3. Defining origin points (central nodes)

     4. Calculating reachable areas based on time or distance thresholds

     5. Generating accessible subgraphs

     6. Visualizing isochrones over the territory

     7. Comparing accessibility scenarios (different modes, times, or locations)


5. **Optional**
* **Other libraries for working with road networks: Accessibility**

  **Pandana**:

  1. Building a road network from a bounding box
     2. Estimating the number of points of interest (POIs)
     3. Aggregating accessibility metrics
     4. Estimating supply and demand levels within a network

     **Urban Access**:

     5. GTFS file manipulation
     6. Creating multimodal networks (pedestrian and vehicular)
     7. Estimating travel times to reference points within a network




**Suggested Reading**

* Barabási, A.-L. (2016). [Network Science](https://eravilaipnada.wordpress.com/wp-content/uploads/2016/01/barabasi-2012.pdf). Cambridge University Press.
* Bhatt, A., & Sinha, S. [Optimal Routes in Road Networks Using Graph Theory](https://www.researchgate.net/publication/275271950_Application_of_Graph_Theory_to_find_Optimal_Paths_for_the_Transportation_Problem)
* Diestel, R. (2017). [*Graph Theory* (5th ed.)](https://www.emis.de/monographs/Diestel/en/GraphTheoryII.pdf). Springer.
* Easley, D., & Kleinberg, J. (2010). [Graphs](https://www.cs.cornell.edu/home/kleinber/networks-book/networks-book-ch02.pdf). In D. Easley & J. Kleinberg (Eds.), [Networks, Crowds, and Markets: Reasoning About a Highly Connected World](https://www.cs.cornell.edu/home/kleinber/networks-book/) (pp. 23-46). Cambridge University Press.
* Easley, D., & Kleinberg, J. (2010). [Networks in Their Surrounding Contexts](https://www.cs.cornell.edu/home/kleinber/networks-book/networks-book-ch04.pdf). In D. Easley & J. Kleinberg (Eds.), [Networks, Crowds, and Markets: Reasoning About a Highly Connected World](https://www.cs.cornell.edu/home/kleinber/networks-book/) (pp. 107-116). Cambridge University Press. Section 4.5: Spatial Model of Segregation.
* Stoilova, Svetla & Stoev, Veselin. (2015). [An application of the graph theory which examines the metro networks](https://www.researchgate.net/publication/283130334_An_application_of_the_graph_theory_which_examines_the_metro_networks). Transport Problems. 10. 35-48. 10.21307/tp-2015-018.

