\# Análisis de la base de datos NFL Concussions



\## 1. Descripción general



\*\*Nombre de la base de datos:\*\* NFL Concussions – Concussion Injuries 2012-2014.



\### ¿Qué es la base de datos?



Es un conjunto de datos relacionado con las lesiones registradas en jugadores de la National Football League (NFL), la liga profesional de fútbol americano de Estados Unidos.



Su propósito es estudiar diferentes características de las lesiones deportivas, teniendo en cuenta aspectos como la posición del jugador, el equipo, la temporada, los partidos perdidos y el tiempo de recuperación.



Esta información permite realizar análisis estadísticos y exploratorios para identificar patrones relacionados con las lesiones sufridas por los jugadores durante las temporadas estudiadas.



\### ¿Qué información contiene?



La base de datos reúne registros de lesiones correspondientes al período 2012-2014. Incluye información de los jugadores, sus equipos, las fechas de los partidos y diferentes características relacionadas con las lesiones reportadas.



El notebook utiliza el archivo:



`Concussion Injuries 2012-2014.csv`



\*\*Fuente de los datos:\*\* Archivo CSV utilizado en el notebook original de Kaggle. La dirección exacta de descarga del conjunto de datos no aparece en el archivo proporcionado.



| Característica | Descripción |

|---|---|

| Número de registros | 361, según la distribución de Games Missed |

| Número de columnas | 18 variables |

| Formato | CSV |

| Nombre del archivo | Concussion Injuries 2012-2014.csv |

| Período estudiado | 2012-2014 |



\## 2. Descripción de las columnas



La base de datos contiene 18 variables relacionadas con los jugadores, los partidos y las lesiones deportivas.



| Nombre de columna | Tipo de dato | Descripción |

|---|---|---|

| ID | Texto (str) | Identificador del registro de lesión. |

| Player | Texto (str) | Nombre del jugador. |

| Team | Texto (str) | Equipo al que pertenece el jugador. |

| Game | Texto (str) | Partido en el que ocurrió la lesión. |

| Date | Fecha (str) | Fecha en la que ocurrió la lesión. |

| Opposing Team | Texto (str) | Equipo contrario. |

| Position | Texto (str) | Posición que ocupa el jugador en el campo. |

| Pre-Season Injury? | Texto (str) | Indica si la lesión ocurrió durante la pretemporada. |

| Winning Team? | Texto (str) | Indica si el equipo del jugador ganó el partido. |

| Week of Injury | Entero (int) | Semana de la temporada en la que ocurrió la lesión. |

| Season | Texto (str) | Temporada correspondiente al registro. |

| Weeks Injured | Entero (int) | Cantidad de semanas que el jugador estuvo lesionado. |

| Games Missed | Decimal (float) | Cantidad de partidos que el jugador se perdió. |

| Unknown Injury? | Texto (str) | Indica si el tipo de lesión es desconocido. |

| Reported Injury Type | Texto (str) | Tipo de lesión reportada. |

| Total Snaps | Entero (int) | Cantidad total de jugadas o participaciones registradas. |

| Play Time After Injury | Texto (str) | Tiempo de juego registrado después de la lesión. |

| Average Playtime Before Injury | Texto (str) | Tiempo promedio de juego antes de la lesión. |



\## 3. Análisis exploratorio de los datos



Después de revisar el notebook y los resultados de las operaciones realizadas, se identificaron los siguientes aspectos:



\### 3.1 Distribución de partidos perdidos (Games Missed)



La variable `Games Missed` permite observar cuántos partidos dejaron de disputar los jugadores debido a las lesiones registradas.



Los resultados obtenidos fueron:



| Partidos perdidos | Número de registros |

|---|---:|

| 0 | 190 |

| 1 | 115 |

| 2 | 25 |

| 3 | 10 |

| 4 | 5 |

| 5 | 5 |

| 6 | 4 |

| 7 | 2 |

| 8 | 1 |

| 10 | 1 |

| 11 | 1 |

| 13 | 1 |

| 14 | 1 |

| \*\*Total\*\* | \*\*361\*\* |



Se observa que 190 registros corresponden a jugadores que no perdieron partidos, mientras que 115 registros corresponden a jugadores que perdieron un partido.



Esto representa aproximadamente el 52,6 % y el 31,9 % de los registros, respectivamente.



\### 3.2 Distribución por posiciones



El notebook realiza una gráfica de barras para estudiar la cantidad de lesiones según la posición de los jugadores.



Esta comparación permite observar cómo se distribuyen los registros entre las diferentes posiciones del fútbol americano.



Sin embargo, el notebook no presenta una tabla con los valores exactos de cada posición, por lo que no es posible establecer cuál presenta la mayor cantidad de registros sin consultar los datos originales.



\### 3.3 Tipos de lesiones reportadas



