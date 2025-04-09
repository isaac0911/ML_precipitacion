# ML_precipitacion

Desarrollo y evaluación en lenguaje Python de modelos de machine learning de pronóstico de precipitación diaria a corto plazo en Guatemala. Los archivos de código son cuadernos de Jupyter Notebook.

El repositorio se compone de 4 carpetas principales y que constituyen una clasificación general del procedimiento experimental: Preprocesamiento, Desarrollo_Modelos, Evaluacion_WRF y Evaluacion_NextGen. A continuación se presenta una descripción del contenido de cada una.

# Preprocesamiento

En esta carpeta se presenta el procedimiento realizado durante el preprocesamiento de datos. Se rellenan valores vacíos, se construyen las variables objetivo, se calculan los datos de la Climatología (promedio y percentiles de precipitación), y, en general, se construye una base de datos adecuada para el desarrollo de los modelos. En un segundo archivo, esta base de datos es separada en dos partes: 80% para datos de entrenamiento y 20% para datos de evaluación.

# Desarrollo_Modelos

Se incluye el código de desarrollo y evaluación de los modelos. El nombre de cada subcarpeta indica la variable objetivo de los modelos que contiene. Se presenta un archivo por cada uno de los algoritmos implementados. El código consiste en entrenar el modelo con los datos obtenidos luego del preprocesamiento, para luego proceder con su evaluación. En cada archivo se entrenan tres modelos: uno con datos del año completo, uno con datos de la época lluviosa y uno con datos de la época seca; cada uno de los tres modelos es evaluado con datos de los tres períodos, de forma que en cada archivo de código se realizan 9 evaluaciones (3 entrenamientos x 3 evaluaciones).

# Evaluacion_WRF

En esta carpeta se halla el código de evaluación del modelo WRF-BMJ-GFS. El procedimiento se desglosa en varios pasos; se presenta un archivo de código por cada paso. Primero, se construyen los pronósticos a partir de los archivos rasterizados proporcionados por el modelo; en segundo lugar, se construyen los valores reales utilizando los registros de INSIVUMEH. Luego, las instancias son separadas en cada uno de los tres tipos de evaluación (general, lluviosa y seca). Finalmente, en el cuarto y último paso, se realiza la evaluación del modelo mediante el cálculo de las métricas de evaluación. Para los modelos de clasificación, el código proporciona la matriz de confusión, la cual es transcrita a un archivo de Excel para el posterior cálculo de la exactitud y demás métricas.

# Evaluacion_NextGen

Se presentan los pasos seguidos para la evaluación del modelo NextGen. Los pasos son exactamente los mismos que se describen para el modelo WRF, con la diferencia de que en este caso se incluye un primera paso adicional. Este paso consiste en obtener la Climatología (promedio y percentiles) de la precipitación acumulada por período estacional, a partir de la base de datos meteorológicos. El modelo NextGen es evaluado únicamente en el pronóstico de Cotas Percentiles, por los motivos expuestos en el informe.

# NOTAS

En este repositorio se encuentra únicamente el código de programación. Debido a las políticas de protección de datos del INSIVUMEH, no es posible proporcionar la base de datos meteorológicos utilizada para el entrenamiento y evaluación de los modelos.

-------------------------------------------------

Autor: Isaac Solórzano Quintana

Correo: sol21765@uvg.edu.gt
