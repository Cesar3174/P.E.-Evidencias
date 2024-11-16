# Problema 98. Validate Binary Search Tree. Leetcode

## LINK DEL PROBLEEMA:
https://leetcode.com/problems/validate-binary-search-tree/submissions/

## EXPLICACIÓN DEL PROBLEMA 
En este problema, la situación consiste en determinar si un árbol binario es un árbol de búsqueda binaria (BST). Un BST tiene la propiedad de que, para cada nodo, todos los valores en su subárbol izquierdo son menores y todos los valores en su subárbol derecho son mayores que el valor del nodo. De tal manera que al final, la respuesta será determinada por medio de un true o un false,dependiendo de si es un árbol de búsqueda binaria o no.

## ELECCIÓN DE FORMA SOLUCIÓN Y FUNCIONAMIENTO
Primero nos guiamos por las especificaciones que vienen el problema para determinar lo que caracteriza a un árbol de búsqueda binaria, 
y revisamos las imágenes que se nos brinda para entender un poco más,después determinamos lo siguiente: 
Un nodo debe ser mayor que todos los nodos en su subárbol izquierdo y menor que todos los nodos en su subárbol derecho. 
Para implementar esto, se utilizan dos límites: un límite mínimo (minVal) y un límite máximo (maxVal) para cada nodo y  
estos límites se actualizan a medida que se desciende por el árbol; se utilizo una función recursiva que toma el nodo actual y 
sus límites como parámetros. Si el nodo es nullptr es válido. Para un nodo no nulo, se verifica si su valor está dentro del rango permitido. 
Si no lo está, se devuelve false.
La función se llama recursivamente para los nodos izquierdo y derecho, actualizando los límites según la regla del BST.
Por último, la refursión también se detiene cuando se alcanzan nodos nulos porque un árbol vacío es un BST válido y por lo tanto aparce un true.

## COMPLEJIDAD
Temporal: La complejidad temporal de esta solución es O(n), donde n es el número de nodos en el árbol, ya que cada nodo se visita una vez. 
Espacial: La complejidad espacial es O(h), donde h es la altura del árbol, debido a la pila de llamadas de la recursión. En el peor de los casos, un árbol muy desbalanceado podría tener una altura de n, pero en un árbol balanceado, la altura sería O(logn).





