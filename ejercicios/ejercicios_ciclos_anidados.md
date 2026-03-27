# Recomendaciones generales

* Analice con cuidado qué hace el ciclo externo y qué hace el ciclo interno.
* Cuando sea necesario, use contadores o acumuladores.
* Antes de programar, trate de escribir en papel qué debe ocurrir en cada fila.
* Pruebe sus programas con valores pequeños antes de usar valores más grandes.
* Realice las pruebas de escritorio de las soluciones que plantee

---

# Taller de práctica: ciclos anidados

## 1. Repetición del número de la fila

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir un patrón en el que cada fila contenga repetido el número de la fila la cantidad de veces correspondiente.

Ejemplo para `n = 4`:

```text
1
2 2
3 3 3
4 4 4 4
```

---

## 2. Patrón alternado de 0 y 1

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir `n` filas. En cada fila se deben mostrar valores alternados entre `0` y `1`, comenzando siempre en `0`.

Ejemplo para `n = 4`:

```text
0
0 1
0 1 0
0 1 0 1
```

---

## 3. Conteo descendente por fila

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir un patrón donde cada fila comience en el número de la fila y termine en 1.

Ejemplo para `n = 5`:

```text
1
2 1
3 2 1
4 3 2 1
5 4 3 2 1
```

---

## 4. Repetición de una letra

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir un patrón usando la letra `A`, repitiéndola según el número de elementos que corresponda a cada fila.

Ejemplo para `n = 4`:

```text
A
A A
A A A
A A A A
```

---

## 5. Triángulo con números pares

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir un triángulo en el que cada fila muestre los primeros números pares, empezando en 2.

Ejemplo para `n = 4`:

```text
2
2 4
2 4 6
2 4 6 8
```

---

## 6. Triángulo con números impares

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir un triángulo en el que cada fila muestre los primeros números impares, comenzando en 1.

Ejemplo para `n = 4`:

```text
1
1 3
1 3 5
1 3 5 7
```

---

## 7. Cuadrado con el número de la fila

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir un cuadrado de tamaño `n x n`, donde en cada fila aparezca siempre el mismo número, correspondiente al número de esa fila.

Ejemplo para `n = 4`:

```text
1 1 1 1
2 2 2 2
3 3 3 3
4 4 4 4
```

---

## 8. Cuadrado con el número de la columna

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir un cuadrado de tamaño `n x n`, donde en cada fila aparezcan los números desde 1 hasta `n`.

Ejemplo para `n = 4`:

```text
1 2 3 4
1 2 3 4
1 2 3 4
1 2 3 4
```

---

## 9. Suma acumulada en cada fila

Escriba un programa que solicite un número entero positivo `n`.
Para cada fila, el programa debe mostrar los números desde 1 hasta el número de la fila y, al final, indicar la suma total de los valores impresos en esa fila.

Ejemplo para `n = 4`:

```text
1 -> suma: 1
1 2 -> suma: 3
1 2 3 -> suma: 6
1 2 3 4 -> suma: 10
```

---

## 10. Producto acumulado en cada fila

Escriba un programa que solicite un número entero positivo `n`.
Para cada fila, el programa debe mostrar los números desde 1 hasta el número de la fila y, al final, indicar el producto total de los valores impresos en esa fila.

Ejemplo para `n = 4`:

```text
1 -> producto: 1
1 2 -> producto: 2
1 2 3 -> producto: 6
1 2 3 4 -> producto: 24
```

---

## 11. Tabla de restas

Escriba un programa que solicite un número entero positivo `n`.
El programa debe generar una tabla de `n x n` donde cada posición contenga el resultado de restar el número de la columna al número de la fila.

Ejemplo para `n = 4`:

```text
0 -1 -2 -3
1 0 -1 -2
2 1 0 -1
3 2 1 0
```

---

## 12. Tabla de divisibilidad

Escriba un programa que solicite un número entero positivo `n`.
Para cada par de números entre 1 y `n`, el programa debe mostrar `SI` si el número de la fila es divisible por el número de la columna, y `NO` en caso contrario.

Ejemplo para `n = 4`:

```text
SI SI SI SI
SI SI NO NO
SI NO SI NO
SI SI NO SI
```

---

## 13. Conteo de números pares por fila

Escriba un programa que solicite dos números enteros positivos: `n` y `m`.
Para cada fila desde 1 hasta `n`, el programa debe revisar los números desde 1 hasta `m` y contar cuántos de ellos son pares.
Al final de cada fila, debe mostrar el total encontrado.

---

## 14. Conteo de múltiplos de 3

Escriba un programa que solicite un número entero positivo `n`.
Para cada fila desde 1 hasta `n`, el programa debe analizar los números desde 1 hasta el valor de la fila y contar cuántos de ellos son múltiplos de 3.

Ejemplo para `n = 6`:

```text
Fila 1: 0
Fila 2: 0
Fila 3: 1
Fila 4: 1
Fila 5: 1
Fila 6: 2
```

---

## 15. Triángulo alineado a la derecha

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir un triángulo de asteriscos alineado a la derecha.

Ejemplo para `n = 4`:

```text
   *
  **
 ***
****
```

---

## 16. Pirámide simple de asteriscos

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir una pirámide de altura `n`, formada con asteriscos.

Ejemplo para `n = 4`:

```text
   *
  ***
 *****
*******
```

---

## 17. Pirámide invertida

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir una pirámide invertida de altura `n`, usando asteriscos.

Ejemplo para `n = 4`:

```text
*******
 *****
  ***
   *
```

---

## 18. Números consecutivos por filas

Escriba un programa que solicite un número entero positivo `n`.
El programa debe imprimir números consecutivos comenzando en 1, organizados por filas, de manera que la primera fila tenga un número, la segunda tenga dos, la tercera tenga tres, y así sucesivamente.

Ejemplo para `n = 4`:

```text
1
2 3
4 5 6
7 8 9 10
```

---

## 19. Comparación entre pares de números

Escriba un programa que solicite un número entero positivo `n`.
El programa debe recorrer todos los pares `(i, j)` entre 1 y `n` y mostrar:

* `IGUALES`, si ambos valores son iguales
* `I_MAYOR`, si el valor de `i` es mayor que el de `j`
* `J_MAYOR`, si el valor de `j` es mayor que el de `i`

---

## 20. Divisores de cada número

Escriba un programa que solicite un número entero positivo `n`.
Para cada número desde 1 hasta `n`, el programa debe mostrar todos sus divisores.

Ejemplo para `n = 5`:

```text
Divisores de 1: 1
Divisores de 2: 1 2
Divisores de 3: 1 3
Divisores de 4: 1 2 4
Divisores de 5: 1 5
```

---



