# Clustering-Clientes-de-Banco
El Dataset proporcionado pertenece a la base de datos de clientes de un banco. El departamento de Marketing esta buscando una forma de segmentar su base de clientes para la realización de campañas dirigidas.  

Para la realización del clasificador se ha utilizado el lenguaje de programación **Python** junto a las librerias **Pandas**, **NumPy**, **Seaborn**, **Matplotlib**, **Sklearn** y **TensorFlow**.

El entorno de desarrollo utilizado ha sido **Google Colab**.

Dataset: https://www.kaggle.com/datasets/arjunbhasin2013/ccdata

## Método de clustering utilizado

**K-MEANS**

## Método para la reducción de características

**PCA**

**Autoencoders**

## Metodología utilizada

El primer paso que se ha dado ha sido el análisis del conjunto de datos. Se ha realizado una búsqueda de valores nulos, y se han rellenado utilizando el valor medio de la característica donde se encontraba. 

Una vez realizado la corrección del dataset, se ha combinado la gráfica de densidad de cada característica con los histogramas, para la búsqueda de tendencias claras en el conjunto de datos. También se ha realizado una matriz de correlación y se ha mostrado en forma de mapa de calor.

Tras toda la corrección y visualización de los datos, se ha empezado a buscar cual es el número óptimo de segmentaciones. Para ello, primero hemos tenido que escalar los datos, ya que la diferencia de escalas entre características era muy notable. Como en la tarea no se nos pedía un número mínimo ni máximo, se ha cogido un valor medio según el método del codo, ya que en el dataset podemos encontrar dos codos a la hora de hacer el K-MEANS con diferentes k.  

Teniendo el número de k, se ha realizado el K-MEANS, mostrando un histograma por cada característica y por cada segmento para encontrar las características que destaca en cada grupo. Las graficas han sido realizadas con los datos iniciales, no con los escalado.

Observando estos resultados se puede observar como el grupo de clientes 6 es el que más dinero dispones y más dinero prestado pide, mientras que el grupo 1 es el que menos dinero dispone en la cuenta, menos ingresos tiene y pide muy poco dinero prestado.

Tras todo esto se ha representado en una nube de puntos los clústeres con diferentes colores, tras ser pasado los datos por un **PCA** para poder mostrarse en 2 dimensiones.

Para mejorar el sistema obtenido hasta ahora, se ha querido realizar el mismo procedimiento anterior, pero disminuyendo el conjunto de características mediante una red neuronal **Autoencoders** realizado mediante **TensorFlow** para posteriormente pasar la salida al K-MEANS. Tras este procedimiento se ha utilizado de nuevo el PCA para representar los nuevos segmentos en 2 dimensiones.
