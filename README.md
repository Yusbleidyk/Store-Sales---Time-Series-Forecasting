# 📈 Predicción de Ventas - Corporación Favorita (Kaggle)

Este proyecto participa en la competencia de Kaggle **"Store Sales - Time Series Forecasting"**, cuyo objetivo es predecir las ventas unitarias de productos en distintas tiendas de la cadena ecuatoriana **Corporación Favorita**.

## 🧠 Objetivo

Desarrollar un modelo de aprendizaje automático que prediga con precisión las ventas futuras de productos, utilizando datos históricos de ventas, promociones, tiendas, productos y otras variables relevantes.

## 🗂️ Descripción del Dataset

El conjunto de datos incluye información de ventas históricas, promociones, tiendas, productos, precios del petróleo y eventos especiales. A continuación se describen los archivos disponibles:

### `train.csv`
- Contiene las series temporales de ventas históricas.
- Columnas:
  - `date`: Fecha de la observación.
  - `store_nbr`: Identificador de la tienda.
  - `family`: Categoría del producto.
  - `sales`: Ventas totales (pueden ser fraccionarias).
  - `onpromotion`: Número de productos en promoción.

### `test.csv`
- Datos para los que se deben predecir las ventas.
- Contiene las mismas columnas que `train.csv` excepto `sales`.

### `stores.csv`
- Información adicional sobre las tiendas:
  - `city`, `state`, `type`, `cluster`.

### `oil.csv`
- Precio diario del petróleo, relevante para la economía de Ecuador.

### `holidays_events.csv`
- Información sobre feriados y eventos especiales.
- Columnas importantes:
  - `type`, `locale`, `transferred`, `description`.
- Notas:
  - Los feriados transferidos deben tratarse como días normales.
  - Los días tipo `Bridge` y `Work Day` modifican el comportamiento de las ventas.

## 📝 Notas Adicionales

- Los salarios del sector público se pagan el día 15 y el último día del mes, lo cual puede influir en las ventas.
- Un terremoto de magnitud 7.8 ocurrió el 16 de abril de 2016, afectando significativamente las ventas durante varias semanas.

## 📊 Evaluación

La métrica utilizada es **Root Mean Squared Logarithmic Error (RMSLE)**, que penaliza más los errores en valores pequeños y es adecuada para datos de ventas.

