# 📊 Análisis de Comportamiento de Clientes - ConnectaTel

Este repositorio contiene el análisis exploratorio de datos (EDA) y la segmentación de clientes para **ConnectaTel**, una empresa de telecomunicaciones con operaciones en México y Colombia.

## 🎯 Objetivo del Proyecto
Evaluar el comportamiento de los clientes (uso de llamadas y mensajes), limpiar y unificar las bases de datos, y detectar patrones de uso y segmentos accionables para optimizar la oferta comercial.

## 📁 Datasets Utilizados
El análisis se realizó utilizando tres fuentes de datos:
*   `plans.csv`: Catálogo de planes (precio, minutos, GB, costos extra).
*   `users_latam.csv`: Información de clientes (edad, ciudad, plan, churn).
*   `usage.csv`: Detalle del uso real (duración de llamadas, longitud de textos).

## 🔄 Etapas del Análisis
1.  **Carga y exploración inicial:** Revisión de tipos de datos y dimensiones.
2.  **Limpieza de datos (Data Cleaning):** 
    *   Corrección de sentinels (reemplazo de `-999` en edades y `?` en ciudades).
    *   Tratamiento de fechas imposibles (años futuros 2026 convertidos a nulos).
    *   Identificación de nulos MAR (Missing At Random) en la tabla de uso.
3.  **Integración (Merge):** Creación de una tabla maestra (`user_profile`) uniendo usuarios, planes y totales de uso.
4.  **Análisis Estadístico y Visual:** Uso de histogramas y boxplots para identificar distribuciones y valores atípicos (outliers).
5.  **Segmentación:** Clasificación de clientes por nivel de uso (Bajo, Medio, Alto) y por edad (Joven, Adulto, Adulto Mayor).
6.  **Insight Ejecutivo:** Conclusiones de negocio y recomendaciones estratégicas.

## 💡 Hallazgos Principales
*   El cliente típico de ConnectaTel es un **adulto** (media de 48 años) con un uso moderado del servicio.
*   Se detectaron **109 usuarios "heavy users"** con consumos extremos de minutos (hasta 155 min), quienes representan el mayor valor para la empresa.
*   El plan **Premium** está capturando exitosamente al segmento de mayor consumo, mientras que el Básico domina el mercado masivo.

## 🚀 Cómo reproducir este análisis
1.  Clona este repositorio.
2.  Asegúrate de tener instaladas las librerías necesarias: `pandas`, `numpy`, `matplotlib` y `seaborn`.
3.  Abre el archivo `.ipynb` (Jupyter Notebook) en tu entorno local o en Google Colab.
4.  Ejecuta las celdas en orden secuencial (Run All).

---
*Análisis realizado por: [Tu Nombre Aquí]*
