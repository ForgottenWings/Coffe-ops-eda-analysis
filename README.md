# Análisis Operacional de una Cafetería Japonesa — EDA, Estadística e Ingeniería de Menú

![Python](https://img.shields.io/badge/Python-3.11-blue)
![SQL](https://img.shields.io/badge/SQL-SQLite-lightgrey)
![Excel](https://img.shields.io/badge/Excel-openpyxl-green)
![Status](https://img.shields.io/badge/Status-En%20desarrollo-orange)

## El problema de negocio

Una cafetería operativa necesita responder preguntas críticas que 
no se pueden ver desde una planilla de Excel desorganizada:

- ¿Cuáles productos generan el mayor margen de contribución real?
- ¿En qué turnos se concentra el 80% del ingreso?
- ¿Cuánto del costo primo está fuera del rango saludable (< 60%)?
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

### Ingeniería de Menú (Kasavana & Smith, 1982)
Análisis de 157 productos con datos reales de 267 días de operación correspondientes al año 2024:

| Clasificación | Productos | Ingresos | % del total | Acción |
|---|---|---|---|---|
| Estrellas | 4 | $3,492,000 | 4.8% | Proteger y promover |
| Caballos de Trabajo | 44 | $60,373,727 | 83.0% | Auditar costos |
| Interrogantes | 30 | $4,175,320 | 5.7% | Reposicionar |
| Perros | 79 | $4,676,095 | 6.4% | Evaluar retiro |

**Hallazgo crítico:** El *Pan dulce relleno con diseño* representa el 12.83% 
del mix de ventas (producto más popular) pero clasifica como Caballo de Trabajo 
— oportunidad de mejora de margen mediante auditoría de costos y ajuste de precio.

**Estrellas identificadas:** Bubble Tea ($992K), Tokyo Box 2 ($960K), 
Curry Pan ($816K) y Frappé ($724K) — alto margen, replicar y promover.

### Validación estadística
- **H1 confirmada:** El ticket varía significativamente por día de semana 
  (Kruskal-Wallis H=115.96, p<0.001)
- **H2 confirmada:** El fin de semana genera mayor ticket promedio 
  ($8,689 vs $7,293 CLP, Mann-Whitney p<0.001)
- **H3 no confirmada:** Correlación precio-popularidad débil (r=-0.120, p=0.136)
- **H4 confirmada:** Ingresos difieren significativamente entre secciones 
  (Kruskal-Wallis H=4415.13, p<0.001)

### KPIs operacionales 2024
- **Ingresos totales:** $75,648,488 CLP (267 días de operación)
- **Ticket promedio:** $7,547 CLP
- **Ingresos promedio diario:** $283,328 CLP
- **Método de pago principal:** Débito (63.3% de los ingresos)
- **Sección líder:** Panadería de autor ($11,622,400 CLP)
- **Propinas registradas:** 421 transacciones

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

Datos reales obtenidos de una cafetería con "temática Japonesa" ubicada en la ciudad de Concepción, Chile; 
con autorización del establecimiento. Los datos fueron anonimizados eliminando información de clientes y personal.

---

## Autor

**Rodolfo Moreno** · Cloud Data Analyst  
Administrador Gastronómico Internacional  
[LinkedIn](#) · [GitHub](https://github.com/ForgottenWings)