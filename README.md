
# 🔌 Laboratorio ETL: Análisis del Sistema Energético en España

## 📖 Descripción
Este laboratorio forma parte de una serie de prácticas enfocadas en el análisis de datos del sistema energético en España. En esta lección, desarrollamos el proceso de *Extracción, Transformación y Carga* (ETL) para limpiar y estructurar datos de consumo y generación eléctrica a nivel provincial, junto con información demográfica y económica. El objetivo es explorar las relaciones entre la demanda, el consumo y la generación eléctrica con factores como la población y el PIB a lo largo del tiempo.

### Objetivo Principal
El análisis busca identificar patrones y correlaciones entre la demanda eléctrica, el consumo y los factores socioeconómicos de distintas provincias en España, y así comprender mejor las dinámicas energéticas regionales y su impacto en el desarrollo económico.

## 🗂️ Estructura del Proyecto

El proyecto está organizado de la siguiente manera:

```markdown
├── data/                   # Contiene los datos crudos y transformados
├── notebooks/              # Notebook Jupyter donde se realiza el análisis
├── src/                    # Scripts de procesamiento y transformación
├── results/                # Visualizaciones y archivos de resultados
├── README.md               # Descripción del proyecto
```

## 🛠️ Instalación y Requisitos

Para ejecutar este proyecto necesitarás Python 3.8 o superior y las siguientes bibliotecas:

- `pandas`: para manipulación y limpieza de datos
- `numpy`: para cálculos numéricos
- `matplotlib`: para visualización básica
- `requests`: para obtener datos de la API
- `datetime`: para manipulación de fechas

Instala las dependencias ejecutando:

```bash
pip install pandas numpy matplotlib requests datetime
```

## ⚙️ Proceso de Transformación

Este laboratorio se centra en la fase de *Transformación* del proceso ETL. A continuación, un desglose de las tareas realizadas:

### 1. Carga de Datos
   - **Demanda Eléctrica**: Datos extraídos de la API de Red Eléctrica Española (REE).
   - **Generación Eléctrica**: Información detallada por tipo de energía (eólica, solar, hidroeléctrica).
   - **Datos Demográficos**: Datos de población a nivel provincial desde el Instituto Nacional de Estadística (INE).
   - **Datos Económicos**: Información del PIB por provincia obtenida del INE.

### 2. Limpieza y Estandarización
   - **Conversión de Timestamps**: Unificación de formatos de fecha en todos los conjuntos de datos (`YYYY-MM` para datos mensuales).
   - **Tratamiento de Valores Nulos**: Identificación y manejo de valores faltantes; se opta por eliminar o sustituir los valores según su impacto.
   - **Estandarización de Nombres de Provincias**: Consistencia en los nombres de provincias entre diferentes fuentes de datos.

### 3. Transformación de Datos
   - **Demanda y Generación Eléctrica**:
      - Conversión de unidades a MWh y normalización de datos entre provincias.
      - Identificación de valores atípicos (outliers) en la generación de energía.
   - **Datos Demográficos y Económicos**:
      - Normalización de PIB entre provincias y en diferentes períodos de tiempo.
      - Consistencia en etiquetas y categorías de datos demográficos.

> **Nota**: Esta limpieza prepara los datos para su futura inserción en una base de datos, facilitando su análisis posterior.

## 📊 Resultados y Conclusiones

- **Hipótesis Evaluadas**:
  - **Demanda vs. Población**: Se espera una correlación positiva entre la población y la demanda eléctrica provincial.
  - **Consumo vs. PIB**: Provincias con un PIB alto presentan mayor consumo energético.
  - **Generación Renovable**: Regiones con condiciones geográficas o económicas favorables generan más energía renovable.

Estos resultados se utilizarán en el próximo análisis para validar las hipótesis y entender las implicancias socioeconómicas de estos datos.

## 🔄 Próximos Pasos

- Inserción de los datos transformados en una base de datos.
- Realización de análisis descriptivos y predictivos.
- Implementación de técnicas avanzadas para la generación de informes.

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Si deseas colaborar, por favor abre un pull request o una issue.

