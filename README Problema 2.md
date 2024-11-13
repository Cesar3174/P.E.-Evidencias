# Problema 155. Min Stack. Leetcode


## LINK DEL PROBLEEMA:
https://leetcode.com/problems/min-stack/description/


## EXPLICACIÓN DEL PROBLEMA 
Este problema "Min Stack" consiste en implementar una estructura que es una pila que permite realizar las operaciones básicas de una pila, 
como agregar y eliminar elementos, con una funcionalidad adicional, la de obtener el valor mínimo en la pila en cualquier momento.
A esto podemos agregar que las operaciones de la pila son las siguientes: 
push: Agregar un elemento a la cima de la pila.
pop: Eliminar el elemento de la cima de la pila.
top: Obtener el elemento de la cima sin eliminarlo.

Dado que MinStack es una variación de una pila estándar que añade una operación adicional:
getMin: Obtener el valor mínimo actual de la pila en tiempo constante O(1).

Para implementar esta funcionalidad de obtener el mínimo en tiempo constante, se utiliza una pila auxiliar que guarda solo los valores mínimos.

## ELECCIÓN FORMA DE SOLUCÓN
En este caso ya se nos proporciona tanto la clase que se debe de implementar como las acciones que una pila realiza y 
que deben de quedar en el código, por lo tanto solo se siguieron esas partes para poder ejecutar el código, 
y claro se fue observando los casos de prueba y las respuestas esperadas para ver si estaba saliendio o 
si se tenían que hacerr modificaciones al código.
Se siguieron los siguientes requerimientos dados en el problema:
1. MinStack(): Constructor que inicializa una instancia vacía del MinStack.

2. push(int val): Agrega un elemento "val" a la cima de la pila. Si este valor es menor o igual al valor actual mínimo, 
también se añade a la pila auxiliar de mínimos.

3. pop(): Elimina el elemento en la cima de la pila. Si este valor es igual al valor en la cima de la pila de mínimos, 
también se elimina de la pila de mínimos.

4. top(): Devuelve el elemento en la cima de la pila principal sin eliminarlo.

5. getMin(): Devuelve el valor mínimo actual en la pila, el cual es el elemento en la cima de la pila de mínimos.

## FUNCIONAMIENTO
El funcionamiento de la solución se basa en el uso de dos pilas:

Una pila dataStack que guarda todos los elementos.
Una pila minStack que guarda los valores mínimos actuales.

Así, cada que agregamos un valor a dataStack, también verificamos si es menor o igual al mínimo actual. Si lo es, lo añadimos a minStack.
Cuando eliminamos un valor de dataStack, también eliminamos el valor en minStack si coincide, garantizando que el mínimo siempre 
se mantenga actualizado.

Esta solución permite que cada operación (push, pop, top, getMin) tenga una complejidad constante O(1), cumpliendo así con los
requisitos del problema.

## COMPLEJIDAD
Compeljidad temporal: Todas las operaciones (push, pop, top, getMin) tienen una complejidad de tiempo constante; en el caso de push, 
porque solo estamos comparando con el último valor en minStack y no  estamos recorriendo ningún elemento; pop, es una operación de 
tiempo constante O(1) en ambas pilas, porque solo estamos quitando el elemento en la cima, sin necesidad de iterar sobre otros elementos; 
top, se accede al elemento en la cima de una pila, como el elemento está siempre en una posición fija que es la cima de la pila pues no 
depende del tamaño de la pila; getmin, como siempre está en en la cima de minStack y se puede acceder en tiempo constante O(1).

La complejidad espacial: Es O(n), donde n es el número de elementos en la pila:O(1)




