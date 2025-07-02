# Logistica Inteligente

## Descripción del Proyecto de Machine Learning:

Este proyecto de Machine Learning se centra en el desarrollo de un modelo predictivo para una empresa dedicada al e-commerce y distribución de productos.

El proyecto consiste en construir un modelo de machine learning capaz de predecir si un pedido realizado en una plataforma de e-commerce llegará a tiempo o sufrirá un retraso. Esta predicción busca optimizar los procesos logísticos y reducir los costos asociados a entregas tardías, mejorando la experiencia del cliente y la eficiencia operativa.

Dado que las consecuencias de un falso positivo (predecir retraso cuando no lo hay) y un falso negativo (no detectar un retraso real) pueden afectar de manera distinta al negocio, se ha decidido optimizar la métrica F1, ya que permite equilibrar precisión y exhaustividad en la predicción de entregas con retraso.

## Contexto del problema:

En el sector del e-commerce, la puntualidad en las entregas es un factor clave para la satisfacción del cliente y la optimización logística.
Retrasos frecuentes pueden traducirse en costos adicionales, pérdida de clientes y afectación a la reputación de la empresa.

Por esta razón, contar con un sistema que permita anticipar posibles demoras antes de que ocurran es una herramienta de gran valor para la toma de decisiones.

## Estructrura del repositorio

```python
├── src/                
    ├── data_sample/    
    ├── img/           
    ├── models/         
    ├── notebooks/      
    ├── utils/          
├── main.ipynb          
├── presentacion.pdf    
├── README.md           
```

## Descripción del Proyecto:

El objetivo de este proyecto es desarrollar un modelo de Machine Learning enfocado en la predicción del desempeño logístico de una empresa de e-commerce.

En concreto, se busca:

1. Construir un modelo de clasificación que permita predecir si un pedido llegará a tiempo o sufrirá retrasos, utilizando datos históricos de envíos, características del producto y del cliente.

2. Identificar las variables (features) que tienen mayor impacto en la puntualidad de las entregas, permitiendo a la empresa conocer los principales factores que contribuyen a los retrasos y tomar decisiones estratégicas para mejorar su cadena de suministro.

## Dataset

Para el desarrollo de este proyecto se utilizará un dataset público disponible en la plataforma Kaggle, especializado en registros históricos de envíos de una empresa de e-commerce.

Este conjunto de datos incluye información detallada sobre:

   * ## Características logísticas:

Bloque de almacén desde donde se envía el pedido (Warehouse_block),

Modo de envío (Mode_of_Shipment),

Peso del producto,

Descuentos aplicados (Discount_offered),

Costo del producto (Cost_of_the_Product).

   * ## Datos del cliente:

Número de llamadas a atención al cliente (Customer_care_calls),

Valoración del cliente (Customer_rating),

Género del cliente (Gender).

   * ## Características del producto:

Importancia del producto (Product_importance),

Número de compras previas del cliente (Prior_purchases).

   * ## Variable objetivo (target):

Reached.on.Time_Y.N, que indica si el pedido llegó a tiempo (0) o sufrió retraso (1).

## Fuente del dataset:

El dataset se obtuvo del siguiente enlace de Kaggle:
[enlace](https://www.kaggle.com/datasets/prachi13/customer-analytics)


## Descripción breve de la solución realizada:

El proyecto siguió una metodología completa de Machine Learning supervisado, que incluyó las siguientes etapas:

* Extracción y carga de datos: Importación del dataset relacionado con entregas de e-commerce.

* Exploración e inspección inicial: Revisión de la estructura de los datos, detección de nulos, valores atípicos y análisis básico de las distribuciones.

* Codificación de variables: Transformación de las variables categóricas mediante técnicas como One-Hot Encoding y Ordinal Encoding, según la naturaleza de cada variable.

* Tratamiento de variables numéricas: Aplicación de escalado (StandardScaler) y transformaciones logarítmicas a aquellas features que lo requerían por su dispersión o sesgo.

* División del conjunto de datos: Separación en train y test set, respetando el balance de clases mediante estratificación.

* Mini EDA (Análisis Exploratorio de Datos): Análisis bivariante y pruebas estadísticas (como la prueba de Mann-Whitney U) para validar la relación entre variables predictoras y la variable objetivo.

* Selección de variables: Identificación y selección de las features más relevantes tanto numéricas como categóricas, basándose en importancia estadística y correlación.

* Se aplicó tratamiento específico a las variables: escalado y transformación logarítmica en las numéricas, y codificación mediante One-Hot Encoding y Ordinal Encoding en las categóricas, garantizando así que todas fueran numéricas y aptas para el entrenamiento de modelos de Machine Learning

* Entrenamiento de diferentes modelos: Comparación de algoritmos como Logistic Regression, KNN, Random Forest, LightGBM, XGBoost y Gradient Boosting.

* Optimización de hiperparámetros: Uso de GridSearchCV para afinar parámetros clave en los modelos más prometedores.

* Evaluación y comparación de modelos: Empleo de validación cruzada (5 folds) con la métrica Balanced Accuracy para asegurar un rendimiento equilibrado en presencia de desbalance de clases.

* Selección y validación del modelo final: Elección de Gradient Boosting optimizado como el mejor modelo, evaluado finalmente en el test set con métricas como Accuracy, Recall, Precision, F1 Score, AUC, matriz de confusión y curva ROC.