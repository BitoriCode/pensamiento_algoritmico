# Banco de Ejercicios: Listas y Tuplas en Python

## Instrucciones Generales

- Todos los ejercicios **requieren funciones**. Define y llama las funciones desde el programa principal.
- **Restricción global:** No usar `sum()`, `min()`, `max()`,  `sort()`, `reverse()`, `sorted()` ni ninguna función de Python que resuelva directamente el problema. Cada ejercicio indica restricciones específicas adicionales.
- Trabaja únicamente con listas y tuplas (no uses diccionarios, sets, clases ni módulos externos).
- Los datos de ejemplo son el punto de partida; las funciones deben funcionar con cualquier lista de igual estructura.

---

## SECCIÓN A: LISTAS

### Grupo 1 – Análisis y Estadísticas

---

## Ejercicio 1: Notas del Semestre

En una universidad colombiana se registraron las notas finales de un grupo de estudiantes en la asignatura de Programación. La escala va de 0.0 a 5.0 y la nota mínima para aprobar es 3.0. Con esta información:

```python
notas = [4.5, 2.8, 3.9, 1.5, 4.0, 3.2, 2.5, 4.8, 3.0, 3.7]
```

**Restricciones:** No usar `sum()`, `min()`, `max()`,  `sorted()`.

**Funciones requeridas:**
- `calcular_promedio(notas)`: retorna el promedio de la lista.
- `contar_aprobados(notas)`: retorna cuántos estudiantes tienen nota ≥ 3.0.
- `mejor_nota(notas)`: retorna la nota más alta de la lista.
- `peor_nota(notas)`: retorna la nota más baja de la lista.
- `clasificar(notas)`: retorna tres listas: `sobresaliente` (≥ 4.5), `aprobado` (3.0–4.49) y `reprobado` (< 3.0).

---

## Ejercicio 2: Asistencia Estudiantil

Un colegio en Bogotá registra la asistencia diaria de un estudiante durante 20 días lectivos. El valor `1` indica que asistió y `0` que faltó. Con estos datos:

```python
asistencias = [1, 1, 0, 1, 1, 1, 0, 0, 1, 1, 1, 1, 0, 1, 0, 1, 1, 1, 0, 1]
```

**Restricciones:** No usar `sum()`,  `count()`.

**Funciones requeridas:**
- `porcentaje_asistencia(asistencias)`: retorna el porcentaje de días que el estudiante asistió.
- `total_faltas(asistencias)`: retorna el número total de días que faltó.
- `racha_faltas(asistencias)`: retorna la racha más larga de faltas consecutivas.
- `racha_asistencia(asistencias)`: retorna la racha más larga de asistencias consecutivas.
- `en_riesgo(asistencias, umbral)`: retorna `True` si el porcentaje de faltas supera el umbral indicado.

---

## Ejercicio 3: Precios de Mercado en Medellín

En una plaza de mercado de Medellín se registraron los precios (en pesos colombianos) de 12 productos básicos de la canasta familiar. Con estos datos se quiere analizar la variación de precios respecto al promedio:

```python
productos = ["arroz", "aceite", "leche", "huevos", "pan", "pollo",
             "papa", "cebolla", "tomate", "azúcar", "sal", "café"]
precios   = [3200, 8500, 2700, 520, 1800, 12000, 1500, 2200, 1900, 2800, 1200, 4500]
```

**Restricciones:** No usar `sum()`, `min()`, `max()`,  `sorted()`.

**Funciones requeridas:**
- `precio_promedio(precios)`: retorna el precio promedio de los productos.
- `productos_bajo_promedio(productos, precios)`: retorna una lista con los nombres de los productos cuyo precio está por debajo del promedio.
- `producto_mas_caro(productos, precios)`: retorna el nombre del producto con el precio más alto.
- `aplicar_descuento(precios, porcentaje)`: retorna una nueva lista con los precios reducidos en el porcentaje indicado.
- `diferencia_con_promedio(precios)`: retorna una lista donde cada elemento es la diferencia entre ese precio y el promedio (puede ser negativa).

---

## Ejercicio 4: Precipitaciones Mensuales en el Valle del Cauca

El IDEAM registró las precipitaciones mensuales (en milímetros) en una estación del Valle del Cauca durante un año. Se considera un mes "seco" si la precipitación es menor a 50 mm. Con estos datos:

```python
meses   = ["Ene", "Feb", "Mar", "Abr", "May", "Jun",
           "Jul", "Ago", "Sep", "Oct", "Nov", "Dic"]
lluvias = [30, 45, 80, 120, 150, 60, 40, 35, 90, 130, 70, 25]
```

**Restricciones:** No usar `sum()`, `min()`, `max()`,  `sorted()`.

**Funciones requeridas:**
- `precipitacion_total(lluvias)`: retorna la precipitación total anual.
- `precipitacion_promedio(lluvias)`: retorna el promedio mensual.
- `meses_secos(meses, lluvias)`: retorna una lista con los nombres de los meses cuya precipitación fue menor a 50 mm.
- `mes_mas_lluvioso(meses, lluvias)`: retorna el nombre del mes con mayor precipitación.
- `racha_seca_maxima(lluvias)`: retorna la racha más larga de meses consecutivos con precipitación menor a 50 mm.

---

