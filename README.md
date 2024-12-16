# Grupo MasAvocadosNo

Jose Niguidula

## Repositorio github: [https://github.com/jniguidula/uoc-proyecto3](https://github.com/jniguidula/uoc-proyecto3)

## Proyecto github: [https://github.com/users/jniguidula/projects/1](https://github.com/users/jniguidula/projects/1)

# Proyecto Final - Análisis de Datos Avanzado

Opción de continuar y ampliar el **"proyecto-1-regresion"**.

*   creación de repositorio en github como repositorio de código, archivos y control de versiones.
*   branch 'main' como unica rama al optar por trabajar en solitario
*   creación de un proyecto github 'uoc-proyecto3' como herramienta de planificación.
    *   creación de tareas como 'backlog' siguiendo los requisitos obligatorios del proyecto.
    *   asignación y cambios de estado de las tareas, creación de 'issues' para poder ligar la tarea con el repositorio github.
    *   actualizacion de fechas de inicio y fin de las tareas y prioridad.
    *   definición de tareas gestionables con sprints de 1 semana con la finalidad de hacer entregas parciales pero tangibles en modo agile.

![GitHub Project](./files/Github-project.png)

*   Para ampliar la CSV del proyecto 1, utilizamos un dataset de kaggle.com con información de Hass Avocados de 2015 hasta 2023 para ampliar el  proyecto-1
    *   [https://www.kaggle.com/datasets/vakhariapujan/avocado-prices-and-sales-volume-2015-2023](https://www.kaggle.com/datasets/vakhariapujan/avocado-prices-and-sales-volume-2015-2023)

## Objetivo del proyecto

1.  Ampliar la exploración y analisis de datos el proyecto-1 con datos actualizados hasta diciembre 2023.
2.  Verificar

**Informe del Análisis Exploratorio de Datos (EDA) y Calidad de los Datos**:

*   Un informe en formato markdown que resuma los hallazgos clave del análisis exploratorio.
*   Incluir visualizaciones de los patrones encontrados y explicaciones claras sobre las conclusiones obtenidas.
*   Un informe detallado sobre la calidad de los datos, incluyendo los problemas identificados y las acciones tomadas para mejorarlos (tratamiento de valores faltantes, inconsistencias, etc.).
*   el archivo csv actualizado incluye datos hasta 2023 y las caracteristicas son parecidas al csv del proyecto 1:

![dataframe](./files/avocado-dataframe.png)

*   faltaba la columna 'year' y procedimos a crear la nueva columna.
*   regularizamos la columna 'Date' para poder tratarlo en python
*   Tenemos mas valores en 'region' y hemos actualizado la clasificación de 'region\_type' para incluir los nuevo regions:

```
region_classification = {
    'Albany': 'City',
    'Atlanta': 'City',
    'BaltimoreWashington': 'Region',
    'BirminghamMontgomery': 'Region',
    'Boise': 'City',
    'Boston': 'City',
    'BuffaloRochester': 'Region',
    'California': 'GreaterRegion',
    'Charlotte': 'City',
    'Chicago': 'City',
    'CincinnatiDayton': 'Region',
    'Columbus': 'City',
    'DallasFtWorth': 'Region',
    'Denver': 'City',
    'Detroit': 'City',
    'GrandRapids': 'City',
    'GreatLakes': 'GreaterRegion',
    'HarrisburgScranton': 'Region',
    'HartfordSpringfield': 'Region',
    'Houston': 'City',
    'Indianapolis': 'City',
    'Jacksonville': 'City',
    'LasVegas': 'City',
    'LosAngeles': 'City',
    'Louisville': 'City',
    'Miami': 'City',
    'MiamiFtLauderdale': 'Region',
    'Midsouth': 'GreaterRegion',
    'Nashville': 'City',
    'NewOrleans': 'City',
    'NewYork': 'City',
    'Northeast': 'GreaterRegion',
    'NorthernNewEngland': 'Region',
    'Orlando': 'City',
    'PeoriaSpringfield': 'Region',
    'Philadelphia': 'City',
    'PhoenixTucson': 'Region',
    'Pittsburgh': 'City',
    'Plains': 'GreaterRegion',
    'Portland': 'City',
    'Providence': 'City',
    'RaleighGreensboro': 'Region',
    'RichmondNorfolk': 'Region',
    'Roanoke': 'City',
    'Sacramento': 'City',
    'SanDiego': 'City',
    'SanFrancisco': 'City',
    'Seattle': 'City',
    'SouthCarolina': 'Region',
    'SouthCentral': 'GreaterRegion',
    'Southeast': 'GreaterRegion',
    'Spokane': 'City',
    'StLouis': 'City',
    'Syracuse': 'City',
    'Tampa': 'City',
    'Toledo': 'City',
    'TotalUS': 'TotalUS',
    'West': 'GreaterRegion',
    'WestTexNewMexico': 'Region',
    'Wichita': 'City'
}
```

*   la diferencia de tener mas regiones con los datos actualizados

![diff](./files/diff-regions.png)

*   el dataset actualizado tiene 53.415 filas versus los 18.250 del proyecto 1.
*   para verificar que los datos originales no difieren con los datos actualizados hasta la fecha final del proyecto 1:

1.  contamos las filas del csv actualizado hasta la ultima fecha del proyecto 1 que era del 2018-03-25: 18.360 filas, puesto que habia unos regionas nuevos.
2.  comparamos la evolución del 'AveragePrice' y vemos que el gráfico sigue el mismo patron.

![Average Price 1](./files/average-price1.png)

![Average Price 2](./files/average-price2.png)


**Modelos Predictivos**:

*   Los modelos de regresión regularizados y clasificación deben estar bien optimizados.
*   Incluir la búsqueda de hiperparámetros para obtener el mejor rendimiento.
*   Presentar los resultados de la validación cruzada (k-fold) y realizar un análisis de los residuos.

**Presentación Ejecutiva**:

*   Un informe conciso que resuma los hallazgos clave, análisis realizados, y los modelos implementados.
*   Este resumen debe estar incluido en el archivo `README.md` del repositorio de GitHub y será la única parte utilizada durante las exposiciones para defender el proyecto