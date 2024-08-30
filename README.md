<h1 align="center"> Test A/A/B para una empresa de venta de productos alimenticios  </h1>

## Descripción
***
En este proyecto se trabaja en una empresa emergente que vende productos alimenticios. El objetivo principal es investigar el comportamiento del usuario para la aplicación de la empresa.
Primero, se estudia el embudo de ventas. Descubriendo cómo los usuarios y las usuarias llegan a la etapa de compra. ¿Cuántos usuarios o usuarias realmente llegan a esta etapa? ¿Cuántos se atascan en etapas anteriores? ¿Qué etapas en particular?
Luego, se observan los resultados de un test A/A/B. 

Este contexto se da ya que al equipo de diseño le gustaría cambiar las fuentes de toda la aplicación, pero la gerencia teme que los usuarios y las usuarias piensen que el nuevo diseño es inadecuado y abandonen la aplicación. 
Los usuarios se dividen en tres grupos: dos grupos de control obtienen las fuentes antiguas y un grupo de prueba obtiene las nuevas. 

Se utilizará el mismo dataset para el análisis general y para el análisis A/A/B, cuyos datos son los siguientes: 

#### Descripción de los datos
Cada entrada de registro es una acción de usuario o un evento.
*	EventName: nombre del evento.
*	DeviceIDHash: identificador de usuario unívoco.
*	EventTimestamp: hora del evento.
*	ExpId: número de experimento: 246 y 247 son los grupos de control, 248 es el grupo de prueba.


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