## Ejercicio 5: Velocidades en la Autopista Bogotá-Villavicencio

En un punto de control de la autopista Bogotá-Villavicencio se registraron las velocidades (en km/h) de 15 vehículos. El límite de velocidad en esa vía es de 80 km/h:

```python
velocidades = [75, 82, 60, 95, 78, 110, 70, 85, 65, 92, 80, 74, 100, 68, 88]
```

**Restricciones:** No usar `sum()`, `min()`, `max()`,  `sorted()`, `count()`.

**Funciones requeridas:**
- `velocidad_promedio(velocidades)`: retorna la velocidad promedio de todos los vehículos.
- `contar_excesos(velocidades, limite)`: retorna cuántos vehículos superaron el límite de velocidad.
- `velocidad_maxima_con_posicion(velocidades)`: retorna una tupla `(velocidad, posicion)` con la velocidad máxima y su índice en la lista.
- `vehiculos_seguros(velocidades, limite)`: retorna una lista con las velocidades de los vehículos que respetaron el límite.
- `clasificar_infraccion(velocidades, limite)`: retorna tres conteos: infracciones `leve` (1–20 km/h sobre el límite), `grave` (21–40 km/h) y `muy_grave` (más de 40 km/h).

---

### Grupo 2 – Manipulación Avanzada

---

## Ejercicio 6: Rotación de Lista por K Posiciones

En un sistema de turnos para una droguería en Cali, el orden de atención se representa como una lista. Cuando se "rota" la lista, el primer turno pasa al final (rotación izquierda) o el último turno pasa al inicio (rotación derecha):

```python
turnos = [101, 102, 103, 104, 105, 106, 107, 108]
k = 3
```

**Restricciones:** No usar slicing (`lista[a:b]`), no usar `deque`, no modificar la lista original.

**Funciones requeridas:**
- `rotar_izquierda(turnos, k)`: retorna una nueva lista rotada k posiciones hacia la izquierda. *(ej. k=2: [103, 104, 105, 106, 107, 108, 101, 102])*
- `rotar_derecha(turnos, k)`: retorna una nueva lista rotada k posiciones hacia la derecha. *(ej. k=2: [107, 108, 101, 102, 103, 104, 105, 106])*
- `normalizar_k(k, n)`: retorna el valor equivalente de k dentro del rango válido (0 a n-1), por si k es mayor que la longitud de la lista. *(Implementar sin el operador `%`.)*

---

## Ejercicio 7: Verificar Palíndromo

En un juego de palabras para estudiantes de primaria en Barranquilla, se quiere verificar si una lista de caracteres o números es palíndromo (se lee igual de izquierda a derecha que de derecha a izquierda):

```python
secuencia_1 = [1, 2, 3, 2, 1]
secuencia_2 = ['r', 'a', 'd', 'a', 'r']
secuencia_3 = [1, 2, 3, 4, 5]
```

**Restricciones:** No usar `reverse()`, `reversed()`, ni slicing inverso (`lista[::-1]`).

**Funciones requeridas:**
- `es_palindromo(secuencia)`: retorna `True` si la secuencia es palíndromo, `False` si no.
- `elemento_central(secuencia)`: si la longitud es impar retorna el elemento central; si es par retorna los dos elementos centrales como lista.
- `primera_diferencia(secuencia)`: si no es palíndromo, retorna la posición (desde el extremo izquierdo) del primer par de elementos que difieren al comparar desde afuera hacia el centro; si sí es palíndromo retorna `-1`.

---

## Ejercicio 8: Entrelazar Dos Listas

En la programación de un evento cultural en Medellín, se tienen dos listas separadas: artistas locales e invitados. Se quiere crear el orden final intercalando un artista local, luego uno invitado, y así sucesivamente:

```python
locales   = ["La Banda Sinfónica", "Coro Municipal", "Grupo Folclórico", "Dúo de Jazz"]
invitados = ["Carlos Vives", "Fonseca", "Maluma"]
```

**Restricciones:** No usar `zip()`, `extend()`, ni concatenación con `+`.

**Funciones requeridas:**
- `entrelazar(lista_a, lista_b)`: retorna una nueva lista intercalando elemento a elemento. Los elementos sobrantes de la lista más larga se agregan al final.
- `entrelazar_n(listas)`: recibe una lista de listas y las entrelaza todas posición por posición. *(ej. [[1,4],[2,5],[3,6]] → [1,2,3,4,5,6])*
- `separar_posiciones(lista)`: dada una lista entrelazada, retorna dos listas: una con los elementos de posiciones pares y otra con los de posiciones impares.

---

## Ejercicio 9: Comprimir Duplicados Consecutivos

En un sistema de monitoreo de temperatura de una bodega en Bucaramanga, el sensor registra la temperatura cada hora pero a veces repite el mismo valor seguidas veces. Se quiere "comprimir" la secuencia eliminando los duplicados **consecutivos** (no todos los duplicados, solo los que aparecen seguidos):

```python
temperaturas = [18, 18, 18, 19, 19, 20, 20, 20, 20, 19, 18, 18, 17, 17, 17]
```

**Restricciones:** No usar `set()`. Solo eliminar duplicados consecutivos, no todos los duplicados.

