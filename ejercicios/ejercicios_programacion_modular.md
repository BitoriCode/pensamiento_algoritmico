# Ejercicios – Programación Modular y Funciones en Python

> **Pensamiento Algorítmico**
>
> **Indicaciones generales:**
>
> - Cada ejercicio incluye la descripción del problema, las entradas/salidas esperadas, validaciones y un pseudocódigo de referencia.
> - Clasifica cada ejercicio según el tipo de función:
>   - **A)** Sin parámetros, sin retorno
>   - **B)** Con parámetros, sin retorno
>   - **C)** Sin parámetros, con retorno
>   - **D)** Con parámetros, con retorno
>   - **E)** Programación modular (varias funciones combinadas)
> - Implementa cada solución en Python.
> - Recuerda aplicar buenas prácticas: nombres descriptivos en `snake_case`, docstrings y validaciones.

---

## Ejercicio 1 – Saludo según la hora

**Tipo:** A) Sin parámetros, sin retorno

**Descripción:** Leer un número entero representando la hora (0–23). Mostrar un saludo según el rango:
- 0–11 → "Buenos días"
- 12–17 → "Buenas tardes"
- 18–23 → "Buenas noches"

**Entradas:** hora (entero).
**Salidas:** mensaje de saludo.
**Validaciones:** si la hora está fuera de 0–23 → "Hora inválida".

**Pseudocódigo**

```text
PROCEDIMIENTO saludo_segun_hora()
    MOSTRAR "Ingrese la hora (0-23):"
    LEER hora
    SI hora < 0 O hora > 23 ENTONCES
        MOSTRAR "Hora inválida"
    SINO SI hora <= 11 ENTONCES
        MOSTRAR "Buenos días"
    SINO SI hora <= 17 ENTONCES
        MOSTRAR "Buenas tardes"
    SINO
        MOSTRAR "Buenas noches"
    FIN SI
FIN PROCEDIMIENTO
```

---

## Ejercicio 2 – Menú de conversión de temperaturas

**Tipo:** A) Sin parámetros, sin retorno

**Descripción:** Mostrar un menú con las opciones:
1. Celsius → Fahrenheit
2. Fahrenheit → Celsius
3. Salir

Repetir hasta que el usuario elija salir. Para cada conversión, leer el valor y mostrar el resultado.

**Fórmulas:** `F = C * 9/5 + 32` y `C = (F - 32) * 5/9`

**Entradas:** opción del menú y temperatura.
**Salidas:** resultado de la conversión.
**Validaciones:** opción inválida → mensaje de error.

**Pseudocódigo**

```text
PROCEDIMIENTO menu_temperaturas()
    MIENTRAS VERDADERO HACER
        MOSTRAR "1. Celsius a Fahrenheit"
        MOSTRAR "2. Fahrenheit a Celsius"
        MOSTRAR "3. Salir"
        LEER opcion
        SI opcion = 3 ENTONCES
            MOSTRAR "Hasta luego"
            SALIR_DEL_BUCLE
        SINO SI opcion = 1 ENTONCES
            LEER temp
            MOSTRAR temp * 9/5 + 32
        SINO SI opcion = 2 ENTONCES
            LEER temp
            MOSTRAR (temp - 32) * 5/9
        SINO
            MOSTRAR "Opción inválida"
        FIN SI
    FIN MIENTRAS
FIN PROCEDIMIENTO
```

---

## Ejercicio 3 – Imprimir triángulo de números

**Tipo:** B) Con parámetros, sin retorno (usa ciclos anidados)

**Descripción:** Recibir un entero `n` e imprimir un triángulo de `n` filas. La fila `k` muestra los números del 1 al `k`.

**Ejemplo** para `n = 4`:
```
1
1 2
1 2 3
1 2 3 4
```

**Validaciones:** si `n < 1` → "Valor inválido".

**Pseudocódigo**

```text
PROCEDIMIENTO triangulo_numeros(n)
    SI n < 1 ENTONCES
        MOSTRAR "Valor inválido"
        RETORNAR
    FIN SI
    PARA k DESDE 1 HASTA n HACER
        PARA j DESDE 1 HASTA k HACER
            MOSTRAR j, " " SIN_SALTO
        FIN PARA
        SALTO_DE_LINEA
    FIN PARA
FIN PROCEDIMIENTO
```

---

## Ejercicio 4 – Clasificador de edades

