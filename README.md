# DataProject-Proyecto-Final

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Data_Analysis-blue?style=for-the-badge)

## 📌 Descripción del Proyecto
Este proyecto de Master desarrolla un análisis telemétrico y de rendimiento histórico de la Fórmula 1 sobre **278.678 registros** abarcan las temporadas **1982–1995** y **2011–2012**. 

El flujo de trabajo combina la exploración de datos avanzada en **Python (Pandas/NumPy)** con el modelado relacional en estrella (*Star Schema*) y la creación de un cuadro de mando interactivo en **Power BI**.

---

## 📊 Arquitectura del Modelo de Datos (Star Schema)

El modelo en Power BI se optimizó separando la tabla plana telemétrica en un **Esquema en Estrella**:

* **Fact_Telemetry:** Tabla principal de hechos a nivel de vuelta disputada.
* **Dim_Driver:** Información descriptiva y demográfica del piloto.
* **Dim_Constructor:** Histórico de escuderías y constructores.
* **Dim_Circuit:** Ubicación geográfica y trazados.
* **Dim_Race:** Temporadas, fechas y Grandes Premios.

---

## 📈 Hallazgos Analíticos Clave

1. **Conversión Pole a Victoria:** La tasa de conversión global de salir en 1ª posición (*Pole Position*) a ganar la carrera se sitúa en un **39,75%**.
2. **Promedio de Remontada:** La ganancia neta media de posiciones por carrera es de **+2,64 puestos**.
3. **Pico de Edad:** El rendimiento óptimo de los pilotos se concentra en la franja de **26 a 30 años**.
4. **Estrategia en Pit Stops:** Se empleó la mediana para aislar el impacto de paradas accidentadas, mostrando una reducción significativa en los tiempos de servicio en la era moderna.

---

## 🖥️ Estructura del Dashboard en Power BI

El dashboard consta de dos páginas navegables:
* **Página 1 (Vista Ejecutiva):** KPIs principales (`Total Carreras`, `Tiempo Medio`, `% Pole to Win`), victorias por escudería y mapa interactivo de circuitos.
* **Página 2 (Vista Técnica):** Comparativa telemétrica de ritmo por vuelta (`lap_seconds`) filtrable por Gran Premio, año y pilotos rivales.

---

## 🛠️ Tecnologías Utilizadas

* **Python 3.x:** Pandas, NumPy, Matplotlib, Seaborn.
* **Power BI Desktop:** Power Query, Lenguaje DAX, Modelado de Datos.
* **Git/GitHub:** Control de versiones.

---

## 📂 Estructura del Repositorio

* `data/`: Dataset telemétrico procesado.
* `notebooks/`: Cuadernos Jupyter con el EDA y preprocesamiento.
* `powerbi/`: Archivo `.pbix` interactivo.
* `docs/`: Memoria/Informe final en PDF.