**Funciones requeridas:**
- `comprimir(lista)`: retorna una nueva lista eliminando los duplicados consecutivos. *(ej. → [18, 19, 20, 19, 18, 17])*
- `comprimir_con_conteo(lista)`: retorna una lista de pares `[elemento, cantidad]` indicando cuántas veces aparece cada grupo consecutivo. *(ej. → [[18,3],[19,2],[20,4],[19,1],[18,2],[17,3]])*
- `descomprimir(lista_comprimida)`: dada la salida de `comprimir_con_conteo`, reconstruye la lista original.
- `grupo_mas_largo(lista)`: retorna el elemento que tiene la racha consecutiva más larga y el tamaño de esa racha, como tupla `(elemento, longitud)`.

---

## Ejercicio 10: Ventana Deslizante (Promedio Móvil)

El Banco de la República de Colombia publica la TRM (precio del dólar) diariamente. Un analista financiero quiere suavizar la serie calculando el promedio móvil de ventana de tamaño K (promedio de los últimos K días) para cada posición posible:

```python
trm_diaria = [3820, 3845, 3830, 3870, 3900, 3860, 3850, 3880, 3910, 3925, 3890, 3870]
k = 3
```

**Restricciones:** No usar `sum()`, no usar slicing, no usar librerías externas.

**Funciones requeridas:**
- `promedio_movil(lista, k)`: retorna una lista con el promedio móvil de tamaño k. El resultado tiene `n - k + 1` elementos.
- `tendencia(lista, k)`: compara el primer y último promedio móvil y retorna `"subida"`, `"bajada"` o `"estable"`.
- `posicion_max_promedio(lista, k)`: retorna el índice inicial de la ventana donde el promedio móvil fue el más alto.
- `posicion_min_promedio(lista, k)`: retorna el índice inicial de la ventana donde el promedio móvil fue el más bajo.

---

## Ejercicio 11: Operaciones de Conjuntos con Listas

Dos sucursales de una cadena de supermercados en Bogotá llevan el registro de los códigos de productos que vendieron en la semana. Se quiere comparar los catálogos sin usar estructuras especiales:

```python
vendidos_norte = [101, 102, 103, 104, 105, 106, 107]
vendidos_sur   = [103, 105, 107, 108, 109, 110, 111]
```

**Restricciones:** No usar `set()`, no usar diccionarios. Usar solo listas y bucles.

**Funciones requeridas:**
- `union(lista_a, lista_b)`: retorna una lista con todos los elementos que aparecen en alguna de las dos listas (sin repetidos).
- `interseccion(lista_a, lista_b)`: retorna una lista con los elementos que aparecen en **ambas** listas.
- `diferencia(lista_a, lista_b)`: retorna los elementos que están en `lista_a` pero **no** en `lista_b`.
- `diferencia_simetrica(lista_a, lista_b)`: retorna los elementos que están en una lista pero no en ambas.
- `esta_contenida(lista_a, lista_b)`: retorna `True` si todos los elementos de `lista_a` están en `lista_b`.

---

## Ejercicio 12: Fusionar Dos Listas Ordenadas

Una empresa de mensajería en Bogotá maneja dos rutas cuyos pedidos están ordenados por número. Se necesita combinar ambas rutas en una sola lista ordenada sin volver a ordenar desde cero:

```python
ruta_norte = [1003, 1007, 1012, 1018, 1025]
ruta_sur   = [1001, 1005, 1009, 1015, 1020, 1030]
```

**Restricciones:** No usar `sort()`, `sorted()`. No concatenar y luego ordenar. El algoritmo debe aprovechar que las listas ya están ordenadas (algoritmo merge).

**Funciones requeridas:**
- `fusionar_ordenado(lista_a, lista_b)`: retorna una nueva lista con todos los elementos de ambas listas en orden ascendente.
- `esta_ordenada(lista)`: retorna `True` si la lista está ordenada de menor a mayor.
- `fusionar_descendente(lista_a, lista_b)`: igual que `fusionar_ordenado` pero el resultado es de mayor a menor. *(Asume que las entradas también están en orden descendente.)*

---

## Ejercicio 13: Frecuencia de Elementos

En una encuesta aplicada a estudiantes universitarios de Colombia se les preguntó cuál era su carrera de preferencia. Las respuestas se almacenaron en una lista. Se quiere saber cuántas veces aparece cada carrera sin usar diccionarios:

```python
respuestas = ["Sistemas", "Medicina", "Derecho", "Sistemas", "Ingeniería",
              "Medicina", "Sistemas", "Derecho", "Contaduría", "Ingeniería",
              "Medicina", "Sistemas", "Ingeniería", "Derecho", "Contaduría"]
```

**Restricciones:** No usar `count()`, `set()`, ni diccionarios. Usar listas paralelas (una para elementos únicos, otra para sus conteos).

**Funciones requeridas:**
- `obtener_unicos(lista)`: retorna una lista con los elementos únicos en el orden en que aparecieron por primera vez.
- `contar_frecuencias(lista)`: retorna dos listas paralelas: `elementos` y `conteos`, donde `conteos[i]` es la cantidad de veces que aparece `elementos[i]`.
- `elemento_mas_frecuente(lista)`: retorna el elemento que más veces aparece.
- `elemento_menos_frecuente(lista)`: retorna el elemento que menos veces aparece.
- `frecuencia_relativa(lista)`: retorna una lista con el porcentaje de aparición de cada elemento único (en el mismo orden que `obtener_unicos`).

