# Análisis y Predicción de la Calidad del Aire en Palma de Mallorca

## Introducción

Este proyecto tiene como objetivo analizar y predecir la calidad del aire en Palma de Mallorca, utilizando datos provenientes de dos estaciones de monitoreo del **Govern de les Illes Balears**:

1. **Estación Bellver**: Ubicada en el parque de Bellver, en un entorno natural y cerca del puerto.
2. **Estación Foners**: Situada en el centro de la ciudad, en una zona con alta actividad urbana y tráfico.

El análisis y las predicciones se realizan a partir de datos históricos de varios años, midiendo gases como el dióxido de azufre (SO₂), los óxidos de nitrógeno (NO y NO₂), ozono (O₃) y partículas PM10. Las unidades de medida son **microgramos por metro cúbico (µg/m³)**.

---

## Objetivos del Proyecto

1. **Análisis Exploratorio de Datos**:
   - Identificar patrones estacionales e interanuales en los niveles de contaminación.
   - Visualizar las diferencias geográficas entre las estaciones de Bellver y Foners.

2. **Predicciones con Modelos Avanzados**:
   - Utilizar técnicas de aprendizaje supervisado, deep learning y modelos estadísticos para predecir los niveles de contaminantes.
   - Comparar la precisión y desempeño de diferentes enfoques.

4. **Aplicaciones Estratégicas**:
   - Proveer insights relevantes para la toma de decisiones en empresas y gobiernos, promoviendo iniciativas de responsabilidad social corporativa (RSC).

---

## Metodología

1. **Preparación de Datos**:
   - Se trabajó inicialmente con las columnas comunes entre las dos estaciones.
   - Se imputaron datos faltantes utilizando el método **forward fill** y se eliminaron las columnas de validación para evitar confusiones.
   - Los nombres de las columnas se ajustaron para reflejar claramente los significados de los datos.

2. **Intentos de Predicción**:
   Se probaron diversos enfoques para modelar y predecir la calidad del aire:
   - **Deep Learning**: LSTM, GRU, Transformer con PyTorch.
   - **Machine Learning Supervisado**: MultiOutputRegressor, Random Forest Regressor.
   - **Foundation Models**: Prophet.
   - **Workflows de Auto ML**: PyCaret.
   - **Modelos Estadísticos**: ARIMA, SARIMA.

   Tras integrar 10 años de datos históricos, las predicciones de **Prophet** resultaron ser las más precisas e interesantes.

3. **Visualización y Análisis**:
   - Se utilizaron librerías como **Seaborn** para identificar patrones estacionales e interanuales.
   - Los contaminantes se analizaron a nivel geográfico y temporal, destacando diferencias clave entre las estaciones.

---

## Conclusiones Principales

1. **Sobre los Contaminantes**:
   - **Bellver** registra niveles altos de SO₂ debido a su proximidad al puerto y carreteras principales, mientras que **Foners** tiene mayores niveles de NO y PM10 por el tráfico urbano.
   - El ozono alcanza sus picos durante el verano, influenciado por la radiación solar.

2. **Complejidad de los Patrones**:
   - Los datos muestran alta variabilidad interanual y patrones estacionales claros.
   - La presencia de outliers y alta varianza en las mediciones complica los análisis y predicciones.

3. **Desempeño en la Predicción**:
   - Los modelos clásicos de aprendizaje supervisado y deep learning ofrecieron resultados limitados, con métricas como R² negativas.
   - Prophet, un modelo estadístico especializado en series temporales, mostró los mejores resultados tras integrar 10 años de datos históricos.

4. **Aplicaciones Estratégicas**:
   - Los insights obtenidos pueden ser útiles para diseñar estrategias de mitigación de contaminación y políticas públicas.
   - Las empresas podrían utilizar esta información para iniciativas de RSC, como reducir emisiones o adoptar tecnologías más limpias.

---

## Próximos Pasos

1. **Incorporar Factores Externos**:
   - Añadir datos meteorológicos, tráfico marítimo y urbano para enriquecer las predicciones.

2. **Explorar Nuevos Modelos**:
   - Probar arquitecturas de deep learning específicas para series temporales, como TCN (Temporal Convolutional Networks).
   - Investigar enfoques híbridos que combinen modelos estadísticos y machine learning.

3. **Publicación de Resultados**:
   - Hacer accesibles las predicciones y visualizaciones mediante dashboards interactivos para usuarios no técnicos.

---

## Código y Recursos

El notebook se encuentra en el pryecto y el código adicional de los modelos de deep learning en el siguiente Colab de experiemntos y pruebas. 

[Google Colab Notebook](https://colab.research.google.com/drive/1AEBeHzZZPbCc41pmV1_vXBBvvms1tv12?authuser=0#scrollTo=m65_vcW9Af-G)

---

Este proyecto proporciona una base sólida para comprender mejor los factores que afectan la calidad del aire en Palma de Mallorca, con aplicaciones potenciales en el ámbito ambiental, social y económico.