**Tipo:** B) Con parámetros, sin retorno

**Descripción:** Recibir una edad (entero) y mostrar la clasificación:
- 0–5 → "Primera infancia"
- 6–11 → "Infancia"
- 12–17 → "Adolescencia"
- 18–25 → "Juventud"
- 26–59 → "Adultez"
- 60 en adelante → "Adulto mayor"

**Validaciones:** si la edad es negativa → "Edad inválida".

**Pseudocódigo**

```text
PROCEDIMIENTO clasificar_edad(edad)
    SI edad < 0 ENTONCES
        MOSTRAR "Edad inválida"
        RETORNAR
    FIN SI
    SI edad <= 5 ENTONCES
        MOSTRAR "Primera infancia"
    SINO SI edad <= 11 ENTONCES
        MOSTRAR "Infancia"
    SINO SI edad <= 17 ENTONCES
        MOSTRAR "Adolescencia"
    SINO SI edad <= 25 ENTONCES
        MOSTRAR "Juventud"
    SINO SI edad <= 59 ENTONCES
        MOSTRAR "Adultez"
    SINO
        MOSTRAR "Adulto mayor"
    FIN SI
FIN PROCEDIMIENTO
```

---

## Ejercicio 5 – Dibujar marco con texto centrado

**Tipo:** B) Con parámetros, sin retorno

**Descripción:** Recibir un texto (cadena) y un carácter de borde (por defecto `*`). Imprimir el texto enmarcado. El ancho del marco se ajusta al largo del texto + 4.

**Ejemplo** para `texto = "Hola"` y borde `*`:
```
********
* Hola *
********
```

**Pseudocódigo**

```text
PROCEDIMIENTO enmarcar_texto(texto, borde = "*")
    ancho = longitud(texto) + 4
    MOSTRAR borde repetido ancho veces
    MOSTRAR borde, " ", texto, " ", borde
    MOSTRAR borde repetido ancho veces
FIN PROCEDIMIENTO
```

---

## Ejercicio 6 – Factorial iterativo

**Tipo:** D) Con parámetros, con retorno

**Descripción:** Recibir un entero `n` y retornar su factorial calculado de forma iterativa (sin usar recursividad ni la función `math.factorial`).

**Validación:** si `n < 0` → retornar `None`.

**Pseudocódigo**

```text
FUNCION factorial(n) RETORNA ENTERO o None
    SI n < 0 ENTONCES
        RETORNAR None
    FIN SI
    resultado = 1
    PARA i DESDE 2 HASTA n HACER
        resultado = resultado * i
    FIN PARA
    RETORNAR resultado
FIN FUNCION
```

---

## Ejercicio 7 – Número invertido

**Tipo:** D) Con parámetros, con retorno

**Descripción:** Recibir un entero positivo y retornar el número con sus dígitos invertidos. Por ejemplo, `1234` → `4321`.

**Validación:** si `n <= 0` → retornar `-1`.

**Pseudocódigo**

```text
FUNCION invertir_numero(n) RETORNA ENTERO
    SI n <= 0 ENTONCES
        RETORNAR -1
    FIN SI
    invertido = 0
    MIENTRAS n > 0 HACER
        digito = n % 10
        invertido = invertido * 10 + digito
        n = n // 10
    FIN MIENTRAS
    RETORNAR invertido
FIN FUNCION
```

---

## Ejercicio 8 – MCD (Máximo Común Divisor) por Euclides

**Tipo:** D) Con parámetros, con retorno

**Descripción:** Recibir dos enteros positivos `a` y `b` y retornar su Máximo Común Divisor usando el algoritmo de Euclides: mientras `b ≠ 0`, reemplazar `(a, b)` por `(b, a % b)`. Al final, `a` es el MCD.

**Validaciones:** si `a <= 0` o `b <= 0` → retornar `-1`.

**Pseudocódigo**

```text
FUNCION mcd(a, b) RETORNA ENTERO
    SI a <= 0 O b <= 0 ENTONCES
        RETORNAR -1
    FIN SI
    MIENTRAS b != 0 HACER
        temporal = b
        b = a % b
        a = temporal
    FIN MIENTRAS
    RETORNAR a
FIN FUNCION
```

---

## Ejercicio 9 – Contador de palabras en una frase

**Tipo:** C) Sin parámetros, con retorno