---

## Ejercicio 14: K-ésimo Mayor Elemento

En un torneo de robótica estudiantil en Pereira, los equipos acumularon puntos a lo largo de la competencia. Se quiere saber el k-ésimo mayor puntaje sin ordenar toda la lista:

```python
puntajes = [450, 720, 390, 810, 680, 530, 760, 420, 610, 840]
k = 3  # 3er mayor puntaje
```

**Restricciones:** No usar `sort()`, `sorted()`, `max()`, `min()`.

**Funciones requeridas:**
- `kesimo_mayor(lista, k)`: retorna el k-ésimo mayor valor de la lista. *(k=1 retorna el mayor, k=2 el segundo mayor, etc.)*
- `kesimo_menor(lista, k)`: retorna el k-ésimo menor valor de la lista.
- `top_k(lista, k)`: retorna una lista con los k valores más altos, en orden descendente.
- `posicion_del_kesimo(lista, k)`: retorna el índice del k-ésimo mayor elemento en la lista original.

---

### Grupo 3 – Transformaciones y Búsqueda

---

## Ejercicio 15: Búsqueda Binaria

En una biblioteca escolar de Manizales, el catálogo de libros está ordenado por número de ISBN. Se necesita implementar un sistema de búsqueda eficiente que aproveche este orden:

```python
isbn_catalogo = [1001, 1045, 1089, 1123, 1187, 1234, 1289, 1345, 1400, 1456, 1500, 1567]
isbn_buscar   = 1289
```

**Restricciones:** No recorrer la lista de forma lineal (no usar un `for` simple que revise uno por uno). Implementar búsqueda binaria.

**Funciones requeridas:**
- `busqueda_binaria(lista, objetivo)`: retorna el índice del elemento si existe, o `-1` si no está en la lista.
- `esta_en_catalogo(lista, objetivo)`: retorna `True` o `False` según si el ISBN existe.
- `rango_busqueda(lista, menor, mayor)`: retorna una lista con todos los ISBN del catálogo que se encuentran entre `menor` y `mayor` (inclusive), usando búsqueda binaria para encontrar el rango.

---

## Ejercicio 16: Codificación y Decodificación RLE

En un sistema de compresión de datos de una empresa de telecomunicaciones en Bogotá se usa el algoritmo Run-Length Encoding (RLE). Una señal de ejemplo es una lista de niveles:

```python
senal = [0, 0, 0, 1, 1, 0, 0, 0, 0, 1, 1, 1, 0, 0, 1]
```

**Restricciones:** No usar librerías de compresión externas.

**Funciones requeridas:**
- `codificar_rle(lista)`: retorna una lista de pares `[cantidad, valor]` con la codificación RLE. *(ej. → [[3,0],[2,1],[4,0],[3,1],[2,0],[1,1]])*
- `decodificar_rle(lista_codificada)`: recibe la lista de pares y reconstruye la lista original.
- `longitud_codificada(lista_codificada)`: retorna el número total de elementos que representa la lista codificada (sin decodificar).
- `es_eficiente(lista_original, lista_codificada)`: retorna `True` si la codificación RLE tiene menos elementos que la lista original.

---

## Ejercicio 17: Aplanar Lista de Listas

En un sistema escolar de Cartagena, los grupos del colegio están organizados como una lista de listas, donde cada sublista contiene los números de identificación de los estudiantes de ese grupo. Se necesita obtener la lista completa de todos los estudiantes:

```python
grupos = [
    [1001, 1002, 1003, 1004],
    [1005, 1006, 1007],
    [1008, 1009, 1010, 1011, 1012],
    [1013, 1014]
]
```

**Restricciones:** No usar `extend()`, no usar librerías externas, no usar comprensiones de lista.

**Funciones requeridas:**
- `aplanar(lista_de_listas)`: retorna una lista con todos los elementos de todas las sublistas en orden.
- `contar_total(lista_de_listas)`: retorna el número total de elementos sin aplanar primero la lista.
- `grupo_mas_grande(lista_de_listas)`: retorna el índice de la sublista con más elementos.
- `grupo_mas_pequeno(lista_de_listas)`: retorna el índice de la sublista con menos elementos.
- `esta_en_algun_grupo(lista_de_listas, elemento)`: retorna `True` y el índice del grupo donde se encontró, o `False` y `-1` si no existe.

---

## Ejercicio 18: Partición de Lista (Pivote)

El algoritmo Quicksort usa una operación fundamental llamada "partición": dado un valor pivote, separar la lista de modo que todos los elementos menores queden a la izquierda y los mayores o iguales a la derecha. En un sistema de inventario de una ferretería en Cúcuta:

```python
inventario_codigos = [34, 12, 67, 45, 23, 78, 56, 9, 42, 31, 60]
pivote = 40
```

**Restricciones:** No usar `sort()`, `sorted()`. No modificar la lista original.

**Funciones requeridas:**
- `particionar(lista, pivote)`: retorna dos listas: una con elementos `< pivote` y otra con elementos `>= pivote`.
- `particionar_tres(lista, pivote)`: retorna tres listas: `menores` (< pivote), `iguales` (== pivote) y `mayores` (> pivote).
- `pivote_optimo(lista)`: retorna el elemento de la lista que, al usarse como pivote, produce las dos particiones más equilibradas en tamaño.

