# ML_precipitacion

Desarrollo y evaluación en lenguaje Python de modelos de machine learning de pronóstico de precipitación diaria a corto plazo en Guatemala. Los archivos de código son cuadernos de Jupyter Notebook.

# Preprocesamiento

En esta carpeta se presenta el procedimiento realizado durante el preprocesamiento de datos. Se rellenan valores vacíos, se construyen las variables objetivo, se calculan los datos de la Climatología (promedio y percentiles de precipitación), y, en general, se construye una base de datos adecuada para el desarrollo de los modelos. En un segundo archivo, esta base de datos es separada en dos partes: 80% para datos de entrenamiento y 20% para datos de evaluación.

# Desarrollo_Modelos

Se incluye el código de desarrollo y evaluación de los modelos. El nombre de cada subcarpeta indica la variable objetivo de los modelos que contiene. Se presenta un archivo por cada uno de los algoritmos implementados. Se importan los datos obtenidos luego del preprocesamiento, y se procede al entrenamiento y posterior evaluación del modelo. En cada archivo se entrenan tres modelos: uno con datos del año completo, uno con datos de la época lluviosa y uno con datos de la época seca. Cada uno de estos tres modelos es, a su vez, evaluado con datos de cada uno de estos tres períodos.

# Evaluacion_WRF

# Evaluacion_NextGen

# NOTAS