**Descripción:** Leer una frase del usuario y retornar la cantidad de palabras. Se considera que las palabras están separadas por espacios. No usar el método `.split()`.

**Pseudocódigo**

```text
FUNCION contar_palabras() RETORNA ENTERO
    LEER frase
    SI frase es vacía ENTONCES
        RETORNAR 0
    FIN SI
    palabras = 1
    PARA cada caracter ch EN frase HACER
        SI ch = " " ENTONCES
            palabras = palabras + 1
        FIN SI
    FIN PARA
    RETORNAR palabras
FIN FUNCION
```

---

## Ejercicio 10 – Es palíndromo

**Tipo:** D) Con parámetros, con retorno

**Descripción:** Recibir una cadena y retornar `True` si es palíndromo (se lee igual de izquierda a derecha que de derecha a izquierda) o `False` en caso contrario. Ignorar mayúsculas/minúsculas y espacios.

**Ejemplo:** `"Anita lava la tina"` → `True`

**Pseudocódigo**

```text
FUNCION es_palindromo(texto) RETORNA BOOLEANO
    limpio = ""
    PARA cada caracter ch EN texto HACER
        SI ch != " " ENTONCES
            limpio = limpio + minuscula(ch)
        FIN SI
    FIN PARA
    izq = 0
    der = longitud(limpio) - 1
    MIENTRAS izq < der HACER
        SI limpio[izq] != limpio[der] ENTONCES
            RETORNAR FALSO
        FIN SI
        izq = izq + 1
        der = der - 1
    FIN MIENTRAS
    RETORNAR VERDADERO
FIN FUNCION
```

---

## Ejercicio 11 – Calculadora con funciones separadas

**Tipo:** E) Programación modular (varias funciones)

**Descripción:** Crear un programa modular de calculadora con las siguientes funciones independientes:
- `sumar(a, b)` → retorna `a + b`
- `restar(a, b)` → retorna `a - b`
- `multiplicar(a, b)` → retorna `a * b`
- `dividir(a, b)` → retorna `a / b` (validar que `b ≠ 0`)
- `menu_calculadora()` → muestra menú, lee opción y operandos, llama la función apropiada y muestra resultado. Repite hasta que el usuario elija salir.

**Pseudocódigo**

```text
FUNCION sumar(a, b) RETORNA REAL
    RETORNAR a + b
FIN FUNCION

FUNCION restar(a, b) RETORNA REAL
    RETORNAR a - b
FIN FUNCION

FUNCION multiplicar(a, b) RETORNA REAL
    RETORNAR a * b
FIN FUNCION

FUNCION dividir(a, b) RETORNA REAL o None
    SI b = 0 ENTONCES
        MOSTRAR "Error: división por cero"
        RETORNAR None
    FIN SI
    RETORNAR a / b
FIN FUNCION

PROCEDIMIENTO menu_calculadora()
    MIENTRAS VERDADERO HACER
        MOSTRAR "1.Sumar 2.Restar 3.Multiplicar 4.Dividir 5.Salir"
        LEER op
        SI op = 5 ENTONCES
            SALIR_DEL_BUCLE
        FIN SI
        SI op >= 1 Y op <= 4 ENTONCES
            LEER a, b
            SI op = 1 ENTONCES
                MOSTRAR sumar(a, b)
            SINO SI op = 2 ENTONCES
                MOSTRAR restar(a, b)
            SINO SI op = 3 ENTONCES
                MOSTRAR multiplicar(a, b)
            SINO
                resultado = dividir(a, b)
                SI resultado != None ENTONCES
                    MOSTRAR resultado
                FIN SI
            FIN SI
        SINO
            MOSTRAR "Opción inválida"
        FIN SI
    FIN MIENTRAS
FIN PROCEDIMIENTO
```

---

## Ejercicio 12 – Generar contraseña aleatoria

**Tipo:** D) Con parámetros, con retorno

**Descripción:** Crear una función que reciba la longitud deseada (entero) y retorne una contraseña generada aleatoriamente con letras minúsculas, mayúsculas y dígitos. Usar el módulo `random`.

**Validación:** si longitud < 4 → retornar `"Longitud mínima: 4"`.

**Pseudocódigo**

