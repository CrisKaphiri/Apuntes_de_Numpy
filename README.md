# Apuntes de NumPy

Este repositorio contiene apuntes personales organizados sobre NumPy, enfocado en su uso para **análisis y manipulación de datos**.

## Contenido

| Sección | Tema | Ejemplo |
|--------|------|---------|
| 1 | Creación de arrays y tipos | `01_creacion_arrays.ipynb` |
| 2 | Información de un array | `02_informacion_arrays.ipynb` |
| 2 | Operaciones matemáticas | `.ipynb` |
| 3 | Indexación y slicing | `.ipynb` |
| 4 | Broadcasting | `.ipynb` |
| 5 | Estadística básica | `.ipynb` |
| 6 | Reshape y concatenación | `.ipynb` |

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

