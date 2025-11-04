Análisis y Predicción del Comportamiento del Conductor (“Driver Score”)


Objetivo:

Analizar registros de viajes de vehículos y construir un modelo predictivo capaz de identificar viajes riesgosos en función de indicadores de conducción como velocidad, aceleración y tiempo de inactividad, 
se realiza en Python utilizando librerías para análisis de datos, visualización y aprendizaje automático, con balanceo de clases y optimización automática de AutoML.

Data principal lectura:  Viajes Mayo BAT (1)
Resultado luego de limpieza: driver_behavior_features.py


Cuerpo:

1. Análisis Exploratorio e Ingeniería de Características

Carga y limpieza de datos:

Se eliminan columnas irrelevantes (rso, TrailerInfo, BatteryEnd, etc.).
Se convierten las variables de tiempo (TotalDrivingTime, TotalIdleTime, etc.) a minutos.

Exploración de variables principales:

Distribuciones de AverageSpeed, MaxSpeed, y TotalDistanceTravelled.
Identificación de patrones de conducción.

Ingeniería de características:

Cálculo de métricas como:

speed_spike: diferencia entre velocidad máxima y promedio.
accel_proxy: proxy de aceleración media.
speed_volatility: variabilidad de velocidad.
smoothness_index: relación entre velocidad promedio y máxima.
active_ratio: proporción de conducción activa frente al tiempo total.
Creación de indicadores de comportamiento:
high_speed_ratio: exceso de velocidad (>80 km/h).
curvy_trip_flag: alta volatilidad de velocidad.
hard_event_flag: eventos bruscos de aceleración/frenado.

Creación de la variable objetivo:

is_risky_trip = (high_speed_ratio == 1) | (curvy_trip_flag == 1) | (hard_event_flag == 1)

Exportación:

Se genera el archivo driver_behavior_features.csv con todas las variables derivadas.


2. Modelo Predictivo ("Driver Score")

Archivo principal: driver_behavior_features.csv o df_model


Preparación de datos:

Selección de variables predictoras (accel_proxy, speed_volatility, smoothness_index).
Imputación de valores faltantes con la mediana.
Balanceo del dataset (submuestreo del grupo mayoritario).
División en conjuntos de entrenamiento (75%) y prueba (25%).

Entrenamiento con AutoML:

Se emplea la librería supervised.automl.AutoML con los algoritmos:
Random Forest, XGBoost, CatBoost, Neural Network

Configuración:

mode="Perform",
ml_task="binary_classification",
eval_metric="f1",
validation_strategy={"validation_type": "kfold", "k_folds": 5}


Evaluación del modelo:

Métricas calculadas: Accuracy, Recall, ROC-AUC
Generación de reporte automático con:  automl.report()


Resultados esperados:

Detección de viajes con comportamiento riesgoso.
Interpretación de variables más influyentes.
Exportación de predicciones y probabilidades de riesgo.

Antes de ejecutar el proyecto, asegúrate de instalar las dependencias necesarias: pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn supervisedy 
o instala los requirements.txt, el .py se ejecuta en la version python 3.12.4

PARA EJECUTAR:
Todo debe estar en el mismo directorio que los scripts, la primera parte genera el archivo driver_behavior_features.csv o df_model
haciendo uso de este entrena el modelo y genera el reporte de resultados.


Resultados:
driver_behavior_features.csv: dataset con variables seleccionadas.
Filter_Model_8 carpeta con el modelo final

Filter_Model_8/: carpeta con modelos entrenados y reportes.

Reporte HTML: interpretaciones automáticas y ranking de variables.
