# Sprint_14_Proyecto_Final_Modular

Este repositorio forma parte de la entrega del proyecto final del Sprint 14 del bootcamp de análisis de datos.  
El objetivo del proyecto es analizar el desempeño operativo de un servicio de telefonía virtual (CallMeMaybe) para identificar posibles áreas de mejora.

El análisis se desarrolló inicialmente en un Jupyter Notebook (`.ipynb`), pero esta versión ha sido **modularizada** en distintos scripts de Python organizados por función, lo que permite un mantenimiento más limpio y profesional.

---

## Estructura inicial del proyecto

- **`load_data.py`**: Carga los datasets crudos desde archivos `.csv` y los convierte en DataFrames para análisis posteriores.
- **`preprocessing.py`**: Contiene funciones para limpiar y transformar los datos, incluyendo el formateo de fechas, creación de columnas clave (`wait_time`, `call_duration`), y tratamiento de outliers. Genera los DataFrames `df_calls`, `df_clients`, `df_calls_no_outliers`, entre otros.

---

## Etapa de Análisis Exploratorio de Datos (EDA)

Se completó la etapa de EDA con una **modularización del análisis**, separando las funciones clave en scripts individuales dentro del directorio `/scripts`.

Esto permite mantener un código limpio, reutilizable y más fácil de escalar o modificar.

### Scripts creados

| Script                     | Descripción                                                            |
| -------------------------- | ---------------------------------------------------------------------- |
| `eda_outliers.py`          | Análisis y visualización de outliers por plan tarifario                |
| `eda_planes.py`            | Distribución de llamadas atípicas por tipo de plan tarifario           |
| `eda_operadores.py`        | Métricas agregadas por operador (llamadas, espera, duración, pérdidas) |
| `eda_tiempos.py`           | Análisis de duración de llamadas y tiempos de espera                   |
| `eda_llamadas_perdidas.py` | Bin de tiempos de espera y proporción de llamadas perdidas             |

### 🔄 Orden sugerido de ejecución

1. `eda_outliers.py`
2. `eda_planes.py`
3. `eda_operadores.py`
4. `eda_tiempos.py`
5. `eda_llamadas_perdidas.py`

---

> Para ejecutar los análisis, asegúrate de tener cargados `df_calls`, `df_clients`, y haber aplicado el preprocesamiento previo. Cada módulo puede ser importado o ejecutado de manera individual.
