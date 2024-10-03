https://github.com/Dalvelac/Algoritmo-movimientos.git
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

## Explicación de cada resultado obtenido
1 Movimiento:

Para 1 movimiento, calculamos los destinos válidos desde cada número directamente (es decir, sin hacer más saltos):

    Desde 1: puede ir a 6 o 8. Hay 2 caminos válidos.
    Desde 2: puede ir a 7 o 9. Hay 2 caminos válidos.
    Desde 3: puede ir a 4 o 8. Hay 2 caminos válidos.
    Desde 4: puede ir a 3, 9, o 0. Hay 3 caminos válidos.
    Desde 5: no puede moverse, así que hay 0 caminos válidos.
    Desde 6: puede ir a 1, 7, o 0. Hay 3 caminos válidos.
    Desde 7: puede ir a 2 o 6. Hay 2 caminos válidos.
    Desde 8: puede ir a 1 o 3. Hay 2 caminos válidos.
    Desde 9: puede ir a 2 o 4. Hay 2 caminos válidos.
    Desde 0: puede ir a 4 o 6. Hay 2 caminos válidos.

Sumando todos estos caminos obtenemos:
2 + 2 + 2 + 3 + 0 + 3 + 2 + 2 + 2 + 2 = 20 caminos válidos.
2 Movimientos:

Ahora calculamos cuántos caminos válidos se pueden hacer con 2 movimientos. Para esto, consideramos todos los posibles destinos después de realizar el primer movimiento.

Ejemplo desde 1 (aplicando la fórmula recursiva):

    Desde 1: el caballo puede ir a 6 o 8.
        Desde 6: puede moverse a 1, 7, o 0.
        Desde 8: puede moverse a 1 o 3.

Entonces:
M(1,2)=M(6,1)+M(8,1)=(3)+(2)=5 caminos vaˊlidos desde 1 con 2 movimientos.
M(1,2)=M(6,1)+M(8,1)=(3)+(2)=5 caminos vaˊlidos desde 1 con 2 movimientos.

Se hace el mismo cálculo para los demás números y se suman todas las posibilidades.

    Para 2 movimientos, el total es 46 caminos válidos.

3 Movimientos:

Continuamos con el mismo proceso para 3 movimientos. El caballo ahora puede hacer 3 saltos en el teclado, y nuevamente sumamos todas las posibilidades válidas desde cada número, utilizando la fórmula recursiva.

    Para 3 movimientos, el total es 104 caminos válidos.

5 Movimientos:

Aplicando el mismo razonamiento, para 5 movimientos:

    El caballo puede realizar 544 caminos válidos en total.

8 Movimientos:

Siguiendo la misma lógica:

    Para 8 movimientos, hay 6576 caminos válidos.

10 Movimientos:

    Para 10 movimientos, hay 34432 caminos válidos.

15 Movimientos:

    Para 15 movimientos, hay 2140672 caminos válidos.

18 Movimientos:

    Para 18 movimientos, hay 25881088 caminos válidos.

21 Movimientos:

    Para 21 movimientos, hay 307302400 caminos válidos.

23 Movimientos:

    Para 23 movimientos, hay 1609056256 caminos válidos.

32 Movimientos:

    Para 32 movimientos, hay 2792668987392 caminos válidos.

Los resultados se han obtenido utilizando el codigo que se encuentra bajo el nombre Calculador Movimientos

## Estructura del Proyecto

El proyecto consta de los siguientes elementos visuales:

El proyecto consta de los siguientes elementos visuales:

1. **Fórmula Recursiva**: Representa la ecuación usada para calcular los movimientos del caballo.
   ![Fórmula Recursiva](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Formula%20recursiva.JPG)

2. **Teclado Numérico**: El teclado donde el caballo se mueve.

    ![Teclado numérico](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Keypad.JPG)

4. **Número de Movimientos Posibles**: La lista de movimientos válidos desde cada número del teclado.
   ![Número de Movimientos Posibles](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Numero%20de%20movimientos%20posibles.JPG)

5. **Tabla de Movimientos**: La tabla que muestra los resultados de las posibilidades válidas para diferentes números de movimientos.
   ![Tabla de Movimientos](https://github.com/Dalvelac/Algoritmo-movimientos/blob/Imagenes/Tabla.JPG)
