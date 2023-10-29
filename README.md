# Algoritmo de Dijkstra

## Introducción
El algoritmo de Dijkstra es un método eficiente para encontrar la ruta más corta entre un nodo de origen y todos los demás nodos en un grafo ponderado. Este algoritmo es particularmente útil en el ámbito de las redes de computadoras, sistemas de navegación, y en diversos campos de la informática y la ingeniería.

## Descripción del Algoritmo de Dijkstra
El algoritmo de Dijkstra trabaja manteniendo un conjunto de nodos cuyas distancias más cortas desde el nodo de origen son conocidas. Inicialmente, este conjunto sólo contiene al nodo de origen, y la distancia al nodo de origen desde sí mismo es 0. Para el resto de los nodos, la distancia inicial es infinito. En cada paso, el algoritmo selecciona el nodo con la distancia más corta desde el nodo de origen que aún no ha sido procesado. Luego, actualiza las distancias a sus nodos adyacentes si encuentra un camino más corto a través del nodo seleccionado. Este proceso se repite hasta que se han procesado todos los nodos.

## Implementación en Java
### Clases y Estructuras Utilizadas
- **Nodo**: Representa un nodo en el grafo. Contiene un identificador, una lista de aristas (vecinos), y variables para almacenar la distancia más corta desde el nodo de origen, un puntero al nodo previo en el camino más corto, y una marca para indicar si el nodo ya ha sido visitado.
  
- **Arista**: Representa una arista en el grafo. Contiene un nodo de destino y un peso (distancia).
  
- **Dijkstra**: Contiene el método estático dijkstra para ejecutar el algoritmo. Utiliza una cola de prioridad para seleccionar siempre el nodo con la distancia más corta pendiente de procesar.

### Desafíos y Soluciones
- **Representación del Grafo**: Opté por una lista de nodos y una lista de aristas por cada nodo para representar sus conexiones. La matriz de adyacencia fue utilizada para construir estas estructuras.
  
- **Inicialización**: Fue crucial asegurarse de que la distancia del nodo de origen a sí mismo se estableciera en 0.
  
- **Selección del Nodo de Distancia Mínima**: Utilicé una cola de prioridad basada en las distancias de los nodos. 
  
- **Actualización de las Distancias**: Aquí fue crucial comprobar si el nodo ya había sido visitado para evitar trabajar innecesariamente en nodos que ya tenían su distancia mínima encontrada.
  
- **Resultados y Verificación**: Tras implementar el algoritmo, imprimí los resultados para verificar su correcto funcionamiento.


  <img width="1512" alt="Captura de pantalla 2023-10-29 a la(s) 1 44 33 p m" src="https://github.com/annlima/DijkstraAlgorithm/assets/89811870/e9309c2c-5830-4afd-9830-1402ac890dc5">

## Complejidad Algorítmica
La complejidad temporal del algoritmo de Dijkstra depende de las estructuras de datos utilizadas. Si se utiliza una cola de prioridad basada en un min_heap, la complejidad temporal es O(|V| + |E| log |V|), donde |V| es el número de nodos y |E| es el número de aristas.

## Conclusión
La implementación del algoritmo de Dijkstra en Java proporcionó una valiosa experiencia en la manipulación de estructuras de datos y la implementación de algoritmos de grafos. A pesar de los desafíos enfrentados, la estrategia de dividir el problema en partes manejables y abordar cada parte paso a paso resultó ser eficaz. Este algoritmo no sólo es fundamental en teoría de grafos, sino que también tiene aplicaciones prácticas en diversas áreas de la informática y la ingeniería.