---

## Ejercicio 19: Representación de Polinomios

En la clase de álgebra de un colegio técnico en Ibagué, los estudiantes representan polinomios como listas de coeficientes donde el índice indica la potencia. Por ejemplo, `[3, 0, -1, 2]` representa $3 + 0x - x^2 + 2x^3$. Los polinomios no deben tener ceros al final (términos de mayor grado):

```python
polinomio_a = [3, 0, -1, 2, 0, 0]
polinomio_b = [1, 2, 3]
```

**Restricciones:** No usar librerías matemáticas externas. Implementar la potencia con bucle (no usar `**`).

**Funciones requeridas:**
- `limpiar_ceros(polinomio)`: retorna el polinomio eliminando los ceros del final.
- `grado(polinomio)`: retorna el grado del polinomio (índice del último coeficiente no cero).
- `sumar_polinomios(p1, p2)`: retorna la lista que representa la suma de dos polinomios (maneja listas de diferente longitud).
- `evaluar(polinomio, x)`: retorna el valor del polinomio para un `x` dado. *(Implementar la potencia con un bucle, no usar `**`.)*
- `escalar(polinomio, k)`: retorna un nuevo polinomio donde cada coeficiente está multiplicado por `k`.

---

## Ejercicio 20: Acceso Circular a Lista

En una rueda de la fortuna de una feria en Santa Marta, los premios están dispuestos en posiciones fijas. La rueda gira y el acceso al siguiente premio es siempre circular (después del último vuelve al primero):

```python
premios = ["Peluche", "Chocolate", "Libre", "Globo", "Vale 5000", "Nada", "Sorpresa", "Nada"]
```

**Restricciones:** No usar el operador `%` directamente; implementar la lógica circular con un bucle o condicional.

**Funciones requeridas:**
- `acceso_circular(lista, indice)`: retorna el elemento en la posición `indice`, incluso si `indice >= longitud` o es negativo, usando lógica circular.
- `siguiente_n(lista, inicio, n)`: retorna una lista con los próximos `n` elementos a partir de la posición `inicio`, de forma circular.
- `contar_vueltas(lista, inicio, pasos)`: dado un punto de inicio y un número de pasos, retorna cuántas vueltas completas da la rueda.
- `posicion_de(lista, elemento)`: retorna la primera posición del elemento buscado, o `-1` si no existe.

---

## Ejercicio 21: Subarray de Suma Máxima

Una empresa de inversión en Bogotá registra la ganancia o pérdida diaria (en millones de pesos) de un portafolio. Se quiere encontrar el período continuo de días con la mayor ganancia acumulada:

```python
ganancias_diarias = [-2, 1, -3, 4, -1, 2, 1, -5, 4, 3, -2, 1]
```

**Restricciones:** No usar `sum()`, `max()`. No generar todos los subarrays posibles; implementar el algoritmo de Kadane o similar.

**Funciones requeridas:**
- `suma_maxima_subarray(lista)`: retorna el valor de la suma máxima de cualquier sublista contigua.
- `subarray_de_suma_maxima(lista)`: retorna la sublista (como lista) que produce esa suma máxima.
- `rango_suma_maxima(lista)`: retorna el índice de inicio y el índice de fin del subarray de suma máxima, como tupla `(inicio, fin)`.
- `suma_minima_subarray(lista)`: retorna el valor de la suma mínima de cualquier sublista contigua (la mayor pérdida acumulada).

---

## Ejercicio 22: Transponer Lista de Listas

En el área de estadística de una empresa en Cali, se tiene una tabla de datos donde cada fila es una semana y cada columna es un día de la semana. A veces es necesario "voltear" la tabla para que cada fila sea un día y cada columna una semana:

```python
semanas = [
    [100, 120, 95,  110, 130],  # Semana 1
    [105, 115, 90,  125, 140],  # Semana 2
    [110, 118, 100, 130, 135],  # Semana 3
    [95,  122, 88,  120, 128]   # Semana 4
]
dias = ["Lunes", "Martes", "Miércoles", "Jueves", "Viernes"]
```

**Restricciones:** No usar `zip()`, no usar librerías externas, no usar comprensiones de lista.

**Funciones requeridas:**
- `transponer(matriz)`: retorna la lista de listas transpuesta (las filas se convierten en columnas y viceversa).
- `suma_por_columna(matriz)`: retorna una lista con la suma de cada columna original.
- `promedio_por_columna(matriz)`: retorna una lista con el promedio de cada columna original.
- `columna_mayor_total(matriz)`: retorna el índice de la columna con la mayor suma total.

---

## SECCIÓN B: TUPLAS

---

## Ejercicio 23: Empleados y Salarios

Una empresa de logística con sucursales en varias ciudades colombianas maneja el registro de sus empleados como una lista de tuplas. Cada tupla contiene: nombre, cargo, salario mensual (en miles de pesos) y ciudad de trabajo:

```python
empleados = [
    ("Andrés Torres",   "Conductor",    2800, "Medellín"),
    ("Laura Gómez",     "Supervisora",  4500, "Bogotá"),
    ("Carlos Ríos",     "Almacenista",  2200, "Cali"),
    ("María Pérez",     "Conductora",   2800, "Medellín"),
    ("Jhon Martínez",   "Coordinador",  3800, "Bogotá"),
    ("Sandra López",    "Almacenista",  2200, "Barranquilla"),
    ("Felipe Suárez",   "Supervisor",   4200, "Cali"),
    ("Ana Rodríguez",   "Coordinadora", 3900, "Bogotá"),
    ("Diego Castillo",  "Conductor",    2800, "Barranquilla"),
]
```

**Restricciones:** No usar `sum()`, `min()`, `max()`,  `sorted()`, diccionarios.

**Funciones requeridas:**
- `salario_promedio(empleados)`: retorna el salario promedio de todos los empleados.
- `empleados_por_ciudad(empleados, ciudad)`: retorna una lista de tuplas con los empleados que trabajan en esa ciudad.
- `salario_promedio_ciudad(empleados, ciudad)`: retorna el salario promedio de los empleados de una ciudad específica.
- `empleado_mejor_pagado(empleados)`: retorna la tupla completa del empleado con el salario más alto.
- `cargos_unicos(empleados)`: retorna una lista con los nombres de cargos únicos que existen en la empresa.

---

## Ejercicio 24: Coordenadas Geográficas de Colombia

El Instituto Geográfico Agustín Codazzi maneja las coordenadas de ciudades colombianas como una lista de tuplas `(ciudad, latitud, longitud)`. La latitud positiva indica norte del Ecuador y negativa indica sur:

```python
ciudades_geo = [
    ("Bogotá",        4.7110,  -74.0721),
    ("Medellín",      6.2442,  -75.5812),
    ("Cali",          3.4516,  -76.5320),
    ("Cartagena",    10.3910,  -75.4794),
    ("Barranquilla", 10.9639,  -74.7964),
    ("Bucaramanga",   7.1254,  -73.1198),
    ("Manizales",     5.0703,  -75.5138),
    ("Pasto",         1.2136,  -77.2811),
    ("Leticia",      -4.2153,  -69.9406),
]
```

**Restricciones:** No usar `math.sqrt()` ni librerías matemáticas. Aproximar la distancia al Ecuador con: 1° de latitud ≈ 111 km.

**Funciones requeridas:**
- `distancia_al_ecuador(ciudad_tupla)`: retorna la distancia aproximada al Ecuador en km de una ciudad dada como tupla.
- `ciudad_mas_lejana_ecuador(ciudades)`: retorna el nombre de la ciudad más lejana del Ecuador.
- `ciudades_norte(ciudades)`: retorna una lista de nombres de ciudades que están al norte del Ecuador (latitud > 0).
- `ciudad_mas_occidental(ciudades)`: retorna el nombre de la ciudad con la longitud más negativa (más al occidente).
- `distancia_entre(ciudad_a, ciudad_b)`: retorna la distancia aproximada en km entre dos ciudades usando la fórmula de distancia euclidiana sobre (lat, lng).

---

## Ejercicio 25: Inventario de Tienda de Tecnología

Una tienda de tecnología en Bogotá maneja su inventario como lista de tuplas. Cada tupla contiene: código del producto, nombre, precio unitario (pesos) y cantidad disponible:

```python
inventario = [
    ("T001", "Audífonos Bluetooth",   89000,  25),
    ("T002", "Cable USB-C 1m",         8500,  80),
    ("T003", "Teclado inalámbrico",  145000,   0),
    ("T004", "Mouse óptico",          35000,  40),
    ("T005", "Cargador rápido 20W",   55000,  15),
    ("T006", "Funda para portátil",   42000,   0),
    ("T007", "Webcam HD",            180000,   8),
    ("T008", "Hub USB 4 puertos",     65000,  30),
    ("T009", "Protector de pantalla", 12000,  60),
]
```

**Restricciones:** No usar `sum()`, `min()`, `max()`,  `sorted()`.

**Funciones requeridas:**
- `valor_total_inventario(inventario)`: retorna el valor total del inventario (suma de precio × cantidad de cada producto).
- `productos_agotados(inventario)`: retorna una lista de tuplas con los productos cuya cantidad es 0.
- `producto_mas_caro(inventario)`: retorna la tupla completa del producto con mayor precio unitario.
- `reabastecer(inventario, codigo, cantidad)`: retorna una **nueva lista** de tuplas donde el producto con ese código tiene la cantidad actualizada.
- `aplicar_descuento(inventario, porcentaje)`: retorna una nueva lista de tuplas donde todos los precios están reducidos en el porcentaje dado.

---

## Ejercicio 26: Clasificación en Olimpiadas de Matemáticas

En las Olimpiadas de Matemáticas del Valle del Cauca participaron estudiantes de varios colegios. Los resultados se almacenaron como lista de tuplas `(nombre, colegio, puntaje)`:

```python
resultados = [
    ("Valentina Muñoz",  "Colegio San José",     95),
    ("Sebastián Castro", "IEM La Merced",         87),
    ("Isabela Vargas",   "Colegio San José",     100),
    ("Martín Ospina",    "Colegio Nuevo Mundo",   78),
    ("Daniela Herrera",  "IEM La Merced",         92),
    ("Tomás Reyes",      "Colegio Nuevo Mundo",   65),
    ("Sofía Mejía",      "Colegio San José",      88),
    ("Julián Mora",      "IEM La Merced",         71),
    ("Alejandra Ríos",   "Colegio Nuevo Mundo",   83),
]
```

