**# Marco Teorico
## Variables estadisticas 
Definicion: Una variable estadistica es una caracteristica que puede ser medida en una poblacion o muestra.

Tipos de variables:

* Cualitativas o atributos: Son aquellas que no se pueden medir, solo se pueden clasificar. Ejemplo: color de ojos, sexo, estado civil, etc.
* Cuantitativas: Son aquellas que se pueden medir. Ejemplo: peso, estatura, edad, etc.
  * Discretas: Son aquellas que solo pueden tomar valores enteros. Ejemplo: numero de hijos, numero de estudiantes, etc.
  * Continuas: Son aquellas que pueden tomar cualquier valor real. Ejemplo: peso, estatura, etc.

## Distribuciones de frecuencias. Tipos

Una distribucion de frecuencias es una tabla que resume los datos de una variable. En la tabla se muestra la frecuencia de cada valor de la variable.

**Frecuencia ordinaria o absoluta** del valor $x_i$ es el numero de veces que aparece en la muestra. Se representa por $n_i$.

**Frecuencia absoluta acumulada** del valor $x_i$ es la suma de las frecuencias absolutas de todos los valores menores o iguales a $x_i$. Se representa por $N_i$.

**Frecuencia relativa** del valor $x_i$ es el cociente entre la frecuencia absoluta y el tamaño de la muestra. Se representa por $f_i = \frac{n_i}{N}$. donde $N$ es el tamaño de la muestra. $N = \sum_{i=1}^{k} n_i$

**Frecuencia relativa acumulada** del valor $x_i$ es la suma de las frecuencias relativas de todos los valores menores o iguales a $x_i$. Se representa por $F_i = \frac{N_i}{N}$. 

**Distribucion de frecuencias** es el conjunto de los valores que presenta una variable estadistica junto con sus frecuencias. En general se escribe $\{ \left( x_i, n_i \right) \}_{i=1,2,...,k}$

Tipos de distribuciones de frecuencias:

* Distribuciones de tipo discreto o de datos sin agrupar.
* Distribuciones de tipo continuo o de datos agrupados.

Ejemplo1 para datos sin agrupar: Se considera la variable "numero de miembros", estudiada a 20 familias:
2,3,4,5,8,2,4,5,7,2,1,3,6,4,2,5,5,1,3,4

|$x_i$|$n_i$| $N_i$ |$f_i$|$F_i$|
|---|---|-------|---|---|
|1|2| 2     |0.1|0.1|
|2|4| 6     |0.2|0.3|
|3|3| 9     |0.15|0.45|
|4|4| 13    |0.2|0.65|
|5|4| 17    |0.2|0.85|
|6|1| 18    |0.05|0.9|
|7|1| 19    |0.05|0.95|
|8|1| $\sum_{i=1}^{k} n_i = N = 20$    |0.05| $\sum_{i=1}^{k} f_i = 1$|


Ejemplo2 para datos agrupados: Se considera la variable "estatura de 20 estudiantes en un salon de clase":
1.60, 1.75, 1.62, 1.73, 1.65, 1.70, 1.68, 1.72, 1.69, 1.71, 1.74, 1.67, 1.63, 1.66, 1.64, 1.61, 1.76, 1.59, 1.58, 1.77

Paso 1: Se ordenan los datos de menor a mayor.

Paso 2: Se calcula el rango de los datos. $R = x_{max} - x_{min}$. En este caso $R = 1.77 - 1.58 = 0.19$

Paso 3: Se calcula el numero de intervalos. $k = 1 + 3.3 \log_{10} N$. En este caso $k = 1 + 3.3 \log_{10} 20 = 1 + 3.3 \times 1.301 = 5.29 \approx 6$

Paso 4: Se calcula la amplitud del intervalo. $a = \frac{R}{k} = \frac{0.19}{6} = 0.0317 \approx 0.03$

Paso 5: Se construye la tabla de distribucion de frecuencias agrupadas.