```text
FUNCION generar_contrasena(longitud) RETORNA CADENA
    SI longitud < 4 ENTONCES
        RETORNAR "Longitud mínima: 4"
    FIN SI
    caracteres = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789"
    contrasena = ""
    PARA i DESDE 1 HASTA longitud HACER
        indice = aleatorio(0, longitud(caracteres) - 1)
        contrasena = contrasena + caracteres[indice]
    FIN PARA
    RETORNAR contrasena
FIN FUNCION
```

---

## Ejercicio 13 – Fibonacci iterativo

**Tipo:** D) Con parámetros, con retorno

**Descripción:** Recibir un entero `n` (≥ 0) y retornar el n-ésimo término de la serie de Fibonacci. La serie es: `F(0) = 0, F(1) = 1, F(n) = F(n-1) + F(n-2)`.

**Validación:** si `n < 0` → retornar `-1`.

**Pseudocódigo**

```text
FUNCION fibonacci(n) RETORNA ENTERO
    SI n < 0 ENTONCES
        RETORNAR -1
    FIN SI
    SI n = 0 ENTONCES
        RETORNAR 0
    FIN SI
    SI n = 1 ENTONCES
        RETORNAR 1
    FIN SI
    anterior = 0
    actual = 1
    PARA i DESDE 2 HASTA n HACER
        siguiente = anterior + actual
        anterior = actual
        actual = siguiente
    FIN PARA
    RETORNAR actual
FIN FUNCION
```

---

## Ejercicio 14 – Suma recursiva de los dígitos

**Tipo:** D) Con parámetros, con retorno (recursivo)

**Descripción:** Recibir un entero no negativo y retornar la suma de sus dígitos usando **recursividad**.

**Caso base:** si `n < 10` → retornar `n`.
**Caso recursivo:** retornar `(n % 10) + suma_digitos_rec(n // 10)`.

**Validación:** si `n < 0` → retornar `-1`.

**Pseudocódigo**

```text
FUNCION suma_digitos_rec(n) RETORNA ENTERO
    SI n < 0 ENTONCES
        RETORNAR -1
    FIN SI
    SI n < 10 ENTONCES
        RETORNAR n
    FIN SI
    RETORNAR (n % 10) + suma_digitos_rec(n // 10)
FIN FUNCION
```

---

## Ejercicio 15 – Potencia recursiva

**Tipo:** D) Con parámetros, con retorno (recursivo)

**Descripción:** Recibir una base `b` y un exponente entero no negativo `e`. Retornar `b^e` usando recursividad.

**Caso base:** si `e = 0` → retornar `1`.
**Caso recursivo:** retornar `b * potencia_rec(b, e - 1)`.

**Validación:** si `e < 0` → retornar `None`.

**Pseudocódigo**

```text
FUNCION potencia_rec(b, e) RETORNA ENTERO o None
    SI e < 0 ENTONCES
        RETORNAR None
    FIN SI
    SI e = 0 ENTONCES
        RETORNAR 1
    FIN SI
    RETORNAR b * potencia_rec(b, e - 1)
FIN FUNCION
```

---

## Ejercicio 16 – Validador de notas con funciones

**Tipo:** E) Programación modular (varias funciones)

**Descripción:** Crear un programa modular para gestionar notas de un estudiante:

- `leer_nota()` → lee una nota del usuario y la retorna. Debe repetir la lectura si el valor no está entre 0.0 y 5.0.
- `calcular_promedio(nota1, nota2, nota3)` → retorna el promedio de tres notas.
- `determinar_estado(promedio)` → retorna `"Aprobado"` si promedio ≥ 3.0, `"Reprobado"` en caso contrario.
- `programa_principal()` → llama las tres funciones anteriores, muestra el promedio y el estado.

**Pseudocódigo**

```text
FUNCION leer_nota() RETORNA REAL
    MIENTRAS VERDADERO HACER
        MOSTRAR "Ingrese nota (0.0 - 5.0):"
        LEER nota
        SI nota >= 0.0 Y nota <= 5.0 ENTONCES
            RETORNAR nota
        FIN SI
        MOSTRAR "Nota fuera de rango, intente de nuevo"
    FIN MIENTRAS
FIN FUNCION

FUNCION calcular_promedio(n1, n2, n3) RETORNA REAL
    RETORNAR (n1 + n2 + n3) / 3
FIN FUNCION

FUNCION determinar_estado(promedio) RETORNA CADENA
    SI promedio >= 3.0 ENTONCES
        RETORNAR "Aprobado"
    SINO
        RETORNAR "Reprobado"
    FIN SI
FIN FUNCION

PROCEDIMIENTO programa_principal()
    nota1 = leer_nota()
    nota2 = leer_nota()
    nota3 = leer_nota()
    prom = calcular_promedio(nota1, nota2, nota3)
    estado = determinar_estado(prom)
    MOSTRAR "Promedio:", prom, " - Estado:", estado
FIN PROCEDIMIENTO
```

