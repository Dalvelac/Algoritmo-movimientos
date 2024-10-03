# Algoritmo de Movimientos del Caballo en un Teclado Numérico

## Descripción

Este proyecto calcula las posibilidades válidas de movimientos de un caballo (pieza de ajedrez) sobre un teclado numérico, utilizando una fórmula recursiva. La cantidad de movimientos permitidos es configurable, y el algoritmo sigue las reglas del movimiento en "L" que realiza el caballo en ajedrez.

## Fórmula para el Algoritmo

La fórmula recursiva utilizada para calcular el número de movimientos válidos es la siguiente:

![Fórmula Recursiva](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Formula%20recursiva.JPG)

**Definiciones**:
- **M(n, N)**: Es el número de movimientos válidos que puede hacer el caballo desde la posición `n` con `N` movimientos restantes.
- **C(n)**: Es el conjunto de números a los que el caballo puede moverse desde la posición `n`.

### Movimientos Válidos
A continuación se muestra el conjunto de movimientos válidos desde cada número en el teclado:

- **C(1) = {6, 8}**
- **C(2) = {7, 9}**
- **C(3) = {4, 8}**
- **C(4) = {3, 9, 0}**
- **C(5) = {}** (ningún movimiento válido)
- **C(6) = {1, 7, 0}**
- **C(7) = {2, 6}**
- **C(8) = {1, 3}**
- **C(9) = {2, 4}**
- **C(0) = {4, 6}**

### Explicación de la Fórmula

- El número de caminos desde un número `n` con `N` movimientos es la suma de los caminos válidos desde cada número al que el caballo puede moverse, con `N-1` movimientos restantes.
- Este proceso se repite hasta que `N = 0`, lo que indica que hemos realizado un camino válido.

## Ejemplo de Teclado Numérico

Planteamos que el caballo de ajedrez se moverá sobre un teclado numérico como el siguiente:

![Teclado numérico](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Keypad.JPG)

## Resultados: Tabla de Movimientos Válidos

La siguiente tabla muestra las posibilidades válidas de movimientos en función de la cantidad de movimientos permitidos:

| Cantidad de movimientos | Posibilidades válidas |
|-------------------------|-----------------------|
| 1                       | 20                    |
| 2                       | 46                    |
| 3                       | 104                   |
| 5                       | 544                   |
| 8                       | 6576                  |
| 10                      | 34432                 |
| 15                      | 2140672               |
| 18                      | 25881088              |
| 21                      | 307302400             |
| 23                      | 1609056256            |
| 32                      | 2792668987392         |

## Estructura del Proyecto

El proyecto consta de los siguientes elementos visuales:

El proyecto consta de los siguientes elementos visuales:

1. **Fórmula Recursiva**: Representa la ecuación usada para calcular los movimientos del caballo.
   ![Fórmula Recursiva](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Formula%20recursiva.JPG)

2. **Teclado Numérico**: El teclado donde el caballo se mueve.
   ![Teclado numérico](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Keypad.JPG)

3. **Número de Movimientos Posibles**: La lista de movimientos válidos desde cada número del teclado.
   ![Número de Movimientos Posibles](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Numero%20de%20movimientos%20posibles.JPG)

4. **Tabla de Movimientos**: La tabla que muestra los resultados de las posibilidades válidas para diferentes números de movimientos.
   ![Tabla de Movimientos](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Tabla.JPG)
