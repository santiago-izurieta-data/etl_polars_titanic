# Titanic ETL Pipeline

![Python](https://img.shields.io/badge/python-v3.9+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 📋 Descripción

Pipeline ETL automatizado que procesa el dataset Titanic desde Kaggle, realiza transformaciones y agregaciones utilizando Polars, y genera visualizaciones finales para análisis de supervivencia. Todo el desarrollo se realizó en Google Colab.

## 🎯 Objetivos

- Extraer datos desde CSV original del dataset Titanic.
- Limpiar y transformar datos inconsistentes (imputación de edades, categorización de tarifas).
- Validar la calidad de los datos (duplicados, nulos y tipos de datos).
- Generar métricas y agregaciones (tasas de supervivencia por clase y género).
- Visualizar resultados en gráficos finales.

## 🛠️ Stack Tecnológico

- **Python 3.9+**
- **Polars** - Manipulación rápida de datos
- **Pandas** - Conversión opcional a DataFrame para visualización
- **Matplotlib & Seaborn** - Visualización
- **pytest** (opcional) - Testing de funciones ETL
- **logging** - Monitoreo y registro de procesos
- **Google Colab**

## 📁 Estructura del Proyecto

etl_polars_titanic/
├── data/
│ ├── bronze/ # Datos crudos
│ ├── silver/ # Datos limpios
│ └── gold/ # Datos agregados
├── notebooks/
│ └── etl_polars_titanic_dataset.ipynb
└── README.md

### 🥉 Bronze
- Extracción desde fuente pública (Titanic CSV)
- Almacenamiento en Parquet sin transformaciones

### 🥈 Silver
- Imputación de edades nulas con la mediana
- Categorización de tarifas (`Low`, `Medium`, `High`, `Very High`)
- Limpieza de duplicados
- Tipificación correcta de columnas

### 🥇 Gold
- Tasas de supervivencia por clase (`Pclass`)
- Tasas de supervivencia por género (`Sex`)
- Resultados en formato Parquet listos para análisis

## 📊 Visualizaciones
1. **Tasa de supervivencia por clase**
2. **Tasa de supervivencia por género**

Generadas automáticamente al final del pipeline con Seaborn y Matplotlib.

## 🚀 Instalación

### Prerrequisitos

- Python 3.9 o superior
- pip
- Google Colab (recomendado para ejecución)

### Pasos

1. Clonar el repositorio:
    git clone https://github.com/tu-usuario/etl_polars_titanic.git
    cd etl_polars_titanic
2. Crear entorno virtual (opcional):
    python -m venv venv
    source venv/bin/activate  # En Windows: venv\Scripts\activate
3. Instalar dependencias:
    pip install -r requirements.txt

💻 Uso
En Colab

1. Abrir notebooks/etl_polars_titanic_dataset.ipynb.
2. Ejecutar todas las celdas para correr el pipeline completo.
3. Se generan automáticamente:
    - Datos crudos en data/bronze/
    - Datos limpios en data/silver/
    - Datos agregados en data/gold/
    - Visualizaciones finales de tasas de supervivencia.

Desde script (opcional)
python src/pipeline.py

🧪 Testing

Aunque el proyecto aún no incluye tests, se puede usar pytest para validar funciones ETL:
pytest tests/
Esto permite asegurar la calidad y consistencia de los datos si se agregan tests futuros.

📊 Resultados

- Limpieza e imputación de datos de edades y tarifas.
- Tablas agregadas de supervivencia por clase y género.
- Visualizaciones finales de análisis de supervivencia.
- Pipeline reproducible en Google Colab.

🔄 Flujo del Pipeline

CSV Titanic → Bronze → Silver → Gold → Visualizaciones
↓
Logging de procesos

📈 Próximas Mejoras

 Agregar tests unitarios con pytest
 Automatizar actualizaciones desde Kaggle
 Dockerización del proyecto
 Exportar resultados a Google Drive o GitHub automáticamente
 Integración con dashboard interactivo

📝 Licencia

Este proyecto está bajo la Licencia MIT - permite usar, modificar y distribuir el código con la obligación de mantener la licencia y créditos al autor.

👤 Autor

Santiago Izurieta

LinkedIn: https://ec.linkedin.com/in/santiago-izurieta-844324125

Portfolio: https://my-data-engineer-folio.lovable.app/

🙏 Agradecimientos

Comunidad de Python y Polars
Documentación de Kaggle y Seaborn
Google Colab para ejecución reproducible