---

## Ejercicio 17 – Cifrado César

**Tipo:** E) Programación modular (varias funciones)

**Descripción:** Implementar el cifrado César con las siguientes funciones:

- `cifrar_caracter(c, desplazamiento)` → recibe un carácter en minúscula y un desplazamiento entero, retorna el carácter cifrado. Si no es letra, lo retorna sin cambio.
- `cifrar_texto(texto, desplazamiento)` → aplica `cifrar_caracter` a cada carácter del texto (convertido a minúsculas) y retorna el texto cifrado.
- `descifrar_texto(texto_cifrado, desplazamiento)` → descifra aplicando el desplazamiento inverso.

**Fórmula del cifrado:** `nuevo = (posicion_original + desplazamiento) % 26`

**Pseudocódigo**

```text
FUNCION cifrar_caracter(c, desp) RETORNA CARACTER
    SI c >= "a" Y c <= "z" ENTONCES
        posicion = codigo(c) - codigo("a")
        nueva_pos = (posicion + desp) % 26
        RETORNAR caracter(codigo("a") + nueva_pos)
    FIN SI
    RETORNAR c
FIN FUNCION

FUNCION cifrar_texto(texto, desp) RETORNA CADENA
    resultado = ""
    PARA cada caracter ch EN minuscula(texto) HACER
        resultado = resultado + cifrar_caracter(ch, desp)
    FIN PARA
    RETORNAR resultado
FIN FUNCION

FUNCION descifrar_texto(texto_cifrado, desp) RETORNA CADENA
    RETORNAR cifrar_texto(texto_cifrado, 26 - desp)
FIN FUNCION
```

---

## Ejercicio 18 – Análisis de números con menú

**Tipo:** E) Programación modular (varias funciones)

**Descripción:** Crear un programa modular que lea un número entero del usuario y ofrezca un menú con opciones de análisis. Cada opción debe estar implementada en una **función separada**:

1. `es_par(n)` → retorna `True` si `n` es par.
2. `es_primo(n)` → retorna `True` si `n` es primo.
3. `suma_digitos(n)` → retorna la suma de los dígitos de `n`.
4. `es_perfecto(n)` → retorna `True` si `n` es un número perfecto (la suma de sus divisores propios es igual a `n`).
5. Salir.

El menú se repite hasta que el usuario elija salir.

**Pseudocódigo**

```text
FUNCION es_par(n) RETORNA BOOLEANO
    RETORNAR n % 2 = 0
FIN FUNCION

FUNCION es_primo(n) RETORNA BOOLEANO
    SI n < 2 ENTONCES
        RETORNAR FALSO
    FIN SI
    PARA k DESDE 2 HASTA n - 1 HACER
        SI n % k = 0 ENTONCES
            RETORNAR FALSO
        FIN SI
    FIN PARA
    RETORNAR VERDADERO
FIN FUNCION

FUNCION suma_digitos(n) RETORNA ENTERO
    n = valor_absoluto(n)
    suma = 0
    MIENTRAS n > 0 HACER
        suma = suma + (n % 10)
        n = n // 10
    FIN MIENTRAS
    RETORNAR suma
FIN FUNCION

FUNCION es_perfecto(n) RETORNA BOOLEANO
    SI n <= 1 ENTONCES
        RETORNAR FALSO
    FIN SI
    suma = 0
    PARA i DESDE 1 HASTA n - 1 HACER
        SI n % i = 0 ENTONCES
            suma = suma + i
        FIN SI
    FIN PARA
    RETORNAR suma = n
FIN FUNCION

PROCEDIMIENTO menu_analisis()
    MOSTRAR "Ingrese un número:"
    LEER num
    MIENTRAS VERDADERO HACER
        MOSTRAR "1.Par? 2.Primo? 3.Suma dígitos 4.Perfecto? 5.Salir"
        LEER op
        SI op = 1 ENTONCES
            MOSTRAR es_par(num)
        SINO SI op = 2 ENTONCES
            MOSTRAR es_primo(num)
        SINO SI op = 3 ENTONCES
            MOSTRAR suma_digitos(num)
        SINO SI op = 4 ENTONCES
            MOSTRAR es_perfecto(num)
        SINO SI op = 5 ENTONCES
            SALIR_DEL_BUCLE
        SINO
            MOSTRAR "Opción inválida"
        FIN SI
    FIN MIENTRAS
FIN PROCEDIMIENTO
```

