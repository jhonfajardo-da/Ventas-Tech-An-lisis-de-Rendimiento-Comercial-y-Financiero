# Ventas Tech – Análisis de Rendimiento Comercial y Financiero

Este proyecto presenta un análisis integral de las operaciones de ventas globales de **Ventas Tech**, una empresa dedicada a la comercialización de productos tecnológicos[cite: 9, 10]. El objetivo principal es evaluar la facturación, los costos, el margen de ganancia y el rendimiento geográfico y por producto para optimizar la toma de decisiones comerciales[cite: 9, 10].

---

## 📊 Indicadores Clave de Rendimiento (KPIs)

* **Facturación Total:** $6.995.302 USD
* **Costo Total:** $2.917.725 USD
* **Ganancia / Margen Bruto:** $4.077.577 USD
* **Margen de Ganancia Global:** 58,29%
* **Unidades Vendidas:** 44.386 unidades

---

## 🔍 Hallazgos Principales

* **Liderazgo por Marca:** **Microsoft** ($2.15M USD) y **Sonos** ($1.79M USD)[cite: 9] representan el **56.3%** del volumen total de facturación.
* **Distribución Geográfica:** **América del Norte** lidera con el **52,89%** ($3.70M USD) de las ventas, seguida por **Europa** con el **25,59%** ($1.79M USD).
* **Categoría y Producto Top:** La categoría de **Sistema de sonido** aporta $2.42M USD (34.5% del total)[cite: 9], mientras que el producto **Lente Leica Vario-APO** genera $1.15M USD individuales[cite: 9].

---

## 🛠️ Tecnologías y Herramientas Utilizadas

* **Python:** Limpieza, procesamiento de datos y verificación de métricas (`pandas`, `openpyxl`).
* **Power BI / DAX:** Modelado de datos multidimensional, creación de medidas y visualización interactiva[cite: 10].
* **Excel:** Análisis exploratorio inicial de la base de datos `Ventas Tech.xlsx`.

---

## 📂 Estructura del Repositorio

```text
├── data/
│   └── Ventas Tech.xlsx       # Dataset principal de ventas
├── notebooks/
│   └── data_analysis.ipynb    # Código Python para exploración y limpieza
├── pbix/
│   └── Ventas_Tech.pbix       # Dashboard interactivo de Power BI
└── README.md                  # Documentación del proyecto

---
## 🖼️ Evidencias / Dashboard

![Dashboard de Productividad y Piezas Fabricadas](screenshots/overview.png)[cite: 10]

---

## 📐 Medidas DAX Implementadas

Fragmento de código
// Facturación Total
Facturacion_Total = SUMX('Hoja1', 'Hoja1'[Precio Unidad] * 'Hoja1'[Cantidad Vendida])

// Costo Total
Costo_Total = SUMX('Hoja1', 'Hoja1'[Costo Unidad] * 'Hoja1'[Cantidad Vendida])

// Ganancia Bruta
Ganancia_Total = [Facturacion_Total] - [Costo_Total]

// % Margen de Ganancia
Margen_Porcentaje = DIVIDE([Ganancia_Total], [Facturacion_Total], 0)
