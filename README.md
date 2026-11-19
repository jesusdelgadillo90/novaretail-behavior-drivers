# NovaRetail+ — Análisis exploratorio de drivers de comportamiento y correlaciones

Análisis correlacional y exploratorio sobre el dataset `novaretail_comportamiento_clientes_2024.csv` (**15,000 clientes** y **12 variables** de comportamiento, segmentación y valor económico) para **NovaRetail+** durante 2024, enfocado en entender qué factores se asocian con el `ingreso_anual` sin confundir correlación con causalidad.

## 📂 Contenido del repositorio
* [`S8_Student_Version_Project_NovaRetail.ipynb`](S8_Student_Version_Project_NovaRetail.ipynb) — *Notebook* con exploración inicial, limpieza de datos (`edad` convertida a entero), revisión de variables numéricas, binarias y categóricas, visualizaciones (*heatmap*, *pairplot* y *scatterplots*), cálculo de coeficientes de correlación, interpretación de hallazgos, limitaciones y próximos pasos.

## ▶ Cómo abrir y reproducir el análisis
1. Abre [`S8_Student_Version_Project_NovaRetail.ipynb`](S8_Student_Version_Project_NovaRetail.ipynb) directamente en GitHub o ábrelo en **Google Colab** para ejecutar las celdas de forma interactiva.
2. Ejecuta las celdas en orden secuencial (el análisis utiliza `pandas`, `numpy`, `scipy.stats`, `matplotlib` y `seaborn`).
3. Revisa las secciones de preparación de datos, correlaciones y conclusiones de negocio.

## 📊 Hallazgos principales y conclusiones
* **Compras mensuales vs. ingreso anual:** Relación lineal positiva muy fuerte (**Pearson = 0.967**, **Spearman = 0.967**), posicionando `compras_mes` como el principal factor asociado con `ingreso_anual`.
* **Publicidad dirigida y tráfico:** Correlación positiva moderada entre `gasto_publicidad_dirigida` y `visitas_mes` (**Pearson = 0.579**, **Spearman = 0.559**), mientras que el vínculo directo entre gasto publicitario e `ingreso_anual` es débil (**~0.20**).
* **Membresía premium y abandono:** Correlaciones punto-biserial bajas/cercanas a cero frente a `ingreso_anual` (`miembro_premium`: **0.093**; `abandono`: **-0.0028**), lo que sugiere revisar métricas complementarias (retención, margen y encuestas de salida) antes de rediseñar el programa.
* **Región y dispositivo:** El predominio es móvil (**65.45%**), y la asociación entre `region` y `tipo_dispositivo` es prácticamente nula (**V de Cramér = 0.0124**).
* **Limitación clave:** Este análisis es correlacional y no establece causalidad; los siguientes pasos recomendados incluyen modelos multivariados/segmentación, pruebas A/B controladas y análisis cualitativo.
