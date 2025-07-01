# Logistica Inteligente

## Descripción del Proyecto de Machine Learning:

Este proyecto de Machine Learning se centra en el desarrollo de un modelo predictivo para una empresa dedicada al e-commerce y distribución de productos.

El objetivo principal es predecir con anticipación si un pedido llegará a tiempo o sufrirá retrasos, utilizando información histórica de los envíos.

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