---

## Ejercicio 19 – Conversor de bases numéricas

**Tipo:** E) Programación modular (varias funciones)

**Descripción:** Crear funciones para convertir un entero decimal positivo a diferentes bases:

- `decimal_a_binario(n)` → retorna la representación binaria como cadena.
- `decimal_a_octal(n)` → retorna la representación octal como cadena.
- `decimal_a_hexadecimal(n)` → retorna la representación hexadecimal como cadena.

**No usar** las funciones integradas `bin()`, `oct()`, `hex()`.

Para cada función, aplicar divisiones sucesivas entre la base correspondiente, acumulando los residuos.

**Validación:** si `n < 0` → retornar `"Número inválido"`.

**Pseudocódigo**

```text
FUNCION decimal_a_binario(n) RETORNA CADENA
    SI n < 0 ENTONCES
        RETORNAR "Número inválido"
    FIN SI
    SI n = 0 ENTONCES
        RETORNAR "0"
    FIN SI
    resultado = ""
    MIENTRAS n > 0 HACER
        residuo = n % 2
        resultado = texto(residuo) + resultado
        n = n // 2
    FIN MIENTRAS
    RETORNAR resultado
FIN FUNCION

FUNCION decimal_a_octal(n) RETORNA CADENA
    SI n < 0 ENTONCES
        RETORNAR "Número inválido"
    FIN SI
    SI n = 0 ENTONCES
        RETORNAR "0"
    FIN SI
    resultado = ""
    MIENTRAS n > 0 HACER
        residuo = n % 8
        resultado = texto(residuo) + resultado
        n = n // 8
    FIN MIENTRAS
    RETORNAR resultado
FIN FUNCION

FUNCION decimal_a_hexadecimal(n) RETORNA CADENA
    SI n < 0 ENTONCES
        RETORNAR "Número inválido"
    FIN SI
    SI n = 0 ENTONCES
        RETORNAR "0"
    FIN SI
    hex_chars = "0123456789ABCDEF"
    resultado = ""
    MIENTRAS n > 0 HACER
        residuo = n % 16
        resultado = hex_chars[residuo] + resultado
        n = n // 16
    FIN MIENTRAS
    RETORNAR resultado
FIN FUNCION
```

---

## Ejercicio 20 – Sistema de gestión de estudiantes

**Tipo:** E) Programación modular (varias funciones – ejercicio integrador)

**Descripción:** Crear un programa completo y modular para gestionar información de estudiantes. El programa usa una lista para almacenar nombres y otra para almacenar promedios. Implementar las siguientes funciones:

- `agregar_estudiante(nombres, promedios)` → lee nombre y promedio, los agrega a las listas. Valida que el promedio esté entre 0.0 y 5.0.
- `mostrar_estudiantes(nombres, promedios)` → imprime la lista de estudiantes con sus promedios.
- `mejor_promedio(nombres, promedios)` → retorna el nombre del estudiante con el promedio más alto.
- `promedio_general(promedios)` → retorna el promedio general de todos los estudiantes.
- `contar_aprobados(promedios, minimo=3.0)` → retorna cuántos estudiantes tienen promedio ≥ `minimo` (parámetro con valor por defecto).
- `menu_principal()` → muestra un menú con las opciones y llama la función correspondiente.

**Pseudocódigo**

