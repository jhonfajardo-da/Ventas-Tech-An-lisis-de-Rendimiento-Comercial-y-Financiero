# 📊 Ventas Tech – Dashboard de Control Financiero y Ventas Globales

![Power BI](https://img.shields.io/badge/Power_BI-F2C94C?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-1D6F42?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

## 📌 Descripción del Proyecto

Este repositorio contiene la solución analítica desarrollada para **Ventas Tech**[cite: 9, 10], una compañía global especializada en el comercio de tecnología, electrónica de consumo y dispositivos de audio/video. El proyecto abarca desde el procesamiento dinámico de transacciones en Python hasta la construcción de un **Dashboard de Control de Ventas y Margen** en Power BI[cite: 9, 10].

El objetivo central es consolidar la visibilidad de los ingresos por región, marca, categoría y estacionalidad, permitiendo monitorear la rentabilidad operativa y detectar oportunidades de expansión en mercados estratégicos.

---

## 🎯 Objetivos Analíticos

* **Evaluar la Facturación Global y Margen de Ganancia:** Determinar la rentabilidad neta descontando los costos unitarios directos.
* **Analizar la Concentración por Marca:** Identificar la cuota de mercado de las marcas del portafolio (*Microsoft*, *Sonos*, *Sony*, entre otras).
* **Mapear el Desempeño Geográfico:** Medir el comportamiento de compra por continente (*América del Norte*, *Europa*, *América del Sur*, etc.)[cite: 9].
* **Monitorear la Estacionalidad de Ventas:** Visualizar la evolución temporal de la facturación y el volumen transaccionado por año y mes[cite: 9].

---

## 📈 Indicadores Clave de Rendimiento (KPIs Globales)

| Métrica KPI | Valor Absoluto | Descripción |
| :--- | :--- | :--- |
| **Facturación Total** | **$6.995.302 USD** | Ventas brutas acumuladas en el periodo evaluado[cite: 9]. |
| **Costo Total** | **$2.917.725 USD** | Costos directos asociados a las unidades vendidas. |
| **Margen / Ganancia** | **$4.077.577 USD** | Utilidad bruta generada por la operación comercial. |
| **% Margen Promedio** | **58,29%** | Porcentaje promedio de rentabilidad sobre ventas. |
| **Unidades Vendidas** | **44.386 Unidades** | Volumen de mercancía distribuida globalmente. |

---

## 🔍 Análisis de Resultados y Hallazgos Clave

### 🏷️ 1. Desempeño Financiero por Marca

* **Liderazgo Comercial:** **Microsoft** ($2.15M USD / 30.75%)[cite: 9] y **Sonos** ($1.79M USD / 25.60%)[cite: 9] concentran el **56.35% de los ingresos totales**.
* **Eficiencia en Margen:** **Microsoft** y **Sony** registran los márgenes más altos de la cartera, superando el **61% de ganancia neta**.
* **Alta Rotación:** Marcas como **Kid Toys** y **Philips** impulsan el volumen físico con **17.621** y **12.114 unidades vendidas** respectivamente[cite: 9].

| Marca | Facturación (USD) | Costo Total (USD) | Margen (USD) | % Margen | Unidades |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Microsoft**[cite: 9] | $2.151.125 | $822.969 | $1.328.155 | 61.74% | 5.468 |
| **Sonos**[cite: 9] | $1.791.088 | $806.788 | $984.300 | 54.96% | 3.773 |
| **Sony**[cite: 9] | $1.259.885 | $486.664 | $773.221 | 61.37% | 3.012 |
| **Philips**[cite: 9] | $745.643 | $335.379 | $410.264 | 55.02% | 12.114 |
| **Kid Toys**[cite: 9] | $627.386 | $284.792 | $342.593 | 54.61% | 17.621 |
| **LG**[cite: 9] | $324.034 | $142.494 | $181.540 | 56.03% | 1.581 |
| **Ninja**[cite: 9] | $96.142 | $38.638 | $57.504 | 59.81% | 817 |

---

### 🌍 2. Distribución Geográfica (Continentes)

* **América del Norte:** Representa el mayor mercado de la compañía con el **52,89% de la facturación** ($3.70M USD) y **23.111 unidades**[cite: 9].
* **Europa:** Se consolida como la segunda región comercial más relevante con el **25,59%** ($1.79M USD)[cite: 9].
* **Oportunidades de Expansión:** América del Sur ($897K USD)[cite: 9] y Asia ($352K USD)[cite: 9] muestran potencial de crecimiento para aumentar la penetración de mercado.

| Continente | Facturación (USD) | Unidades Vendidas | Participación (%) |
| :--- | :--- | :--- | :--- |
| **América del Norte**[cite: 9] | $3.699.700 | 23.111 | 52.89% |
| **Europa**[cite: 9] | $1.789.918 | 11.556 | 25.59% |
| **América del Sur**[cite: 9] | $897.027 | 5.802 | 12.82% |
| **Asia**[cite: 9] | $352.824 | 2.260 | 5.04% |
| **África**[cite: 9] | $214.412 | 1.344 | 3.07% |
| **Oceanía**[cite: 9] | $41.420 | 313 | 0.59% |

---

### 📦 3. Categorías y Productos Destacados

* **Categoría Más Vendida:** **Sistema de sonido** lidera el volumen financiero acumulando **$2.416.565 USD** (34,55% del total de ventas)[cite: 9].
* **Producto Bestseller:** **Lente Leica Vario-APO** destaca como el producto individual de mayor facturación con **$1.146.565 USD** (16.39% del acumulado total)[cite: 9].

---

## 🖼️ Evidencias / Dashboard

![Dashboard de Control Financiero y Ventas Globales](Ventas%20Tech.pdf)

---

## 📐 Medidas DAX Utilizadas

El modelo analítico en Power BI incorpora lógica de cálculo mediante medidas DAX optimizadas:

```dax
// 1. Facturación Total
Facturacion_Total = 
SUMX(
    'Hoja1', 
    'Hoja1'[Precio Unidad] * 'Hoja1'[Cantidad Vendida]
)

// 2. Costo Total de Ventas
Costo_Total = 
SUMX(
    'Hoja1', 
    'Hoja1'[Costo Unidad] * 'Hoja1'[Cantidad Vendida]
)

// 3. Margen de Ganancia Bruta
Margen_Total = [Facturacion_Total] - [Costo_Total]

// 4. Porcentaje de Margen Global
Margen_Porcentaje = 
DIVIDE([Margen_Total], [Facturacion_Total], 0)

// 5. Total de Unidades Vendidas
Cantidad_Total_Vendida = SUM('Hoja1'[Cantidad Vendida])
