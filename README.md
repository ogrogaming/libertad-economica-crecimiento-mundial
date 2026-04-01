# Libertad Económica y Crecimiento — Análisis de Panel Data

Análisis empírico de la relación entre libertad económica y bienestar
en 164 países entre 2000 y 2023, usando el índice Economic Freedom of
the World del Fraser Institute y datos del World Bank.

## Hallazgos principales

- Los países del cuartil más libre tienen un PBI per cápita **13 veces mayor**
  que los del cuartil menos libre (USD 31.813 vs USD 2.402)
- La mortalidad infantil es **7 veces menor** en los países más libres
  (7.7 vs 53.3 por mil nacidos)
- La regresión de panel con fixed effects de país y año muestra que
  **desregulación** y **comercio libre** son las áreas con mayor efecto
  significativo sobre el crecimiento

## Resultados econométricos (Panel FE, errores clustered por país)

| Área | Coeficiente | p-value | Significativo |
|------|-------------|---------|---------------|
| Regulación (área 5) | +0.74 | 0.005 | Sí |
| Comercio libre (área 4) | +0.35 | 0.028 | Sí |
| Moneda sana (área 3) | +0.21 | 0.061 | Marginal |
| Sistema legal (área 2) | +0.03 | 0.920 | No |
| Tamaño del gobierno (área 1) | -0.25 | 0.265 | No |

## Visualizaciones

### Libertad económica vs. crecimiento del PBI — 164 países
Gráfico de burbujas interactivo. Tamaño = PBI per cápita. Color = región.

### Índice de Libertad Económica por país (2000–2023)
Mapa coroplético animado. Reproducir para ver cómo evolucionó la libertad
económica globalmente año a año.

### Bienestar por cuartil de libertad
PBI per cápita, crecimiento y mortalidad infantil desagregados por cuartil.

### Coeficientes de regresión con intervalos de confianza
¿Cuál de las 5 áreas del índice Fraser realmente impulsa el crecimiento?

## Fuentes de datos

- [Fraser Institute — Economic Freedom of the World 2024]
  (https://www.fraserinstitute.org/economic-freedom/dataset)
- [World Bank Open Data API](https://data.worldbank.org)
  - PBI per cápita (USD constantes): NY.GDP.PCAP.KD
  - Crecimiento PBI per cápita: NY.GDP.PCAP.KD.ZG
  - Coeficiente de Gini: SI.POV.GINI
  - Mortalidad infantil: SP.DYN.IMRT.IN

## Herramientas

- Python 3.12
- pandas, numpy
- linearmodels (Panel OLS con Fixed Effects)
- Plotly Express (gráficos interactivos + coroplético)
- Google Colab

## Cómo reproducir el análisis

1. Descargar el dataset del Fraser Institute desde el link de arriba
2. Abrir `notebook.ipynb` en Google Colab
3. Subir el archivo `.xlsx` cuando se solicite
4. Ejecutar todas las celdas en orden

## Marco teórico

Análisis enmarcado en la tradición de la Escuela Austriaca y la Escuela
de Chicago: Hayek sobre orden espontáneo y señales de precios, Friedman
sobre estabilidad monetaria y libre comercio, y la literatura de economía
institucional sobre derechos de propiedad y estado de derecho como
determinantes del crecimiento de largo plazo.

## Autor

Gabriel López del Cerro — Economista y Data Scientist
https://www.linkedin.com/in/gabriellopezdelcerro
