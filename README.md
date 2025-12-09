# TelecomX LATAM (Challenge)

Descripción
- Notebook: [ChallengeTelecomX_LATAM.ipynb](c:\Users\Juve\Downloads\ChallengeTelecomX_LATAM.ipynb)
- Objetivo: Extraer, limpiar, transformar y analizar datos de churn para TelecomX LATAM. Incluye EDA, visualizaciones y un informe final con hallazgos y recomendaciones.

Estructura del notebook
- Extracción: obtiene JSON desde la URL definida en la variable `api_url`.
- Transformación:
  - Desanida columnas: `customer`, `phone`, `internet`, `account` → DataFrames (`customer_df`, `phone_df`, `internet_df`, `account_df`).
  - Normaliza nombres y valores, elimina filas con churn vacío y duplicados, mapea variables binarias.
  - Resultado principal en `df`.
- Carga y análisis: estadísticas, cruces por churn, gráficos (Matplotlib/Seaborn).
- Informe final: salida formateada con insights y recomendaciones.

Dependencias
- Python 3.8+
- pandas
- requests
- matplotlib
- seaborn

Instalación rápida
```sh
pip install pandas requests matplotlib seaborn
```

Cómo ejecutar (en VS Code)
1. Abrir el archivo [ChallengeTelecomX_LATAM.ipynb](c:\Users\Juve\Downloads\ChallengeTelecomX_LATAM.ipynb).
2. Seleccionar un kernel de Python con las dependencias instaladas.
3. Ejecutar las celdas en orden (Extracción → Transformación → Análisis → Informe).
4. Ver salida/plots en el panel de notebooks de VS Code.

Variables y artefactos clave
- `api_url` — URL de la fuente JSON. ([ver celda](c:\Users\Juve\Downloads\ChallengeTelecomX_LATAM.ipynb))
- `df` — DataFrame final preparado para análisis y modelado. ([ver celda](c:\Users\Juve\Downloads\ChallengeTelecomX_LATAM.ipynb))
- `customer_df`, `phone_df`, `internet_df`, `account_df` — DataFrames intermedios tras la desanidación. ([ver celda](c:\Users\Juve\Downloads\ChallengeTelecomX_LATAM.ipynb))

Salida esperada
- DataFrame limpio con ~7,043 registros y 20 columnas.
- Visualizaciones: distribución de churn, churn por género, por tipo de contrato, boxplot de tenure.
- Informe textual con insights y recomendaciones (impreso al final del notebook).

Siguientes pasos recomendados
- Guardar `df` a CSV para uso posterior: `df.to_csv("telecomx_clean.csv", index=False)`.
- Construir modelo predictivo de churn usando el `df` procesado.
- Integrar el notebook en un pipeline reproducible (scripts + tests).

Licencia
- Uso interno / educativo. Ajustar según políticas de datos de la organización.
