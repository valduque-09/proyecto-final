\# NumPy



\*\*Algorítmica y Programación\*\*



La presentación explica qué es \*\*NumPy\*\*, una biblioteca de Python utilizada para trabajar con datos numéricos, realizar operaciones matemáticas y organizar grandes cantidades de información de manera rápida y sencilla.



\## 1. ¿Qué es NumPy?



Es una biblioteca de Python que permite realizar cálculos numéricos mediante arreglos llamados `ndarray`.



Se complementa con otras bibliotecas:



\- \*\*NumPy:\*\* cálculos numéricos.

\- \*\*Pandas:\*\* organización y manipulación de datos.

\- \*\*Matplotlib:\*\* creación de gráficos.

\- \*\*Seaborn:\*\* visualización de datos.



\## 2. Listas de Python vs. NumPy



NumPy permite realizar operaciones sobre varios elementos al mismo tiempo, sin necesidad de utilizar ciclos `for`.



Esto hace que los cálculos sean más rápidos y el código más sencillo.



\## 3. Creación de arreglos



Algunas funciones principales son:



\- `np.array()`: crea arreglos.

\- `np.zeros()`: crea arreglos llenos de ceros.

\- `np.arange()`: genera números con intervalos definidos.

\- `np.linspace()`: genera una cantidad determinada de valores.

\- `np.random.normal()`: genera datos aleatorios.



\## 4. Forma y dimensiones



NumPy permite conocer cómo están organizados los datos:



\- `shape`: cantidad de filas y columnas.

\- `ndim`: número de dimensiones.

\- `size`: cantidad total de elementos.

\- `dtype`: tipo de dato almacenado.



\## 5. Indexación y selección



Permite seleccionar elementos específicos de un arreglo utilizando posiciones de filas y columnas.



También permite seleccionar filas completas, columnas o fragmentos de una matriz.



\## 6. Operaciones matemáticas



NumPy permite realizar operaciones directamente sobre los arreglos, como sumas, restas, multiplicaciones, divisiones y potencias.



También incluye funciones matemáticas como:



\- `np.sqrt()`: raíz cuadrada.

\- `np.exp()`: exponencial.

\- `np.log()`: logaritmo.

\- `np.abs()`: valor absoluto.

\- `np.round()`: redondeo.



\## 7. Broadcasting



Es una característica que permite realizar operaciones entre arreglos de diferentes dimensiones o tamaños compatibles, sin necesidad de modificar manualmente sus estructuras.



\## 8. Filtrado de datos



Permite seleccionar elementos que cumplen determinadas condiciones.



Por ejemplo, identificar las notas mayores o iguales a 3 para determinar cuáles cumplen el criterio de aprobación.



\## 9. Estadística descriptiva



NumPy incluye funciones para analizar datos:



\- `mean()`: calcula la media.

\- `median()`: calcula la mediana.

\- `std()`: calcula la desviación estándar.

\- `min()`: obtiene el valor mínimo.

\- `max()`: obtiene el valor máximo.

\- `sum()`: suma los elementos.

\- `unique()`: identifica valores diferentes.



\## 10. Organización de arreglos



También permite modificar y combinar los datos mediante funciones como:



\- `reshape()`: cambia la forma del arreglo.

\- `concatenate()`: une arreglos.

\- `split()`: divide arreglos.

\- `sort()`: ordena los elementos.

\- `ravel()`: convierte el arreglo en una dimensión.



\## 11. Valores faltantes



NumPy permite identificar y trabajar con datos faltantes, representados mediante `NaN`.



Algunas funciones son:



\- `np.isnan()`: identifica valores faltantes.

\- `np.nanmean()`: calcula la media ignorando los valores faltantes.

\- `np.nanstd()`: calcula la desviación estándar ignorándo