**Restricciones:** No usar `sorted()`, `sort()`, `min()`, `max()`, .

**Funciones requeridas:**
- `ganador(resultados)`: retorna la tupla completa del estudiante con el puntaje más alto.
- `top_tres(resultados)`: retorna una lista con las 3 tuplas de los puntajes más altos, en orden descendente (sin `sorted`).
- `promedio_colegio(resultados, colegio)`: retorna el puntaje promedio de los estudiantes de un colegio dado.
- `mejor_colegio(resultados)`: retorna el nombre del colegio con el mayor promedio de puntajes.
- `clasificados(resultados, umbral)`: retorna una lista con los estudiantes que superan el puntaje umbral, ordenada de mayor a menor puntaje (sin `sorted`).

---

## Ejercicio 27: Historial de Ventas

Una empresa de ventas directas en Barranquilla registra cada transacción como una tupla `(número_de_día_del_año, monto_en_pesos, nombre_vendedor)`:

```python
ventas = [
    (  1, 350000, "Camilo"),
    (  1, 120000, "Diana"),
    ( 15, 480000, "Camilo"),
    ( 32, 290000, "Diana"),
    ( 45, 650000, "Ricardo"),
    ( 60, 410000, "Camilo"),
    ( 75, 380000, "Diana"),
    ( 90, 720000, "Ricardo"),
    (100, 290000, "Camilo"),
    (120, 550000, "Diana"),
    (150, 810000, "Ricardo"),
    (180, 430000, "Camilo"),
]
```

**Restricciones:** No usar `sum()`, `min()`, `max()`, `sorted()`, diccionarios.

