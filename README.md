<h1 align="center"> Test A/A/B para una empresa de venta de productos alimenticios 🍎  </h1>

## Descripción
***
En este proyecto se trabaja en una empresa emergente que vende productos alimenticios. El objetivo principal es investigar el comportamiento del usuario para la aplicación de la empresa.
Primero, se estudia el embudo de ventas. Descubriendo cómo los usuarios y las usuarias llegan a la etapa de compra. ¿Cuántos usuarios o usuarias realmente llegan a esta etapa? ¿Cuántos se atascan en etapas anteriores? ¿Qué etapas en particular?
Luego, se observan los resultados de un test A/A/B. 

Este contexto se da ya que al equipo de diseño le gustaría cambiar las fuentes de toda la aplicación, pero la gerencia teme que los usuarios y las usuarias piensen que el nuevo diseño es inadecuado y abandonen la aplicación. 
Los usuarios se dividen en tres grupos: dos grupos de control obtienen las fuentes antiguas y un grupo de prueba obtiene las nuevas. 

Se utilizará el mismo dataset para el análisis general y para el análisis A/A/B, cuyos datos son los siguientes: 

## Descripción de los datos
Cada entrada de registro es una acción de usuario o un evento.
*	EventName: nombre del evento.
*	DeviceIDHash: identificador de usuario unívoco.
*	EventTimestamp: hora del evento.
*	ExpId: número de experimento: 246 y 247 son los grupos de control, 248 es el grupo de prueba.

![Muestra de los datos](https://github.com/user-attachments/assets/d39c0a53-e91c-401e-914f-6d43f4f4a7d7)


## Tareas 

### 1. Preparar los datos para el análisis
* Cambiamos el nombre de las columnas de manera que sea conveniente para ti
* Corregimos los tipos de datos, así como valores ausentes y/o duplicados 
* Agregamos una columna de fecha y hora y una columna separada para las fechas
  
### 1. Estudiar y comprobar los datos
Para realizar esta tarea buscaremos respuesta a las siguientes preguntas: 
* ¿Cuántos eventos hay en los registros?
* ¿Cuántos usuarios y usuarias hay en los registros?
* ¿Cuál es el promedio de eventos por usuario?
* ¿Qué periodo de tiempo cubren los datos?
* ¿Podemos tener seguridad de que hay datos igualmente completos para todo el periodo?
 * ¿Qué periodo representan realmente los datos?
* ¿Perdimos muchos eventos y usuarios al excluir los datos más antiguos?
  
### 3. Estudiar el embudo de eventos
Observaremos qué eventos hay en los registros y su frecuencia de suceso. 
Encontramos la cantidad de usuarios y usuarias que realizaron cada una de estas acciones. 
Después ordenamos los eventos por el número de usuarios y usuarias. 
Finalmente calculamos la proporción de usuarios y usuarias que realizaron la acción al menos una vez. 
Una vez tenemos estos insights, se responden las siguientes preguntas:
* ¿En qué orden crees que ocurrieron las acciones? 
* ¿Cuál es la proporción de usuarios y usuarias que pasan de una etapa a la siguiente? (Por ejemplo, para la secuencia de eventos A → B → C, se calcula la proporción de usuarios en la etapa B a la cantidad de usuarios en la etapa A y la proporción de usuarios en la etapa C a la cantidad en la etapa B).
* ¿En qué etapa se pierden más usuarios y usuarias?
* ¿Qué porcentaje de usuarios y usuarias hace todo el viaje desde su primer evento hasta el pago?
### 4. Estudiar los resultados del experimento
Tenemos dos grupos de control en el test A/A, donde comprobamos nuestros mecanismos y cálculos. Observaremos primero si hay una diferencia estadísticamente significativa entre las muestras 246 y 247.

Seleccionamos el evento más popular. En cada uno de los grupos de control, encontramos la cantidad y proporción de usuarios y usuarias que realizaron esta acción. 
Comprobamos si la diferencia entre los grupos es estadísticamente significativa y se repite el procedimiento para todos los demás eventos 

Haremos lo mismo para el grupo con fuentes alteradas, comparando los resultados con los de cada uno de los grupos de control para cada evento de forma aislada. 
Finalmente comparamos los resultados con los resultados combinados de los grupos de control.



## Tecnologías
***
Los recursos utilizados en este proyecto son:
* Librerías de Python 
	* Pandas 
	* Numpy
	* Matplotlib
	* Seaborn
	* Scipy stats
  * Plotly

* Jupyter Notebooks

Utilizamos Pandas y Numpy principalmente para la limpieza y preparación de los datos, utilizamos Matplotlib y Seaborn para visualizar las estadísticas adecuadas sobre todo aquellas que indican la distribución de los datos, en el caso de la visualización de embudos al requerir gráficas más interactivas usamos la librería Plotly. 
Finalmente para el análisis estadístico y pruebas de hipótesis se usó la librería de Scipy stats

## Uso del código 
Todos los bloques de código se encuentran en el archivo .ipynb y el set de datos en el arhivo .csv. Para utilizarlo descargar los archivos csv, copie el cuaderno y ejecute los bloques de código.

