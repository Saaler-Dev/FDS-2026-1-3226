# FDS-2026-1-3226

## Integrantes del grupo

| Código | Nombre |
| :--- | :--- |
| U202315231 | Mariana Alexa Rafael Sosa |
| U20231H075 | Alvaro Jerry Rivera Calderón |
| U202413604 | Ronal Sebastian Cueto Ninaja |
| U202322704 | Ericks Santiago Alarcon Castellanos |

---

## Objetivo del proyecto

Una consultora internacional con sede en Lima requiere conocer las tendencias de los videos de YouTube en siete países, a solicitud de un cliente de marketing digital. Este repositorio desarrolla la parte del análisis correspondiente a **Alemania (DE)**, aplicando la metodología CRISP-DM para:

* Crear conocimiento y valor de negocio a partir de los datos de videos en tendencia.
* Evaluar la factibilidad de predecir el número de vistas de un video a partir de sus demás métricas de interacción (likes, dislikes, comentarios), categoría y antigüedad, mediante un modelo de regresión lineal.

---

## Descripción del conjunto de datos

El conjunto de datos usado es **Trending YouTube Video Statistics**, un registro diario de los videos en tendencia de YouTube, obtenido originalmente de Kaggle y adaptado por el curso para este proyecto.

* **Archivos en carpeta data:** `DEvideos_cc50_202101.csv` y `DE_category_id.json`
* **Periodo cubierto:** noviembre 2017 – junio 2018
* **Columnas principales:** `video_id`, `trending_date`, `title`, `channel_title`, `category_id`, `publish_time`, `views`, `likes`, `dislikes`, `comment_count`, `comments_disabled`, `ratings_disabled`, `video_error_or_removed`

*Nota: Durante la fase de Preparación de los Datos se identifican y corrigen los problemas de calidad correspondientes a filas incompletas o registros con fechas inconsistentes (el detalle de la limpieza se documenta en el notebook).*

---

## Conclusiones principales

* **Predominancia:** Los videos de la categoría de entretenimiento suelen tener un volumen de apariciones significativamente mayor en las tendencias alemanas.
* **Interacción:** La categoría de música destaca por acumular un alto volumen bruto de likes, mientras que la categoría de viajes muestra un ratio de aceptación más eficiente (likes/dislikes).
* **Comportamiento temporal:** El periodo procesado muestra una tendencia decreciente en cuanto al volumen total de videos capturados en tendencias por mes a lo largo del año.

---

## Licencia de uso

MIT
