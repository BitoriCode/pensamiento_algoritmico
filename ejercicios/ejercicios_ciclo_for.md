# Taller — Ciclos `for`

## Objetivo
Practicar ciclos **`for` usando únicamente `range()`**, combinados con **condicionales** (`if/elif/else`) y variables de apoyo (acumuladores/contadores).  
La solución debe construirse en **dos etapas**:
1. **Pseudocódigo**
2. **Código en Python**

---

## Reglas del taller
### Permitido:
- `for i in range(...)`
- `if / elif / else`
- Acumuladores y contadores (`suma`, `contador`, `mayor`, `menor`, etc.)
- Operadores aritméticos y lógicos
- `input()` y `print()`


---

## Plantilla sugerida (pseudocódigo)
Usa esta estructura para cada ejercicio:

**Pseudocódigo**
- Inicio
- Leer entradas (si aplica)
- Inicializar variables
- Para i desde ... hasta ... (con paso ...)
  - Si (condición) entonces ...
  - Actualizar acumuladores/contadores
- Mostrar salida
- Fin

---

# Ejercicios (incrementales)

> Nota: Cada ejercicio está en 2 formatos:
> - **A) GitHub:** Entrada / Proceso / Salida
> - **B) Prosa:** enunciado directo

---

## 1) Contar del 1 al 10
**A) Entrada / Proceso / Salida**
- **Entrada:** ninguna
- **Proceso:** recorrer con `range` e imprimir cada número
- **Salida:** números del 1 al 10 (uno por línea)

**B) Prosa**
Imprime en pantalla los números del 1 al 10 usando un `for` con `range()`.

---

## 2) Contar del 10 al 1
**A) Entrada / Proceso / Salida**
- **Entrada:** ninguna
- **Proceso:** recorrer con `range` descendente e imprimir
- **Salida:** números del 10 al 1 (uno por línea)

**B) Prosa**
Imprime los números del 10 al 1 usando un `for` con `range()` descendente.

---

## 3) Saltos de 5 en 5 (0 a 50)
**A) Entrada / Proceso / Salida**
- **Entrada:** ninguna
- **Proceso:** recorrer de 0 a 50 con paso 5 e imprimir
- **Salida:** `0, 5, 10, ..., 50`

**B) Prosa**
Imprime los múltiplos de 5 desde 0 hasta 50.

---

## 4) Pares entre 1 y N
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (entero positivo)
- **Proceso:** recorrer 1..N y con condicional imprimir solo pares
- **Salida:** pares entre 1 y N

**B) Prosa**
Pide un número `N` e imprime únicamente los números pares entre 1 y `N`.

---

## 5) Impares entre 1 y N
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (entero positivo)
- **Proceso:** recorrer 1..N y con condicional imprimir solo impares
- **Salida:** impares entre 1 y N

**B) Prosa**
Pide un número `N` e imprime únicamente los números impares entre 1 y `N`.

---

## 6) Suma del 1 al N
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (entero positivo)
- **Proceso:** acumular `1 + 2 + ... + N`
- **Salida:** suma total

**B) Prosa**
Pide `N` y calcula la suma de todos los números del 1 hasta `N`.

---

## 7) Suma de pares hasta N
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (entero positivo)
- **Proceso:** recorrer 1..N; si es par, sumarlo
- **Salida:** suma de pares

**B) Prosa**
Pide `N` y calcula la suma de los números pares entre 1 y `N`.

---

## 8) Contar múltiplos de 3 (1 a N)
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (entero positivo)
- **Proceso:** recorrer 1..N; contar si `i % 3 == 0`
- **Salida:** cantidad de múltiplos de 3

**B) Prosa**
Pide `N` y cuenta cuántos múltiplos de 3 hay entre 1 y `N`.

---

## 9) Producto del 1 al N
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (entero positivo)
- **Proceso:** multiplicar acumulativamente `1 * 2 * ... * N`
- **Salida:** producto total

**B) Prosa**
Pide `N` y calcula el producto de `1 * 2 * 3 * ... * N`.

