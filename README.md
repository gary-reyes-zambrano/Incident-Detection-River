# Incident-Detection-River
Analisis Inteligente de incidentes de tráfico usando Online Machine Learning (ARF &amp; DenStream) y datos simulados de Twitter/X.

## Entorno de Ejecución

Este proyecto fue desarrollado y ejecutado en el entorno de **Google Colab**,
lo que permite trabajar fácilmente con flujos de datos y librerías de
aprendizaje automático en línea.

Por esta razón, la notebook incluye comandos de instalación de librerías
mediante `pip` y utiliza rutas propias del entorno Colab (por ejemplo,
`/content/`).

## Dependencias
Opcionalmente, las dependencias del proyecto se encuentran listadas en el
archivo `requirements.txt` para su ejecución en entornos distintos a Google
Colab.

# Incident-Detection-River

Sistema experimental para la detección de incidentes de tráfico utilizando
aprendizaje automático en línea (Online Machine Learning) a partir de flujos
de datos simulados basados en reportes de redes sociales (Twitter/X).

El proyecto implementa un mismo flujo de procesamiento y modelado para
diferentes escenarios urbanos, empleando los algoritmos Adaptive Random Forest
(ARF) y DenStream.

---

## Objetivo del Proyecto

Evaluar el comportamiento de modelos de aprendizaje en línea para la detección
de incidentes de tráfico en tiempo real, utilizando datasets simulados de
diferentes ciudades bajo un mismo pipeline experimental.

---

## Algoritmos Utilizados

- **Adaptive Random Forest (ARF)**  
  Clasificación en flujo de datos y detección de cambios conceptuales.

- **DenStream**  
  Agrupamiento incremental para la identificación de patrones emergentes en
  flujos de datos.

---

## Datasets Utilizados

Se emplean **datasets simulados**, diseñados para representar reportes de
tráfico provenientes de redes sociales en dos contextos urbanos distintos:

- **Guayaquil (Ecuador):**  
  `reportes_guayaquil_balanceado_final.csv`

- **Panamá:**  
  `reportes_panama_simulados.csv`

Ambos datasets poseen la **misma estructura**, permitiendo ejecutar el mismo
flujo de procesamiento sin modificaciones adicionales en el código. Fueron basados en datasets reales.

---

## Flujo Experimental

El pipeline experimental incluye:

1. Carga del flujo de datos.
2. Preprocesamiento de características.
3. Clasificación incremental con Adaptive Random Forest.
4. Agrupamiento en línea con DenStream.
5. Análisis de los resultados obtenidos.

---

##  Ejecución del Proyecto

El experimento se ejecuta desde el notebook ubicado en la carpeta
`notebooks/`.

### Selección del Dataset

Para cambiar el dataset a utilizar, **solo es necesario modificar la línea de
carga del archivo** en el notebook:

```python
df = pd.read_csv("/content/reportes_guayaquil_balanceado_final.csv") la cambiamos a
df = pd.read_csv("/content/reportes_panama_simulados.csv")

