# Aprendizaje Automático: Regresión Lineal

## Predicción de Ventas del Black Friday

## Descripción

Proyecto de aprendizaje automático desarrollado en Python para predecir el monto de compra de los clientes durante el Black Friday en una tienda minorista de Estados Unidos.

El trabajo utiliza un conjunto de datos de transacciones comerciales y aplica técnicas de exploración, ingeniería de características y modelado para construir un modelo de regresión lineal. El objetivo es estimar el valor de una compra a partir de características relacionadas con los clientes y los productos.

## Objetivos

- Explorar y comprender la estructura del conjunto de datos.
- Identificar valores nulos, duplicados y tipos de datos.
- Seleccionar las variables relevantes para el análisis.
- Aplicar técnicas de ingeniería de características (*Feature Engineering*).
- Transformar variables categóricas para utilizarlas en el modelo.
- Entrenar un modelo de regresión lineal utilizando Scikit-Learn.
- Generar predicciones del monto de compra.
- Evaluar el rendimiento del modelo mediante la métrica RMSE.

## Dataset

El proyecto utiliza el archivo `BlackFriday.csv`, que contiene una muestra de transacciones realizadas durante el Black Friday.

Los datos se descargan desde el repositorio público de [AnyoneAI](https://github.com/anyoneai/notebooks).

### Variables utilizadas

| **Columna** | **Descripción** |
|---|---|
| `Gender` | Género del cliente. |
| `Age` | Rango de edad del cliente. |
| `Occupation` | Código de ocupación del cliente. |
| `City_Category` | Categoría de la ciudad donde reside el cliente. |
| `Stay_In_Current_City_Years` | Años de permanencia del cliente en su ciudad actual. |
| `Marital_Status` | Estado civil del cliente. |
| `Product_Category_1` | Primera categoría del producto. |
| `Product_Category_2` | Segunda categoría del producto, cuando está disponible. |
| `Product_Category_3` | Tercera categoría del producto, cuando está disponible. |
| `Purchase` | Monto de la compra; variable objetivo que se busca predecir. |

## Tecnologías utilizadas

- **Python:** desarrollo y ejecución del análisis.
- **Pandas:** carga, exploración y transformación de los datos.
- **NumPy:** operaciones numéricas y cálculo de métricas.
- **Matplotlib:** herramientas para la visualización de datos.
- **Seaborn:** herramientas para la exploración y visualización estadística.
- **Scikit-Learn:** entrenamiento del modelo de regresión lineal y evaluación de sus predicciones.
- **Google Colab:** entorno de desarrollo y ejecución del notebook.

## Metodología

1. **Exploración de datos:** carga del conjunto de datos, inspección de columnas, tipos de datos, valores nulos, valores únicos y duplicados.
2. **Selección de variables:** conservación de las columnas relevantes para predecir el monto de compra.
3. **Tratamiento de valores nulos:** reemplazo por cero de los valores faltantes en `Product_Category_2` y `Product_Category_3`.
4. **Ingeniería de características:** transformación de las variables `Gender` y `City_Category` mediante variables indicadoras (*One-Hot Encoding*), asignación de valores representativos a los rangos de edad y conversión de `4+` a `5` en los años de permanencia en la ciudad.
5. **Creación de una característica:** incorporación de `num_categorias`, que representa la cantidad de categorías de producto registradas para cada compra.
6. **Modelado:** separación de los datos en conjuntos de entrenamiento (80 %) y prueba (20 %), y entrenamiento de un modelo de regresión lineal.
7. **Predicción:** estimación del monto de compra para los registros del conjunto de prueba y comparación de una predicción individual con su valor real.
8. **Evaluación:** cálculo del error cuadrático medio de la raíz (RMSE) para analizar la diferencia entre los montos reales y los predichos.

## Resultados del análisis

### Modelo de regresión lineal

| **Indicador** | **Resultado** |
|---|---|
| Variable objetivo | `Purchase` |
| Proporción de entrenamiento | 80 % |
| Proporción de prueba | 20 % |
| Modelo utilizado | `LinearRegression` de Scikit-Learn |
| Métrica de evaluación | RMSE |
| RMSE aproximado | 4620 unidades monetarias |

El error RMSE obtenido es de aproximadamente 4620 unidades monetarias, según la interpretación incluida en el notebook. Esto representa una referencia del tamaño del error de predicción del modelo, expresado en la misma unidad que el monto de compra.

Para valorar adecuadamente su rendimiento, este error debe interpretarse en relación con la distribución y la escala de los montos de compra.

## Cómo ejecutar el proyecto

1. Abrir el notebook en Google Colab.
2. Ejecutar las celdas en orden.
3. Verificar que el archivo CSV se cargue correctamente desde la fuente pública.
4. Consultar la exploración y las transformaciones realizadas sobre los datos.
5. Ejecutar el entrenamiento del modelo y revisar las predicciones y la métrica de evaluación.

El notebook descarga automáticamente el conjunto de datos desde la siguiente dirección:

`https://raw.githubusercontent.com/anyoneai/notebooks/main/datasets/BlackFriday.csv`

## Estado del proyecto

Proyecto práctico de aprendizaje automático enfocado en la predicción de montos de compra mediante regresión lineal, aplicando técnicas de exploración de datos, ingeniería de características, modelado y evaluación.

