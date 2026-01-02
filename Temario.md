# Técnicas y Análisis de datos del Transporte

## Laboratorio \- Redes de transporte

## Objetivo

El presente laboratorio se propone como una instancia práctica en la que l@s participantes deberán comprender y ejecutar ejemplos escritos en Python. Con esto, se pretende fomentar tanto la búsqueda de claridad a la hora de plantear un problema como de autonomía para buscar la solución.  

El laboratorio se articula alrededor de la idea del transporte como “red”. La intención de esto es introducir a l@s participantes en nuevas estructuras de datos y formas de gestionarlos. Ya sean librerías, tipos de archivos o técnicas útiles para trabajar con redes de transporte.  

## Clases

1. **Práctica guiada n°1**

* **El grafo como estructura de datos: NetworkX**  
  * **Componentes de una red:**   
    * nodos y ejes  
    * visualización de una red  
  * **Tipos de grafos**  
    * dirigidos/no dirigidos  
    * ejes simples/multi ejes  
    * self-loops  
    * matrices de adyacencia  
  * **Métricas de una red:**  
    * grado del nodo  
    * grado promedio de una red  
    * centralidad y estimación de distancias  
    * uso de impedancias/pesos

2. **Práctica guiada n°2**  
* **Python aplicado al modelado de redes de transporte: BA Ecobici**  
  * Análisis de representación del transporte público de bicicletas aplicando teoría de grafos  
    * **Componentes de la red**:  
      * definición de los nodos y ejes de la red  
    * **Tipo de red**  
      * definición de la clase de grafo  
      * definición del límite de conexiones  
      * definición sobre el conteo de ejes (simples o paralelos)  
    * **Conectividad**  
      * localización de las estaciones: asignación de coordenadas  
      * evolución en el tiempo: densificación de la red  
      * métricas de centralidad: grado promedio de la red, grado de las estaciones, centralidad de grado de los nodos, etc.  
      * comportamiento de los nodos con alta centralidad  
      * conexiones entrantes y salientes  
      * análisis de adyacencia   
      * evolución en el tiempo: patrones de uso horario  
      * estimación de métricas de centralidad por hora   
      * visualización de las métricas de centralidad por hora y estación (In-Out)

3. **Prácticas guiadas n°3 y n°4**  
* **Otras librerías para el trabajo con redes viales**

  **OSMNx (I):**

  1. Setup inicial: settings para uso de log y cache  
     2. formas de instanciar geometrías a partir del Map Features de OSM o de una referencia geográfica: geometries from place, geocode to gdf & project  
     3. formas de instanciar y visualizar un grafo a partir de una red de calles con la API de OSM  
     4. formas de instanciar y visualizar un grafo a partir de distintos tipos de redes viales (pedestre, transporte vehicular, etc.): graph from bounding box, graph from point, graph from polygon,  graph from address & graph from place  
     5. implicancias del uso de los parámetros  network distance y network type en la construcción de un grafo.

     **OSMNx (II):**

     6. Simplificación de una red (identificación y remoción de nodos)  
     7. Visualización de los atributos de una red vial: largo de calles y calles de sentido único  
     8. Estadśiticas base: nodos, ejes, largo de calles, conteo de segmentos, circuito promedio, etc.  
     9. Área de cobertura de una red y proyección del CRS de un grafo  
     10. Cálculo y visualización de la centralidad de intermediación para los nodos y ejes de una red  
     11. Identificación del camino más corto entre pares de nodos: el uso de nearest nodes y shortest path routing

4. **Práctica guiada n°5: Isocronas**  
* **Análisis de accesibilidad espacial a partir de redes de transporte.**

  1. Concepto de isocronas y su relación con la accesibilidad

     2. Construcción de redes viales para análisis de isocronas

     3. Definición de puntos de origen (nodos centrales)

     4. Cálculo de áreas alcanzables según umbrales de tiempo o distancia

     5. Generación de subgrafos accesibles

     6. Visualización de isocronas sobre el territorio

     7. Comparación de escenarios de accesibilidad (distintos modos, tiempos o localizaciones)


5. **Opcional**  
* **Otras librerías para el trabajo con redes viales: Accesibilidad**

  **Pandana**:

  1. Construcción de una red vial a partir de un bounding box  
     2. Estimación de la cantidad de puntos de interés o pois  
     3. Agregación de métricas de accesibilidad  
     4. Estimación del nivel de oferta y demanda dentro de una red

     **Urban Access**:

     5. manipulación de archivos GTFS  
     6. creación de redes multimodales (pedestres y vehiculares)  
     7. estimación de tiempos de viaje a puntos de referencia dentro de una red.


  


  


  
**Lectura sugerida**

* Barabási, A.-L. (2016). [Network Science](https://eravilaipnada.wordpress.com/wp-content/uploads/2016/01/barabasi-2012.pdf). Cambridge University Press.  
* Bhatt, A., y Sinha, S. [Optimal Routes in Road Networks Using Graph Theory](https://www.researchgate.net/publication/275271950_Application_of_Graph_Theory_to_find_Optimal_Paths_for_the_Transportation_Problem)  
* Diestel, R. (2017). [*Graph Theory* (5th ed.)](https://www.emis.de/monographs/Diestel/en/GraphTheoryII.pdf). Springer.  
* Easley, D., & Kleinberg, J. (2010). [Graphs](https://www.cs.cornell.edu/home/kleinber/networks-book/networks-book-ch02.pdf). En D. Easley & J. Kleinberg (Eds.), [Networks, Crowds, and Markets: Reasoning About a Highly Connected World](https://www.cs.cornell.edu/home/kleinber/networks-book/) (pp. 23-46). Cambridge University Press.  
* Easley, D., & Kleinberg, J. (2010). [Networks in Their Surrounding Contexts](https://www.cs.cornell.edu/home/kleinber/networks-book/networks-book-ch04.pdf). En D. Easley & J. Kleinberg (Eds.), [Networks, Crowds, and Markets: Reasoning About a Highly Connected World](https://www.cs.cornell.edu/home/kleinber/networks-book/) (pp. 107-116). Cambridge University Press. Sección 4.5: Spatial Model of Segregation.  
* Stoilova, Svetla & Stoev, Veselin. (2015). [An application of the graph theory which examines the metro networks](https://www.researchgate.net/publication/283130334_An_application_of_the_graph_theory_which_examines_the_metro_networks). Transport Problems. 10\. 35-48. 10.21307/tp-2015-018. 

