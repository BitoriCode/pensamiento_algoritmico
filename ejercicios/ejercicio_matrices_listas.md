# Ejercicios de Matrices con Programación Modular

## Instrucciones generales

- Todos los ejercicios **requieren funciones**. Cada función debe tener al menos un parámetro y retornar un valor con `return`.
- **Restricción global:** No usar `sum()`, `min()`, `max()`, `sort()`, `sorted()` ni librerías externas.
- Los datos provistos son de ejemplo; las funciones deben funcionar con matrices de cualquier tamaño válido.
- El programa principal debe llamar a cada función y mostrar los resultados con un mensaje claro.

---

## Ejercicio 1 — Liga BetPlay: goles por equipo

Una plataforma de estadísticas deportivas registra los **goles anotados** por 5 equipos colombianos a lo largo de 5 fechas del torneo. Los datos se almacenan en una matriz donde cada **fila es un equipo** y cada **columna es una fecha**.

```python
equipos = ["Nacional", "Santa Fe", "Millonarios", "América", "Junior"]

#             Fecha1  Fecha2  Fecha3  Fecha4  Fecha5
goles = [
    [3, 1, 2, 4, 1],   # Nacional
    [1, 2, 3, 1, 2],   # Santa Fe
    [2, 0, 1, 3, 5],   # Millonarios
    [0, 3, 2, 2, 1],   # América
    [1, 2, 4, 0, 2],   # Junior
]
```

Con base en lo anterior se pide un algoritmo que, usando programación modular, permita:

- Calcular el **promedio de goles** anotados por cada equipo en las 5 fechas. Mostrar el nombre del equipo y su promedio. **(15%)**
- Mostrar la **fecha en que se anotaron más goles en total** (sumando todos los equipos). **(15%)**
- Mostrar **cuántas fechas "ganó"** cada equipo, es decir, en cuántas fechas tuvo el mayor número de goles entre todos los equipos de esa fecha. **(15%)**
- Mostrar el equipo con la **mayor diferencia** entre su fecha de más goles y su fecha de menos goles. Por ejemplo, si un equipo anotó como máximo 5 y como mínimo 0, su diferencia es 5. **(15%)**

---

## Ejercicio 2 — Consumo eléctrico en barrios de Medellín

Una empresa de servicios públicos registra el **consumo de energía eléctrica (en kWh)** de 5 barrios de Medellín durante 6 meses. Cada **fila es un barrio** y cada **columna es un mes**.

```python
barrios = ["Poblado", "Laureles", "Belén", "Aranjuez", "Castilla"]

#               Ene   Feb   Mar   Abr   May   Jun
consumo = [
    [1200, 1100,  980, 1050, 1350, 1100],   # Poblado
    [ 900,  870,  820,  680,  960,  880],   # Laureles
    [1050,  980,  910,  950, 1120,  950],   # Belén
    [ 700,  640,  600,  820,  720,  660],   # Aranjuez
    [ 850,  800,  760,  780,  660,  830],   # Castilla
]
```

Con base en lo anterior se pide un algoritmo que, usando programación modular, permita:

- Calcular el **consumo total acumulado** de cada barrio en los 6 meses y mostrarlo de mayor a menor. **(15%)**
- Por cada mes, mostrar el **nombre del barrio con menor consumo**. **(15%)**
- Mostrar el **mes en que el consumo total de todos los barrios fue el más alto**. **(15%)**
- Mostrar el **barrio que más veces estuvo por encima del promedio general del mes** (promedio entre los 5 barrios en ese mes). Por ejemplo, si en un mes el promedio es 900 kWh y un barrio consumió 1050, ese barrio "estuvo por encima" ese mes. **(15%)**

---

## Ejercicio 3 — Ventas semanales en una tienda de barrio

Una tienda de barrio en Bogotá lleva el registro de las **unidades vendidas** de 5 productos durante 5 semanas. Cada **fila es un producto** y cada **columna es una semana**.

```python
productos = ["Arroz", "Aceite", "Leche", "Azúcar", "Café"]

#              Sem1  Sem2  Sem3  Sem4  Sem5
ventas = [
    [120, 135, 110, 145,  98],   # Arroz
    [ 85,  90,  78,  95,  88],   # Aceite
    [200, 185, 210, 195, 220],   # Leche
    [ 65,  72,  55,  80,  75],   # Azúcar
    [150, 140, 165, 155, 160],   # Café
]
```

Con base en lo anterior se pide un algoritmo que, usando programación modular, permita:

- Mostrar la **semana con menores ventas totales** (sumando todos los productos esa semana). **(15%)**
- Por cada producto, mostrar si sus ventas **aumentaron, disminuyeron o se mantuvieron igual** comparando la primera y la última semana. Por ejemplo: `"Arroz: disminuyó en 22 unidades"`. **(15%)**
- Dado un **umbral de 70 unidades**, mostrar los productos que **nunca bajaron** de ese umbral en ninguna semana. **(15%)**
- Mostrar la **semana con mayor variación interna**, entendida como la diferencia entre el producto más vendido y el menos vendido de esa semana. **(15%)**
