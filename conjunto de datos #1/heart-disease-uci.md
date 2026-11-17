\# Análisis de la base de datos Heart Disease UCI



\## 1. Descripción general



\*\*Nombre de la base de datos:\*\* Heart Disease UCI – Biomedical Data Analysis.



\### ¿Qué es la base de datos?



Es una base de datos que contiene información clínica relacionada con enfermedades cardiovasculares. Su propósito es analizar diferentes características de los pacientes para identificar posibles relaciones entre sus condiciones médicas y la presencia de enfermedades cardíacas.



Esta información permite realizar análisis estadísticos y desarrollar modelos de aprendizaje automático que ayuden a estudiar y clasificar los casos de enfermedad cardiovascular.



\### ¿Cómo se obtuvieron los datos?



Los datos corresponden a registros clínicos de pacientes recopilados en diferentes centros médicos. Incluyen información demográfica, antecedentes y mediciones relacionadas con evaluaciones cardiovasculares.



El conjunto de datos reúne información de cuatro procedencias: Cleveland, Hungary, VA Long Beach y Switzerland.



\*\*Fuente:\*\* \[Kaggle – Heart Disease UCI](https://www.kaggle.com/datasets/andreshinojosadata/heart-disease-uci-biomedical-data-analysis)



| Característica | Descripción |

|---|---|

| Número de filas | 920 registros |

| Número de columnas | 16 variables |

| Formato | CSV (valores separados por comas) |

| Nombre del archivo | `heart\_disease\_uci.csv` |



\## 2. Descripción de las columnas



| Nombre de columna | Tipo de dato | Descripción | Ejemplo |

|---|---|---|---|

| id | Entero (int) | Identificador único de cada registro. | 1 |

| age | Entero (int) | Edad del paciente en años. | 63 |

| sex | Texto (str) | Sexo del paciente. | Male |

| dataset | Texto (str) | Centro o procedencia del registro clínico. | Cleveland |

| cp | Texto (str) | Tipo de dolor en el pecho presentado por el paciente. | asymptomatic |

| trestbps | Decimal (float) | Presión arterial en reposo, medida en mmHg. | 120.0 |

| chol | Decimal (float) | Nivel de colesterol sérico en mg/dl. | 233.0 |

| fbs | Booleano (bool) | Indica si el nivel de azúcar en sangre en ayunas es superior a 120 mg/dl. | True |

| restecg | Texto (str) | Resultados del electrocardiograma en reposo. | normal |

| thalch | Decimal (float) | Frecuencia cardíaca máxima alcanzada. | 150.0 |

| exang | Booleano (bool) | Indica si el paciente presentó angina inducida por ejercicio. | False |

| oldpeak | Decimal (float) | Depresión del segmento ST inducida por el ejercicio respecto al reposo. | 2.3 |

| slope | Texto (str) | Pendiente del segmento ST durante el ejercicio máximo. | flat |

| ca | Decimal (float) | Número de vasos sanguíneos principales observados mediante fluoroscopia. | 0.0 |

| thal | Texto (str) | Resultado de la prueba relacionada con talasemia. | normal |

| num | Entero (int) | Variable objetivo que representa el diagnóstico de enfermedad cardíaca. | 0 |



\## 3. Análisis exploratorio de los datos



Después de revisar la base de datos, se identificaron los siguientes resultados:



\### 3.1 Distribución por sexo



\- Hombres: 726 registros.

\- Mujeres: 194 registros.



Se observa una mayor cantidad de registros correspondientes a pacientes masculinos.



\### 3.2 Distribución por edad



\- Edad mínima: 28 años.

\- Edad máxima: 77 años.

\- Edad promedio: aproximadamente 53,5 años.



Esto muestra que la mayoría de la información corresponde a pacientes adultos.



\### 3.3 Procedencia de los registros



La base de datos contiene información de cuatro centros:



\- Cleveland: 304 registros.

\- Hungary: 293 registros.

\- VA Long Beach: 200 registros.

\- Switzerland: 123 registros.



\### 3.4 Distribución de la variable objetivo (num)



La columna `num` permite identificar la presencia y el nivel de diagnóstico de enfermedad cardíaca:



| Valor | Número de registros |

|---|---:|

| 0 | 411 |

| 1 | 265 |

| 2 | 109 |

| 3 | 107 |

| 4 | 28 |

| \*\*Total\*\* | \*\*920\*\* |



En total, 509 registros presentan valores diferentes de cero, mientras que 411 corresponden al valor cero.



\### 3.5 Valores faltantes



Durante la revisión se encontraron datos faltantes en algunas columnas:



| Columna | Valores faltantes |

|---|---:|

| trestbps | 59 |

| chol | 30 |

| fbs | 90 |

| restecg | 2 |

| thalch | 55 |

| exang | 55 |

| oldpeak | 62 |

| slope | 309 |

| ca | 611 |

| thal | 486 |



Las columnas `ca`, `thal` y `slope` presentan una cantidad importante de información faltante. Por esta razón, sería necesario tener especial cuidado al realizar futuros análisis estadísticos o modelos predictivos.



También se identificaron 172 registros con colesterol igual a cero, valor que conviene revisar antes de realizar el análisis definitivo.



\## 4. Importancia en la ingeniería biomédica



Esta base de datos tiene importancia en la ingeniería biomédica porque permite estudiar información clínica relacionada con el funcionamiento del sistema cardiovascular.



Variables como la presión arterial, el colesterol, la frecuencia cardíaca y los resultados del electrocardiograma permiten analizar diferentes características fisiológicas de los pacientes.



Además, el uso de herramientas de análisis de datos puede contribuir al desarrollo de sistemas computacionales que apoyen la investigación y el estudio de enfermedades cardiovasculares.



\## 5. Conclusiones



La base de datos Heart Disease UCI contiene información relevante para el análisis de enfermedades cardiovasculares. Está compuesta por 920 registros y 16 columnas que incluyen características demográficas, mediciones clínicas y resultados relacionados con el diagnóstico cardíaco.



A través del análisis exploratorio se identificó que existe una mayor cantidad de registros masculinos y que 509 registros presentan algún valor positivo en la variable de diagnóstico.



También se encontraron valores faltantes y algunos datos que requieren revisión, por lo que es importante realizar una adecuada preparación de la información antes de desarrollar modelos de análisis o predicción.



Finalmente, este conjunto de datos representa una herramienta útil para aplicar conocimientos de gestión de datos, estadística e ingeniería biomédica en el estudio de información cardiovascular.



\*\*Nota:\*\* Este análisis tiene fines académicos y no constituye una herramienta de diagnóstico médico.