|Intervalo| $n_i$ | $N_i$ | $f_i$ | $F_i$ |
|---|---|---|---|---|
|1.58 - 1.61| 2 | 2 | 0.1 | 0.1 |
|1.61 - 1.64| 3 | 5 | 0.15 | 0.25 |
|1.64 - 1.67| 3 | 8 | 0.15 | 0.4 |
|1.67 - 1.70| 4 | 12 | 0.2 | 0.6 |
|1.70 - 1.73| 4 | 16 | 0.2 | 0.8 |
|1.73 - 1.76| 3 | 19 | 0.15 | 0.95 |
|1.76 - 1.79| 1 | 20 | 0.05 | 1 |

considerando intervalos abiertos a la izquierda y cerrados a la derecha, para evitar que algun $x_i$ pueda pertenecer a mas de un intervalo, se define la amplitud
del intervalo $\left( l_{i-1},l_i \right]$ como $c_i = l_i - l_{i-1}$. 
Como representante de la clase, o valor ideal de la misma, se toma la marca de clase, que es el punto medio del intervalo:
$x_i = \frac{l_{i-1} + l_i}{2}$

Las distribuciones agrupadas en intervalos se resumiran en una tabla con el formato siguiente:

|$l_{i-1}-l_i$|$n_i$|$x_i$|$c_i$|
|---|---|---|---|
|$l_0 - l_1$|$n_1$|$x_1 = \frac{l_0 + l_1}{2}$|$c_1 = l_1 - l_0$|
|$l_1 - l_2$|$n_2$|$x_2 = \frac{l_1 + l_2}{2}$|$c_2 = l_2 - l_1$|
|...|...|...|...|
|$l_{k-1} - l_k$|$n_k$|$x_k = \frac{l_{k-1} + l_k}{2}$|$c_k = l_k - l_{k-1}$|

# Medidas de posicion
## Medidas centrales
### Media aritmetica
La media aritmetica de la distribucion de frecuencias es el valor:

$ \bar{x} = \frac{\sum_{i=1}^{k} n_i x_i}{N} = \sum_{i=1}^{k} f_i x_i$

Observacion: Si la variable viene agrupada en intervalos, la media aritmetica se calcula utilizando las marcas de clase.
El valor resultante de la media aritmetica vendra influenciado por la eleccion de los intervalos, siendo mayor la presicion
cuanto menores sean las longitudes de los intervalos.

### Mediana

En las distribuciones de frecuencias agrupadas en intervalos, no es posible identificar directamente al valor central. 
En este caso seguiremos los pasos siguientes:

* Se calculan las frecuencias acumuladas, $N_i$

# Taller - parte 1

Enunciado:

Se tiene la informacion de la estatura de 20 estudiantes de dos salones de clase:

Salon 1: 1.60, 1.75, 1.62, 1.73, 1.65, 1.70, 1.68, 1.72, 1.69, 1.71, 1.74, 1.67, 1.63, 1.66, 1.64, 1.61, 1.76, 1.59, 1.58, 1.77
Salon 2: 1.70, 1.63, 1.66, 1.64, 1.61, 1.76, 1.59, 1.58, 1.77, 1.60, 1.75, 1.62, 1.73, 1.65, 1.70, 1.68, 1.72, 1.69, 1.71, 1.74

El archivo "estaturas.csv" contiene la informacion de los dos salones de clase y tiene la siguiente estructura

```csv
salon1,salon2
1.6,1.7
1.75,1.63
1.62,1.66
1.73,1.64
1.65,1.61
1.7,1.76
1.68,1.59
1.72,1.58
1.69,1.77
1.71,1.6
1.74,1.75
1.67,1.62
1.63,1.73
1.66,1.65
1.64,1.7
1.61,1.68
1.76,1.72
1.59,1.69
1.58,1.71
1.77,1.74
```
Se pide: en c++ leer el archivo "estaturas.csv" y crear funciones y arreglos para imprimir la tabla de frecuencias de datos agrupados para cada salon de clase.
Ademas se pide imprimir un histograma de cada salon de clase en la consola usando asteriscos.**