---

## 10) Promedio de K números
**A) Entrada / Proceso / Salida**
- **Entrada:** `K` y luego `K` números
- **Proceso:** acumular suma; al final dividir entre K
- **Salida:** promedio

**B) Prosa**
Pide `K` y luego solicita `K` números; al final muestra el promedio.

---

## 11) Mayor de K números
**A) Entrada / Proceso / Salida**
- **Entrada:** `K` y luego `K` números
- **Proceso:** mantener un `mayor` y actualizarlo si aparece un número más grande
- **Salida:** el mayor

**B) Prosa**
Pide `K` y luego solicita `K` números; al final muestra el número mayor.

---

## 12) Menor y mayor de K números
**A) Entrada / Proceso / Salida**
- **Entrada:** `K` y luego `K` números
- **Proceso:** mantener `menor` y `mayor` (actualizarlos con condicionales)
- **Salida:** menor y mayor

**B) Prosa**
Pide `K` y luego solicita `K` números; al final muestra el menor y el mayor.

---

## 13) Clasificar K números (positivos/negativos/ceros)
**A) Entrada / Proceso / Salida**
- **Entrada:** `K` y luego `K` números
- **Proceso:** contar positivos, negativos y ceros con `if/elif/else`
- **Salida:** 3 conteos

**B) Prosa**
Pide `K` números y al final indica cuántos fueron positivos, cuántos negativos y cuántos ceros.

---

## 14) Aprobados y reprobados
**A) Entrada / Proceso / Salida**
- **Entrada:** `K` notas (0.0 a 5.0)
- **Proceso:** contar `>= 3.0` y `< 3.0`
- **Salida:** aprobados y reprobados

**B) Prosa**
Pide `K` notas y al final indica cuántas son aprobadas (>= 3.0) y cuántas reprobadas (< 3.0).

---

## 15) Suma separada: pares vs impares (1 a N)
**A) Entrada / Proceso / Salida**
- **Entrada:** `N`
- **Proceso:** recorrer 1..N; acumular pares e impares en variables distintas
- **Salida:** suma de pares y suma de impares

**B) Prosa**
Pide `N` y calcula por separado la suma de pares y la suma de impares entre 1 y `N`.

---

## 16) Factorial de N (con validación)
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (entero)
- **Proceso:** si `N < 0` mostrar mensaje; si no, calcular `N!`
- **Salida:** factorial o mensaje

**B) Prosa**
Pide `N`; si es negativo muestra un mensaje, y si no, calcula el factorial `N!`.

---

## 17) Serie alternada: 1 - 2 + 3 - 4 + ... ± N
**A) Entrada / Proceso / Salida**
- **Entrada:** `N`
- **Proceso:** recorrer 1..N; si `i` es par, restar; si no, sumar
- **Salida:** resultado final

**B) Prosa**
Pide `N` y calcula el valor de la serie alternada `1 - 2 + 3 - 4 + ... ± N`.

---

## 18) Contar cuántos divisores tiene N
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (entero positivo)
- **Proceso:** recorrer 1..N; contar cuántos números dividen a N exacto
- **Salida:** cantidad de divisores

**B) Prosa**
Pide `N` y cuenta cuántos divisores exactos tiene entre 1 y `N`.

---

## 19) Detector de número primo (básico)
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (entero >= 2)
- **Proceso:** recorrer posibles divisores; si tiene más de 2 divisores, no es primo
- **Salida:** “Es primo” o “No es primo”

**B) Prosa**
Pide `N` y determina si es primo probando divisores con un único `for` (sin ciclos anidados).

---

## 20) Fibonacci de N términos (sin listas obligatorias)
**A) Entrada / Proceso / Salida**
- **Entrada:** `N` (cantidad de términos, `N >= 1`)
- **Proceso:** usar dos variables para generar términos y mostrarlos en cada iteración
- **Salida:** los N términos

**B) Prosa**
Pide `N` y muestra los `N` primeros términos de Fibonacci usando solo un ciclo `for`.

---