**Funciones requeridas:**
- `total_vendedor(ventas, vendedor)`: retorna el monto total vendido por un vendedor durante el año.
- `vendedor_del_anio(ventas)`: retorna el nombre del vendedor con el mayor monto total acumulado.
- `ventas_en_rango(ventas, dia_inicio, dia_fin)`: retorna todas las tuplas cuyo día esté en el rango [dia_inicio, dia_fin].
- `mes_mas_activo(ventas)`: determina en qué mes (1-12) se generó la mayor cantidad de transacciones. *(Asumir meses de 31 días: mes = (día - 1) // 31 + 1.)*
- `promedio_por_venta(ventas)`: retorna el monto promedio por transacción de todo el historial.

---

## Ejercicio 28: Resultados de Atletismo

En los Juegos Nacionales de Colombia se registraron los tiempos de los atletas en la prueba de 400 metros planos. Cada resultado es una tupla `(nombre_atleta, departamento, tiempo_en_segundos)`:

```python
atletas = [
    ("Carlos Perea",   "Valle",       46.85),
    ("Juan Soto",      "Antioquia",   47.12),
    ("Pedro Lemos",    "Bogotá D.C.", 45.98),
    ("Luis Hoyos",     "Valle",       47.50),
    ("Andrés Moya",    "Bolívar",     48.20),
    ("Rodrigo Paz",    "Antioquia",   46.75),
    ("Gabriel Nieto",  "Bogotá D.C.", 46.10),
    ("Héctor Vélez",   "Bolívar",     47.90),
    ("Felipe Arcos",   "Valle",       46.30),
]
```

**Restricciones:** No usar `sorted()`, `sort()`, `min()`, `max()`, .

**Funciones requeridas:**
- `ganador_prueba(atletas)`: retorna la tupla del atleta con el **menor** tiempo.
- `podio(atletas)`: retorna una lista con las 3 tuplas de los atletas más rápidos, en orden de llegada (sin `sorted`).
- `mejor_por_departamento(atletas)`: retorna una lista de tuplas `(departamento, nombre_atleta, mejor_tiempo)` con el mejor tiempo de cada departamento. Usar listas paralelas para departamentos únicos.
- `tiempo_promedio(atletas)`: retorna el tiempo promedio de todos los atletas.
- `atletas_bajo_tiempo(atletas, tiempo_limite)`: retorna los nombres de los atletas cuyo tiempo fue menor al límite indicado.

---

## Ejercicio 29: Puntos en el Plano Cartesiano

En la clase de geometría analítica de un colegio en Manizales, los estudiantes trabajan con coordenadas en el plano. Cada punto se representa como una tupla `(x, y)`:

```python
puntos = [
    (3, 4), (-2, 5), (0, -3), (6, 2), (-4, -4),
    (1, 7), (-5, 1), (8, -1), (2, -6), (-3, 3)
]
```

**Restricciones:** No usar `math.sqrt()`. Calcular la raíz cuadrada usando potencia `0.5` (`valor ** 0.5`). No usar `min()`, `max()`, `sorted()`.

**Funciones requeridas:**
- `distancia_al_origen(punto)`: retorna la distancia euclidiana del punto al origen (0, 0).
- `punto_mas_lejano(puntos)`: retorna la tupla del punto más lejano al origen.
- `cuadrante(punto)`: retorna el número del cuadrante (1, 2, 3 o 4) o `"eje"` si está sobre algún eje.
- `contar_por_cuadrante(puntos)`: retorna una lista de cuatro valores con la cantidad de puntos en cada cuadrante `[Q1, Q2, Q3, Q4]`.
- `par_mas_cercano(puntos)`: retorna las dos tuplas de los puntos que tienen la menor distancia entre sí.

---

## Ejercicio 30: Datos Meteorológicos

El IDEAM recolecta datos climáticos de varias ciudades colombianas. Cada registro es una tupla `(ciudad, temperatura_mínima, temperatura_máxima)`, ambas en grados Celsius:

```python
datos_clima = [
    ("Bogotá",        7,  19),
    ("Medellín",     16,  28),
    ("Cali",         18,  32),
    ("Barranquilla", 24,  34),
    ("Pasto",         5,  17),
    ("Cartagena",    26,  35),
    ("Bucaramanga",  18,  29),
    ("Manizales",    12,  22),
    ("Pereira",      17,  28),
    ("Cúcuta",       22,  36),
]
```

**Restricciones:** No usar `sum()`, `min()`, `max()`, `sorted()`.

**Funciones requeridas:**
- `amplitud_termica(dato)`: retorna la diferencia entre temperatura máxima y mínima de una ciudad (recibe una sola tupla).
- `ciudad_mas_calida(datos)`: retorna el nombre de la ciudad con la temperatura máxima más alta.
- `ciudad_mas_fria(datos)`: retorna el nombre de la ciudad con la temperatura mínima más baja.
- `clima_ideal(datos, temp_min_ideal, temp_max_ideal)`: retorna los nombres de ciudades cuya temperatura mínima sea ≥ `temp_min_ideal` Y cuya temperatura máxima sea ≤ `temp_max_ideal`.
- `ordenar_por_amplitud(datos)`: retorna una nueva lista de tuplas ordenada de mayor a menor amplitud térmica **sin** usar `sorted()`.

---

## Ejercicio 31: Itinerario de Viaje por Colombia

Una agencia de turismo en Bogotá gestiona itinerarios de viaje. Cada destino es una tupla `(ciudad, días_de_estadía, lista_de_actividades)`:

```python
itinerario = [
    ("Cartagena",    3, ["Playa Bocagrande", "Ciudad Amurallada", "Islas del Rosario"]),
    ("Santa Marta",  2, ["Parque Tayrona", "Ciudad Perdida"]),
    ("Barranquilla", 1, ["Carnaval tour"]),
    ("Medellín",     4, ["El Poblado", "Museo de Antioquia", "Parque Arví", "Guatapé"]),
    ("Bogotá",       2, ["La Candelaria", "Monserrate"]),
]
```

**Restricciones:** No usar `sum()`,  `max()`, `sorted()`.

**Funciones requeridas:**
- `total_dias(itinerario)`: retorna el número total de días del viaje.
- `ciudad_con_mas_actividades(itinerario)`: retorna el nombre de la ciudad que tiene más actividades en su lista.
- `actividades_por_dia(itinerario)`: retorna una lista de tuplas `(ciudad, ratio)` donde `ratio` es la cantidad de actividades dividida entre los días de estadía.
- `buscar_actividad(itinerario, actividad)`: retorna el nombre de la ciudad donde se realiza esa actividad, o `"No encontrada"` si no existe.
- `extender_estadia(itinerario, ciudad, dias_extra)`: retorna un **nuevo** itinerario (lista de tuplas) donde la ciudad indicada tiene sus días de estadía aumentados en `dias_extra`.

---

## Ejercicio 32: Registro Médico Simplificado

En una clínica en Cali se maneja el registro básico de pacientes como lista de tuplas. Cada tupla contiene: nombre, edad, tipo_de_sangre y condición_principal:

```python
pacientes = [
    ("María López",     28, "O+",  "Hipertensión"),
    ("Carlos Ruiz",     45, "A+",  "Diabetes"),
    ("Ana Herrera",     33, "B+",  "Asma"),
    ("Pedro Gómez",     62, "O-",  "Hipertensión"),
    ("Laura Castro",    19, "AB+", "Apendicitis"),
    ("Sofía Mendoza",   71, "O+",  "Diabetes"),
    ("Julián Torres",   40, "A-",  "Asma"),
    ("Valentina Ríos",  55, "B-",  "Hipertensión"),
    ("Andrés Mora",     38, "O+",  "Diabetes"),
    ("Gabriela Pinto",  27, "A+",  "Apendicitis"),
]
```

**Restricciones:** No usar `sum()`,  `max()`, `sorted()`, `count()`, diccionarios.

**Funciones requeridas:**
- `pacientes_por_condicion(pacientes, condicion)`: retorna una lista de tuplas con los pacientes que tienen esa condición.
- `tipos_sangre_disponibles(pacientes)`: retorna una lista con los tipos de sangre únicos presentes en el registro.
- `conteo_por_tipo_sangre(pacientes)`: retorna dos listas paralelas `tipos` y `conteos`, indicando cuántos pacientes tienen cada tipo de sangre.
- `edad_promedio_condicion(pacientes, condicion)`: retorna la edad promedio de los pacientes con esa condición.
- `paciente_mayor(pacientes)`: retorna la tupla completa del paciente de mayor edad.
