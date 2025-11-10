# Apuntes de NumPy

Este repositorio contiene apuntes personales organizados sobre NumPy, enfocado en su uso para **análisis y manipulación de datos**.

## Contenido

| Sección | Tema | Ejemplo |
|--------|------|---------|
| 1 | Creación de arrays y tipos | `01_creacion_arrays.ipynb` |
| 2 | Información de un array    | `02_informacion_arrays.ipynb` |
| 3 | Indexación y Slicing       | `03_indexacion.ipynb` |
| 4 | Operaciones básicas        | `04_operaciones.ipynb` |
| 5 | Estadística básica         | `05_estadistica.ipynb` |

## 1. Crear array o matríz

| Método | Ejemplo | Descripción |
| ------ | ------- | ----------- |
| `np.array()`       | `np.array([1, 2, 3])`  | Crea array o matríz a partir de una lista |
| `np.zeros()`       | `np.zeros((3, 3))`     | Crea una matríz llena de 0's |
| `np.ones()`        | `np.ones(4)`           | Crea un vector de 1's |
| `np.full()`        | `np.full((3, 3), 5)`   | Crea una matríz llena de un valor específico |
| `np.empty()`       | `np.empty(2, 3)`       | Crea una matríz vacía |
| `np.arange()`      | `np.arange(0, 10, 2)`  | Crea un vector a partir de un rango |
| `np.linspace()`    | `np.linspace(0, 1, 5)` | Crea un vector de N puntos entre dos valores |
| `np.random.rand()` | `np.random.rand(3, 4)` | Crea una matriz con valores entre 1 y 0 |

## 2. Información de un array

| Atributo | Ejemplo | Descripción |
| ------ | ------- | ----------- |
| `.dtype`    | `a.dtype`   | Tipo de dato |
| `.ndim`     | `a.ndim`    | N° de dimensiones |
| `.shape`    | `a.shape`   | Forma del array |
| `.size`     | `a.size`    | Total de elementos |

**NumPy** tiene algunos tipos de datos adicionales y se refiere a ellos con un solo carácter, como `i` para enteros, `u` para enteros sin signos, etc.

| Carácter | Tipo de dato |
| -------- | ------------ |
| `i` | integer |
| `b` | boolean |
| `u` | unsigned integer |
| `f` | float |
| `c` | complex float |
| `m` | timedelta |
| `M` | datetime |
| `O` | object |
| `S` | string |
| `U` | unicode string |
| `V` | void |

La mejor manera de cambiar el tipo de dato de un array existente es crear una copia con el método `astype()`. La función `astype()` crea una copia del array y permite especificar el tipo de dato como parámetro.

El tipo de dato se puede especificar mediante una cadena, como `f` para float, `i` para integer, etc.

O bien, se puede usar el tipo de dato directamente, como `float` para float e `int` para integer.

```
arr=np.array((1.2,20.2 ,30.3)) -> [1.2, 20.2, 30.3] 
arr2=arr.astype("i") -> [1, 20, 30]
```

## 3. Indexación

| Acción | Ejemplo | Resultado |
| ------ | ------- | --------- |
| Acceso por índice    | `a[0]`    | Primer elemento |
| Acceso 2 dimensiones | `a[1, 2]` | Elemento de Fila 2, Columna 3 |
| Rango de valores     | `a[1:4]`  | Elemento desde el indice 1 al indice 3 |
| Saltos               | `a[::2]`  | Cada 2 elementos |
| Corte por fila       | `a[1, :]` | Toda la fila 2 |
| Corte por columna    | `a[:, 0]` | Toda la primera columna |

## 4. Operaciones básicas

Al realizar operaciones con array, se realizan elemento a elemento: `arr = a[i] + b[i]`, creando un nuevo array o modificando sobre el mismo.

| Tipo | Ejemplos |
| ---- | -------- |
| Aritmética            | `a + b` `a - b` `a * 2` `a ** 2` |
| Comparaciones         | `a > 3` `a == b` |
| Álgebra lineal        | `np.dot(a, b)` `np.matmul(a, b)` |
| Funciones matemáticas | `np.sqrt(a)` `np.exp(a)` `np.log(a)` |
| Redondeo              | `np.round(a)` `np.floor(a)` `np.ceil(a)` |

## 5. Estadística

| Función                   | Ejemplo                  | Resultado               |
| ------------------------- | ------------------------ | ----------------------- |
| Media                     | `np.mean(a)`             | Promedio                |
| Mediana                   | `np.median(a)`           | Valor central           |
| Máx / Mín                 | `np.max(a)`, `np.min(a)` | Extremos                |
| Suma total                | `np.sum(a)`              | Sumar todos los valores |
| Varianza / Desv. estándar | `np.var(a)`, `np.std(a)` | Dispersión              |
| Percentiles               | `np.percentile(a, 75)`   | Cuartiles / percentiles |

