# FDS-2026-1-3226

## Integrantes del grupo y roles

| Código | Nombre | Rol | Fase(s) de mayor participación |
| :--- | :--- | :--- | :--- |
| U20231H075 | Alvaro Jerry Rivera Calderón | Business Project Sponsor | Comprensión del negocio, Conclusiones de negocio |
| U202322704 | Ericks Santiago Alarcon Castellanos | Data Engineer | Preparación de los datos, limpieza y feature engineering |
| U202315231 | Mariana Alexa Rafael Sosa | Data Science | Modelado, Evaluación de resultados |
| U202413604 | Ronal Sebastian Cueto Ninaja | Data Analyst | Comprensión y exploración de los datos, visualizaciones |

---

## Objetivo del proyecto

Una consultora internacional con sede en Lima requiere desarrollar un proyecto de Ciencia de Datos para conocer las tendencias de los videos de YouTube en siete países, a solicitud de una empresa de marketing digital. Este repositorio desarrolla el análisis correspondiente al conjunto de datos de **Alemania (DE)**, aplicando la metodología CRISP-DM para:

* Crear conocimiento y valor a partir de los datos de tendencias de YouTube en Alemania, fundamentando decisiones de marketing digital basadas en evidencia.
* Determinar qué categorías, canales y estados concentran mayor tendencia y mayor interacción del público.
* Evaluar la factibilidad de predecir el número de vistas (alcance) de un video a partir de sus señales tempranas de interacción mediante modelos de regresión supervisada.

---

## Descripción del conjunto de datos

Se trabajó con el dataset **Trending YouTube Video Statistics**, específicamente los archivos correspondientes al mercado alemán:

* **Archivos en carpeta data:** `DEvideos_cc50_202101.csv` (40,840 registros, 20 columnas) y el catálogo de categorías `DE_category_id.json`.
* **Periodo cubierto:** 14 de noviembre de 2017 al 14 de junio de 2018.
* **Métricas analizadas:** `views` (variable objetivo), `likes`, `dislikes`, `comment_count` y variables derivadas como `days_to_trend` e `like_dislike_ratio`.

*Nota: Durante la fase de preparación de datos, se realizó un proceso de limpieza (manejo de descripciones nulas, corrección de inconsistencias temporales en `days_to_trend`) y se aplicó una transformación logarítmica (log1p) para mitigar la fuerte asimetría de los datos virales.*

---

## Modelado y Evaluación

Se abordó el problema como una tarea de regresión supervisada. El modelo principal desarrollado superó con creces a la línea base:

* **Regresión Lineal (Línea Base):** $R^2 = 0.77$
* **Random Forest Regressor:** $R^2 = 0.87$

El modelo **Random Forest** logró explicar cerca del **87% de la varianza** en el conjunto de prueba. Las variables con mayor peso predictivo resultaron ser `log_dislikes` y `log_likes`, confirmando que el volumen de interacción es el indicador más robusto para estimar el alcance final de un video.

---

## Conclusiones de Negocio

* **Volumen de tendencias:** Las categorías `Entertainment`, `People & Blogs` y `News & Politics` concentran la mayor cantidad de apariciones en tendencias en Alemania, siendo ideales para maximizar exposición masiva.
* **Afinidad de Marca:** Los videos de `Music`, `Movies` y `Nonprofits & Activism` registran el promedio más alto de 'Me gusta', lo que los vuelve altamente atractivos para campañas de branding emocional.
* **Seguridad de Marca:** Las categorías `Pets & Animals`, `Autos & Vehicles` y `Travel & Events` presentan los menores niveles de polarización (mejor ratio likes/dislikes), representando entornos más seguros para anunciantes que buscan minimizar riesgos reputacionales.

---

## Licencia de uso

MIT
