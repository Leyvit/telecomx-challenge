# 📡 TelecomX — Análisis de Evasión de Clientes (Churn)
### Challenge · Oracle Next Education × Alura Latam

---

## 📌 Propósito del análisis

Telecom X enfrenta una alta tasa de cancelación de clientes. Como analista de datos, el objetivo es aplicar un proceso completo de **ETL (Extracción, Transformación y Carga)** y **Análisis Exploratorio de Datos (EDA)** para identificar los factores que llevan a la evasión de clientes y generar insights estratégicos que permitan reducir el churn.

---

## 📁 Estructura del proyecto

```
telecomx-challenge/
│
├── TelecomX_Challenge.ipynb      # Notebook principal con ETL + EDA + Informe
├── README.md                     # Este archivo
├── grafico_churn_distribucion.png  # Pie — Distribución de evasión
├── grafico_churn_categoricas.png   # Barras — Evasión por variables categóricas
├── grafico_churn_numericas.png     # Histogramas — Evasión por variables numéricas
├── grafico_scatter_churn.png       # Dispersión — Cargos vs Tiempo de contrato
└── grafico_correlacion.png         # Matriz de correlación
```

---

## 🔄 Proceso ETL aplicado

**Extracción:** Datos cargados directamente desde la API de Telecom X en formato JSON usando Python y Pandas.

**Transformación:**
- Normalización de columnas anidadas (JSON → DataFrame plano)
- Eliminación de duplicados
- Tratamiento de valores nulos
- Estandarización de strings y tipos de datos
- Conversión de variables binarias (Yes/No → 1/0)
- Creación de columna `Cargos_Diarios`

**Carga:** Dataset limpio listo para análisis y modelos predictivos.

---

## 📊 Análisis realizados

- Distribución general de la evasión (tasa de churn)
- Evasión por variables categóricas (género, tipo de contrato, método de pago, etc.)
- Evasión por variables numéricas (tiempo de contrato, cargos mensuales, total gastado)
- Análisis de correlación entre variables (extra opcional)

---

## 📈 Visualizaciones generadas

| Gráfico | Tipo | Descripción |
|---|---|---|
| Distribución de churn | Pie | Proporción de clientes que evadieron vs se quedaron |
| Variables categóricas | Barras agrupadas | Churn según género, contrato, pago, etc. |
| Variables numéricas | Histogramas | Distribución de cargos y tenure por churn |
| Cargos vs Tenure | Dispersión | Relación entre tiempo de contrato y cargos mensuales |
| Correlación | Mapa de calor | Correlación entre todas las variables numéricas |

---

## Insights principales

| Métrica | Resultado |
|---|---|
| Total de clientes analizados | 7,267 |
| Clientes que evadieron | 1,869 (25.7%) |
| Clientes que se quedaron | 5,398 (74.3%) |
| Cargo mensual prom. (evadieron) | $74.44 |
| Cargo mensual prom. (se quedaron) | $61.35 |

- Perfil de mayor riesgo: clientes con **contrato mes a mes**, **alto cargo mensual** y **baja antigüedad**
- A mayor tiempo de contrato, menor probabilidad de churn
- Principal recomendación: fidelización temprana y migración a contratos anuales

---

## Cómo ejecutar el proyecto

### Opción 1 — Google Colab (recomendado)

1. Abre [Google Colab](https://colab.research.google.com/)
2. Sube el archivo `TelecomX_Challenge.ipynb`
3. Ejecuta todas las celdas con `Runtime > Run all`

### Opción 2 — Local

```bash
git clone https://github.com/Leyvit/telecomx-challenge.git
cd telecomx-challenge

pip install pandas matplotlib numpy

jupyter notebook TelecomX_Challenge.ipynb
```

---

## Dependencias

- Python 3.8+
- pandas
- matplotlib
- numpy

---

## Autor

Desarrollado por **Edmundo Leyva Ramos**
Challenge 2 — Oracle Next Education × Alura Latam

🔗 [LinkedIn — Edmundo Leyva Ramos](https://www.linkedin.com/in/ed-leyva/)
