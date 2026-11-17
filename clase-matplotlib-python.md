Clase: Matplotlib en Python

¿Qué es Matplotlib?

Es una biblioteca de Python que permite crear gráficas y representar datos visualmente.

* plt: permite crear y personalizar gráficas.
* np: permite realizar operaciones numéricas.
* plt.plot(): crea una gráfica de líneas.
* plt.show(): muestra la gráfica.

1. Personalización

* color: cambia el color.
* linestyle: cambia el estilo de línea.
* marker: cambia los marcadores.
* linewidth: cambia el grosor de la línea.

2. Elementos de la gráfica

* plt.title(): agrega un título.
* plt.xlabel(): asigna el nombre del eje X.
* plt.ylabel(): asigna el nombre del eje Y.
* plt.grid(True): agrega una cuadrícula.
* plt.xlim(): establece los límites del eje X.
* plt.ylim(): establece los límites del eje Y.

3. Tipos de gráficas y leyendas

* label: asigna un nombre a las líneas.
* plt.legend(): muestra la leyenda.

4. Subgráficas

* plt.subplot(filas, columnas, posición): permite colocar varias gráficas en una misma figura.

5. Textos y anotaciones

* plt.text(): escribe texto en una coordenada.
* plt.annotate(): señala un punto mediante una anotación o flecha.

6. Tamaño y guardado

* figsize: establece el tamaño de la figura.
* savefig(): guarda la gráfica.
* dpi: establece la resolución de la imagen.

7. Errores comunes

* Los arreglos X e Y deben tener el mismo tamaño.
* Para utilizar leyendas se necesita asignar un label.
* Se recomienda guardar la gráfica antes de utilizar plt.show().
* Utilizar suficientes puntos para obtener curvas suaves.
