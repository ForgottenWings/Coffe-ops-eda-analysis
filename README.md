# Análisis Operacional de una Cafetería Japonesa — EDA, Estadística e Ingeniería de Menú

![Python](https://img.shields.io/badge/Python-3.11-blue)
![SQL](https://img.shields.io/badge/SQL-SQLite-lightgrey)
![Excel](https://img.shields.io/badge/Excel-openpyxl-green)
![Status](https://img.shields.io/badge/Status-En%20desarrollo-orange)

## El problema de negocio

Una cafetería con operación diaria necesita responder preguntas críticas que 
no puede ver desde una planilla de Excel desorganizada:

- ¿Cuáles productos generan el mayor margen de contribución real?
- ¿En qué turnos se concentra el 80% del revenue?
- ¿Cuánto del prime cost está fuera del rango saludable (< 60%)?
- ¿Qué ítems del menú deberían eliminarse y cuáles potenciarse?

Este proyecto responde esas preguntas usando análisis exploratorio de datos,
estadística inferencial e Ingeniería de Menú (Kasavana & Smith, 1982) sobre
datos reales de una cafetería chilena ubicada en la ciudad de Concepción, con autorización del establecimiento.

---

## Stack tecnológico

| Herramienta | Uso en este proyecto |
|---|---|
| Python 3.11 | Limpieza, análisis y visualización |
| Pandas / NumPy | Manipulación de datos |
| SciPy / Statsmodels | Estadística inferencial |
| Matplotlib / Seaborn | Visualizaciones |
| SQLite + SQLAlchemy | Análisis SQL sobre los datos |
| openpyxl | Reporte ejecutivo en Excel |
| Jupyter Notebook | Documentación narrativa del análisis |

---

## Estructura del proyecto

Coffe-ops-eda-analysis/
├── data/
│   ├── raw/            ← datos originales (no incluidos en el repo)
│   └── processed/      ← datos limpios generados por el código
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_estadistica.ipynb
│   └── 03_ingenieria_menu.ipynb
├── sql/
│   └── cafeteria_analytics.sql
├── src/
│   ├── data_cleaning.py
│   └── menu_engineering.py
├── output/             ← gráficos generados
├── reports/
│   └── executive_report.xlsx
├── requirements.txt
└── README.md

---

## Hallazgos principales

> Esta sección se completará al finalizar el análisis.

---

## Cómo reproducir este proyecto

```bash
# 1. Clonar el repositorio
git clone https://github.com/ForgottenWings/Coffe-ops-eda-analysis.git
cd Coffe-ops-eda-analysis

# 2. Crear entorno virtual
python -m venv venv
venv\Scripts\activate      # Windows
source venv/bin/activate   # Mac/Linux

# 3. Instalar dependencias
pip install -r requirements.txt

# 4. Ejecutar notebooks en orden
jupyter notebook
```

---

## Contexto del negocio

Datos reales de la cafetería ubicada en ciudad de Concepción, Chile, 
con autorización del establecimiento. Los datos fueron anonimizados
eliminando información de clientes y personal.

---

## Autor

**Rodolfo Moreno** · Cloud Data Analyst  
Administrador Gastronómico Internacional  
[LinkedIn](#) · [GitHub](https://github.com/ForgottenWings)