# Modelos de clustering

Verás que en algunos de los modelos que subí los datasets los he importada de la misma librería Sklearn, tomemos de ejemplo el archivo de KMeans (vinos)

```sh
from sklearn import datasets
X_wine, Y_wine = datasets.load_wine(return_X_y=True, as_frame = True)
```
Puedes revisar la documentación de sklearn para cargar más datasets de tu interés aquí: `https://scikit-learn.org/stable/datasets/toy_dataset.html`

KMeans es un algoritmo de clustering no supervisado que agrupa un conjunto de datos en K clusters diferentes, donde cada punto de datos pertenece a un cluster cercano al centroide del cluster.

* Ten en cuenta que el número de clusters puede ir variando, eso nos corresponde establecerlo de acuerdo como va actuando nuestras métricas y gráficas.

* En cada iteración, el algoritmo KMeans actualiza los centroides de los clusters como el promedio de los puntos de datos asignados a cada centroide. y reasigna cada punto de datos al cluster más cercano. El objetivo del algoritmo es minimizar la suma de las distancias al cuadrado entre cada punto de datos y el centroide del cluster correspondiente.

* Se repite los pasos 2 y 3 hasta que la asignación de los puntos de datos a los centroides no cambie o hasta que se alcance un número máximo de iteraciones.

En el siguiente código puedes ir cambiando la cantidad de clusters como también el máximo de iteraciones

`model = KMeans(n_clusters = 3,max_iter = 2000)`

La elección del número de iteraciones puede afectar el rendimiento y la calidad del modelo generado por KMeans. En general, si se elige un número bajo de iteraciones, el modelo puede no converger correctamente y los resultados pueden no ser óptimos. Si se elige un número muy alto de iteraciones, el modelo puede tardar más en ajustarse y puede ser propenso al sobreajuste (overfitting). 
