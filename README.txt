## Descripción de los datos
Este conjunto de datos contiene información transaccional de compradores frecuentes en una tienda retail. La
La historia de los datos es de 2 años.

## Objetivo del análisis
1. Describir los clientes de la tienda en base a su información transaccional
2. Crear un modelo que nos permita detectar a los clientes que son buenos compradores para ofrecerles descuentos
personalizados.

## Tareas por hacer
1.  Análisis exploratorio de los datos

-  El análisis exploratorio de los datos se encuentra en ambos notebooks.

2. ¿Qué categorías de productos generan aproximadamente el 80% de las ventas? Análisis de PARETO

- Para esta pregunta realize el analisis en el notebook llamado Top_Product_Categories.ipynb

3. Entrenar modelo de ML.

- Para esto use un modelo de clasificación sin supervisión llamada K Means de la librería de Scikit learn. El código
relacionado a la implementación y entrenamiento esta en el notebook llamado custumer_segmenetation_k-means.ipynb

4. Evaluación y explicación de los resultados del modelo.

- Después de haber analizado la data, entrenado el modelo de clasificación de K Means pude evaluar 4 clusters
importantes. Estos clusters los evalúe en base a "elbow method" que construye distancias llamadas centroids en base
de el coeficiente de inercia. En otros casos se podría usar directamente el Euclidean distance que representa la
hipotenusa de un punto en relación con la predicción.

- Estos 4 clusters los podría dividir en 4 categorías de clientes:

* CLUSTER 0: Representa un gran porcentaje de las ventas masivas sin embargo consta con la mayor cantidad de clientes
y tienen un ratio de 1.88 visitas al mes.

* CLUSTER 1: Representa alrededor del 10% de las ventas en revenue sin embargo podemos ver que están más concentrados
en 14 tiendas en específico y tienen una concurrencia más alta en la tienda por lo que una promoción por visitar a
menudo la tienda podría ser la mejor opción.

* CLUSTER 2: representa un volumen más alto de compras y está distribuido en 19 tiendas y tiene una frecuencia de
visita de 3 veces al mes, podemos pensar que no hay riesgo de churn.

* CLUSTER 3: Representa un volumen bajo de ventas sin embargo está relacionado a solo dos clientes que van a dos tiendas
en específico con un ratio de casi 4 veces al mes. Este podría ser el tipo de cliente más valioso que probablemente
esté relacionado con Business-to-business. Se le puede hacer ofertas al por mayor a estos clientes.

En lo personal escogería cuatro nombres para estos clientes y les generaría un label.

5. Sugerencia de posibles desarrollos que se puedan realizar a partir de los datos analizados y de los resultados
obtenidos.

- Respecto a los posibles desarrollos, basándose en el hecho de que el modelo de clasificación que se implementó
genera un label en la columna de cluster, podríamos crear un modelo predictivo supervisado usando estos valores. De
esta manera poder generar un score de cliente y de esta manera predecir qué tipo de cliente es y tener una mejor
precisión en la siguiente mejor oferta. Para esto pensé utilizar el modelo de XGBoost sin embargo opte por inicialmente
usar un modelo de clasificación ya que la data que tengo es muy poca y mi modelo carecería de precisión. Por otro lado
no tengo data nueva para probar la inferencia.

- En lo personal para poner a productivo este modelo construirá un webservice que pase la data através de un API y
retorne los scores de la misma manera.

