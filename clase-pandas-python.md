Clase #3: Pandas en Python

Pandas es una biblioteca de Python que sirve para organizar, limpiar y analizar datos en tablas.

1. Conceptos principales

* DataFrame: tabla con filas y columnas.
* Series: una sola columna.
* Índice: identifica cada fila.

2. Comandos básicos

Comando	Función
pd.read_csv()	Cargar archivos CSV
df.head()	Ver primeras filas
df.shape	Ver filas y columnas
df.info()	Ver tipos de datos
df.describe()	Ver estadísticas
df.dropna()	Eliminar datos faltantes
df.drop_duplicates()	Eliminar duplicados

3. Seleccionar datos

* df["nota"]: seleccionar una columna.
* df.loc[]: seleccionar por etiquetas.
* df.iloc[]: seleccionar por posiciones.

4. Filtrar datos

Permite mostrar datos que cumplen condiciones.

df[df["nota"] >= 3]

* & significa Y.
* | significa O.

5. Crear columnas

df["nota_100"] = df["nota"] * 20

6. Agrupar datos

df.groupby("programa")["nota"].mean()

Sirve para calcular promedios por grupos.
