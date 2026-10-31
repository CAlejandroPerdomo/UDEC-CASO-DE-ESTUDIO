# Análisis de la deserción escolar en Medellín (2017)

Trabajo académico de análisis de datos que estudia el patrón de la **deserción escolar** en
Medellín durante 2017, a partir de los registros educativos oficiales desagregados por
establecimiento, sexo y grado.

## Pregunta de investigación

> ¿Cuál es el patrón de deserción escolar en Medellín durante 2017 según el nivel educativo
> (grado) y el sexo?

## Resumen de resultados

| Hallazgo | Resultado |
|---|---|
| Tasa global de deserción | 3,18 % |
| Educación para adultos vs. regular | 10,47 % vs. 2,45 % (p < 0,001) |
| Pico en educación regular | Grado 6: 4,67 % |
| Por sexo (hombres vs. mujeres) | 3,55 % vs. 2,81 % (no significativo, p = 0,88) |
| Por sector | Cobertura contratada: 5,61 % |
| Correlación matrícula–deserción | Spearman ρ = 0,67 |

**Conclusión:** la deserción se concentra en la *educación para adultos* y, dentro de la
regular, en la *transición a secundaria* (grado 6). El **sexo no es un factor discriminante**.

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `desercion_educativa.csv` | Dataset original (única fuente de datos). |
| `analisis_desercion.ipynb` | Notebook principal con el análisis completo: carga, limpieza, transformación, estadística descriptiva, visualización, pruebas de hipótesis e interpretación. |
| `informe_desercion.pdf` | Informe académico final en formato PDF (LaTeX). |
| `informe_desercion.tex` | Código fuente LaTeX del informe. |
| `fig_*.png` | Figuras generadas para el informe (grado, tipo, sexo y sector). |

## Requisitos

El notebook fue desarrollado en **Python 3.14** con las siguientes librerías:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scipy`

## Reproducción

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/CAlejandroPerdomo/UDEC-CASO-DE-ESTUDIO.git
   ```

2. Abrir y ejecutar `analisis_desercion.ipynb` (por ejemplo, en JupyterLab) en orden, de
   arriba hacia abajo. Todos los resultados son reproducibles re-ejecutando las celdas.

## Metodología

- **Limpieza:** se verificó la ausencia de valores nulos, duplicados e inconsistencias; se
  normalizaron tipos y categorías.
- **Transformación:** cálculo de la tasa de deserción (`deserciones / matrícula × 100`) y
  reorganización de los datos a formato largo (una fila por grado).
- **Análisis estadístico:** estadística descriptiva, análisis por grupo, correlación de
  Spearman y pruebas de hipótesis no paramétricas (Shapiro-Wilk, Mann-Whitney U y
  Kruskal-Wallis, con comparaciones post-hoc corregidas por Bonferroni).

## Autor

**Cristian Alejandro Perdomo Rivas**