```text
PROCEDIMIENTO agregar_estudiante(nombres, promedios)
    MOSTRAR "Nombre del estudiante:"
    LEER nombre
    MIENTRAS VERDADERO HACER
        MOSTRAR "Promedio (0.0 - 5.0):"
        LEER prom
        SI prom >= 0.0 Y prom <= 5.0 ENTONCES
            SALIR_DEL_BUCLE
        FIN SI
        MOSTRAR "Promedio inválido"
    FIN MIENTRAS
    agregar nombre a nombres
    agregar prom a promedios
    MOSTRAR "Estudiante agregado"
FIN PROCEDIMIENTO

PROCEDIMIENTO mostrar_estudiantes(nombres, promedios)
    SI longitud(nombres) = 0 ENTONCES
        MOSTRAR "No hay estudiantes registrados"
        RETORNAR
    FIN SI
    PARA i DESDE 0 HASTA longitud(nombres) - 1 HACER
        MOSTRAR i + 1, ". ", nombres[i], " - Promedio: ", promedios[i]
    FIN PARA
FIN PROCEDIMIENTO

FUNCION mejor_promedio(nombres, promedios) RETORNA CADENA
    SI longitud(nombres) = 0 ENTONCES
        RETORNAR "No hay estudiantes"
    FIN SI
    mejor_idx = 0
    PARA i DESDE 1 HASTA longitud(promedios) - 1 HACER
        SI promedios[i] > promedios[mejor_idx] ENTONCES
            mejor_idx = i
        FIN SI
    FIN PARA
    RETORNAR nombres[mejor_idx]
FIN FUNCION

FUNCION promedio_general(promedios) RETORNA REAL
    SI longitud(promedios) = 0 ENTONCES
        RETORNAR 0.0
    FIN SI
    suma = 0
    PARA cada p EN promedios HACER
        suma = suma + p
    FIN PARA
    RETORNAR suma / longitud(promedios)
FIN FUNCION

FUNCION contar_aprobados(promedios, minimo = 3.0) RETORNA ENTERO
    contador = 0
    PARA cada p EN promedios HACER
        SI p >= minimo ENTONCES
            contador = contador + 1
        FIN SI
    FIN PARA
    RETORNAR contador
FIN FUNCION

PROCEDIMIENTO menu_principal()
    nombres = []
    promedios = []
    MIENTRAS VERDADERO HACER
        MOSTRAR "1.Agregar 2.Mostrar 3.Mejor promedio"
        MOSTRAR "4.Promedio general 5.Aprobados 6.Salir"
        LEER op
        SI op = 1 ENTONCES
            agregar_estudiante(nombres, promedios)
        SINO SI op = 2 ENTONCES
            mostrar_estudiantes(nombres, promedios)
        SINO SI op = 3 ENTONCES
            MOSTRAR mejor_promedio(nombres, promedios)
        SINO SI op = 4 ENTONCES
            MOSTRAR promedio_general(promedios)
        SINO SI op = 5 ENTONCES
            MOSTRAR contar_aprobados(promedios)
        SINO SI op = 6 ENTONCES
            SALIR_DEL_BUCLE
        SINO
            MOSTRAR "Opción inválida"
        FIN SI
    FIN MIENTRAS
FIN PROCEDIMIENTO
```

---

## Tabla resumen de ejercicios

| # | Ejercicio | Tipo | Conceptos clave |
|---|---|---|---|
| 1 | Saludo según la hora | A | Condicionales, sin parámetros |
| 2 | Menú de conversión de temperaturas | A | Bucle `while`, menú interactivo |
| 3 | Triángulo de números | B | Ciclos anidados, parámetros |
| 4 | Clasificador de edades | B | Condicionales, parámetros |
| 5 | Marco con texto centrado | B | Parámetros por defecto, cadenas |
| 6 | Factorial iterativo | D | Ciclo `for`, retorno |
| 7 | Número invertido | D | Operadores `%` y `//`, retorno |
| 8 | MCD por Euclides | D | Algoritmo clásico, `while`, retorno |
| 9 | Contador de palabras | C | Recorrido de cadenas, retorno |
| 10 | Es palíndromo | D | Cadenas, dos punteros, retorno booleano |
| 11 | Calculadora modular | E | Múltiples funciones, menú |
| 12 | Generar contraseña | D | Módulo `random`, cadenas |
| 13 | Fibonacci iterativo | D | Serie, variables auxiliares |
| 14 | Suma recursiva de dígitos | D | Recursividad |
| 15 | Potencia recursiva | D | Recursividad |
| 16 | Validador de notas | E | Modularidad, validación de entrada |
| 17 | Cifrado César | E | Modularidad, ASCII, cadenas |
| 18 | Análisis de números | E | Modularidad, menú, múltiples funciones |
| 19 | Conversor de bases | E | Modularidad, divisiones sucesivas |
| 20 | Gestión de estudiantes | E | Integrador, listas, parámetros por defecto |
