# Problema 912. Sort an Array. Leetcode

## LINK DEL PROBLEEMA:
https://leetcode.com/problems/sort-an-array/submissions/?source=submission-ac

## EXPLICACIÓN DEL PROBLEMA 
Este problema "Sort an Array" conciste en en ordenar un arreglo de números enteros llamado "nums" en orden ascendente y 
devolver el arreglo de manera ya ordenada. El código debe de  garantizar que el algoritmo tenga una complejidad temporal de O(nlogn) y 
una complejidad espacial mínima. De acuerdo a esto llegamos a la conclusión de utilizar métodos como el merge sort o el quick sort, 
en este caso utilizaremos marge sortpor su estabilidad y su estructura que es relativamente sencilla.

## ELECCIÓN MERGE SORT
1. Complejidad Temporal: El requisito de O(nlogn) descarta los algoritmos de ordenamiento más simples como el bubble sort o el insertion sort, 
que tienen complejidad O(n^2).
2. Consumo de Espacio: Aunque Merge Sort requiere espacio adicional para el arreglo temporal "temp", esgo garantiza la complejidad temporal 
necesaria y es relativamente sencillo de implementar en este problema.
3. Estabilidad: Merge Sort es un algoritmo estable, lo que significa que si hay elementos con el mismo valor en el arreglo, 
el algoritmo mantiene el orden en que aparecían originalmente, esto nos ayuda cuando hay duplicados

## FUNCIONAMIENTO MERGE SORT
El Merge Sort funciona de la siguiente manera, se centra en dividir el arreglo en partes más pequeñas hasta llegar a arreglos de un solo tamaño,
y luego combinar estas partes en orden para formar el arreglo completo y ordenado, siguiendo esto nos asegura una complejidad temporal de 
O(nlogn)del proceso.
Por poner el ejemplo de las pruebas, el arreglo es [5,2,3,1]
El paso a realizar primeramente es dividir el arreglo en dos mitades de manera recursiva hasta que cada subarreglo contiene solo un elemento, 
[5, 2] y [3, 1], Estos subarreglos se dividen nuevamente hasta llegar a [5], [2], [3], y [1], combina [5] y [2] en [2, 5] y [3] y [1] en
[1, 3] y finalmente se  combina [2, 5] y [1, 3] en el arreglo completo y ordenado [1, 2, 3, 5].

## COMPLEJIDAD
1. Temporal: O(nlogn), ya que en cada nivel de la recursión dividimos el arreglo en dos mitades y luego combinamos, lo cual resulta en un total 
de logaritmos multiplicados por el tamaño del arreglo.
2. Espacial: Usamos un arreglo temporal para combinar las partes ordenadas, lo cual es necesario para que merge rort funcione de manera correcta




