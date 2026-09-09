# DataProject-Proyecto-Final

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Data_Analysis-blue?style=for-the-badge)

## Descripción del Proyecto
Este proyecto desarrolla un análisis telemétrico y de rendimiento histórico de la Fórmula 1 sobre **278.678 registros** abarcan las temporadas **1982–1995** y **2011–2012**. 
El proyecto aborda desde el ritmo telemétrico vuelta a vuelta hasta la eficiencia en paradas en boxes, la conversión de *pole positions* y el rendimiento histórico por escuderías.

El flujo de trabajo combina la exploración de datos avanzada en **Python (Pandas/NumPy)** con el modelado relacional y la creación de un dashboard en **Power BI**.

---

## Arquitectura Técnica y Tecnologías

El flujo de trabajo se divide en tres fases principales:

1. **Exploración y Preprocesamiento (Python / Jupyter Notebooks):**
   * Limpieza de datos, imputación de nulos y estandarización con **Pandas** y **NumPy**.
   * Análisis exploratorio de datos (EDA) para identificar patrones de edad, ritmo de carrera y degradación telemétrica.
   * Exportación del dataset consolidado e higienizado (`f1_data.csv`).

2. **Modelado y ETL (Power Query):**
   * Verificación de tipos de datos e integración de coordenadas geográficas (`lat`, `lng`).
   * Categorización de la columna `country` como tipo *País o Región* para la integración fluida con mapas.

3. **Visualización (Power BI Desktop):**
   * Desacoplamiento del dataset plano en un modelo relacional.
   * Creación de medidas analíticas dinámicas en **DAX** informativos.

---

## Modelo de Datos Relacional (Star Schema)

Para optimizar la interpretación de los datos y garantizar filtrados cruzados de respuesta inmediata, se diseñó la siguiente arquitectura:

```text
       Conductor [1] ────┐
                         │
       Constructor[1]    ────┼───> [*] DatosPowerBI
                         │
       Circuito.[1]  ────┤
                         │
       Carrera [1]   ────┘
```
---

## Tecnologías Utilizadas

* **Python 3.14.3:** Pandas, NumPy.
* **Power BI Desktop:** Power Query, Lenguaje DAX, Modelado de Datos.
* **Git/GitHub:** Control de versiones.
---
##  Estructura del Repositorio

```text

├── rawdata/                         # Carpeta con archivos de origen / conexion local
├── 1-limpiezadatos.ipynb            # Notebook de ingesta y preprocesamiento
├── 2-AnalisisEDA.ipynb              # Notebook del Análisis Exploratorio de Datos (EDA)
├── DATA PROJECT_ PROYECTO FINAL.pdf # Memoria / Informe académico en PDF
├── Dashboard-ProyectoFinal.pbix     # Archivo interactivo de Power BI Desktop
├── f1_data.csv                      # Dataset procesado y unificado
├── data_combinada.csv.zip           # Dataset comprimido de respaldo
└── README.md                        