La variable `Reported Injury Type` permite identificar las diferentes categorías de lesiones registradas.



En los ejemplos mostrados en el notebook aparecen categorías como:



\- Head.

\- Concussion.



El análisis utiliza una gráfica de barras para comparar los tipos de lesiones reportadas.



Es importante tener en cuenta que no todas las lesiones registradas deben interpretarse automáticamente como conmociones cerebrales.



\### 3.4 Distribución por temporadas



Se utilizan gráficas para comparar los registros de lesiones correspondientes a las temporadas 2012/2013, 2013/2014 y 2014/2015.



También se realiza una comparación entre las temporadas y las semanas que los jugadores permanecieron lesionados.



Estas representaciones permiten explorar cómo se distribuyen los registros a lo largo de los períodos estudiados.



\### 3.5 Valores faltantes



Durante la revisión de la base de datos se identificaron valores faltantes en cuatro columnas:



| Columna | Valores faltantes |

|---|---:|

| Games Missed | 31 |

| Reported Injury Type | 3 |

| Play Time After Injury | 43 |

| Average Playtime Before Injury | 51 |



Las columnas `Average Playtime Before Injury` y `Play Time After Injury` presentan la mayor cantidad de información faltante.



Esto es importante porque estas variables permiten estudiar el tiempo de juego antes y después de una lesión.



Por esta razón, es necesario realizar una adecuada preparación de los datos antes de desarrollar análisis estadísticos o modelos predictivos.



\### 3.6 Tratamiento de datos faltantes



En el notebook se utiliza la herramienta `SimpleImputer` de Scikit-learn para completar los valores faltantes mediante la estrategia de valor más frecuente.



Posteriormente, se utiliza `LabelEncoder` para transformar las variables categóricas en valores numéricos.



Estas operaciones permiten preparar la información para realizar análisis de correlación y desarrollar modelos de aprendizaje automático.



\## 4. Aplicación del aprendizaje automático



El notebook utiliza un modelo de árbol de decisión mediante la clase `DecisionTreeClassifier` de Scikit-learn.



Se trabaja con dos ejercicios de clasificación y análisis:



\- \*\*Predicción de la posición:\*\* se utiliza la variable `Position` como objetivo para estudiar su relación con las demás características de los registros.

\- \*\*Análisis del tiempo promedio de juego antes de la lesión:\*\* se utiliza `Average Playtime Before Injury` como variable objetivo para explorar su relación con otras características.



También se genera una gráfica de importancia de características, que permite observar qué variables tienen mayor participación en las decisiones del modelo.



Es importante señalar que el segundo ejercicio utiliza un clasificador para una variable que representa tiempo de juego. Sería necesario revisar su tipo de dato y considerar un modelo de regresión si se desea predecir un valor numérico continuo.



Además, el notebook no presenta métricas de evaluación como exactitud, precisión, sensibilidad o matriz de confusión. Por lo tanto, no es posible afirmar que los modelos tengan una capacidad predictiva determinada.



\## 5. Importancia en la ingeniería biomédica



Esta base de datos tiene importancia en la ingeniería biomédica porque permite estudiar las lesiones deportivas y su relación con diferentes características de la actividad física.



Las conmociones cerebrales representan un tema importante dentro de la investigación biomédica, debido a que los impactos repetitivos en la cabeza pueden relacionarse con alteraciones neurológicas.



El análisis de datos permite organizar información sobre las lesiones, estudiar su frecuencia y explorar variables relacionadas con la recuperación de los deportistas.



Además, el uso de herramientas computacionales y modelos estadísticos puede contribuir a investigaciones orientadas a comprender mejor los riesgos asociados con las lesiones deportivas.



\## 6. Conclusiones



La base de datos NFL Concussions contiene información relacionada con lesiones registradas en jugadores de fútbol americano durante el período 2012-2014.



A partir del notebook se identificaron 18 variables que incluyen información de los jugadores, equipos, temporadas, posiciones, tipos de lesiones y partidos perdidos.



El análisis exploratorio permitió identificar que 190 registros corresponden a jugadores que no perdieron partidos y 115 corresponden a jugadores que perdieron un partido.



También se encontraron valores faltantes en cuatro columnas, especialmente en las variables relacionadas con el tiempo de juego antes y después de las lesiones.



Finalmente, el notebook demuestra la aplicación de herramientas de Python como Pandas, NumPy, Matplotlib, Seaborn y Scikit-learn para realizar análisis exploratorios y desarrollar modelos de aprendizaje automático.



Esta base de datos representa una oportunidad para aplicar conocimientos de programación, estadística e ingeniería biomédica al estudio de las lesiones deportivas.



\*\*Nota:\*\* Este análisis tiene fines académicos y no constituye una herramienta de diagnóstico médico ni permite establecer diagnósticos de conmoción cerebral o encefalopatía traumática crónica (CTE).

