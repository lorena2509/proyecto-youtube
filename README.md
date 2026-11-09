# Proyecto estadísticas de YouTube (PLN)

Universidad de Cundinamarca, Extensión Facatativá. Machine learning y algoritmos genéticos / Procesamiento de lenguaje natural. Docente: Fredy Martinez.

Integrantes (máximo 3): [COMPLETAR]

## Qué hace el proyecto

Analiza `comments.csv` (comentarios) y `videos-stats.csv` (estadísticas de videos) con PLN en Google Colab:

1. **Cuaderno 1:** clasifica el sentimiento de los comentarios (TF-IDF + regresión logística). F1 macro de 66,1 y exactitud de 73,5 % en el conjunto de prueba.
2. **Cuaderno 2:** agrupa títulos de videos (TF-IDF + LSA + k-medias). Silueta de 0,078 con K = 4 y de 0,107 con K = 6.
3. **Cruce por Video ID:** relaciona sentimiento y visualizaciones (Spearman rho = 0,143). Es una asociación, no una causa.
4. **Mejoras (cuaderno 04):** emojis + n-gramas de caracteres suben el F1 macro de 66,1 a 70,4 en la prueba (IC 95 % de la diferencia: +3,1 a +5,7 puntos). Las palabras vacías de dominio no mejoraron la agrupación de títulos.
5. **Etapa 3:** segmentación de clientes con K-Means (ejercicio con datos ficticios). Silueta de 0,611 con K = 3 y de 0,585 con K = 2.

## Estructura

```
notebooks/            cuadernos de Colab (.ipynb); el 04 ya trae salidas
notebooks_ejecutados/ cuadernos 01 a 03 ejecutados con los datos (referencia)
data/        archivos CSV
results/              salidas de K-Means y PDFs generados por los cuadernos (results/youtube)
docs/        informes en PDF
```

## Cómo ejecutarlo en Google Colab

1. Abre el cuaderno desde GitHub: en Colab, Archivo > Abrir cuaderno > GitHub, y pega la URL de este repositorio.
2. Ejecuta las celdas en orden. Cuando pida archivos, sube los CSV de `data/`.
3. Dependencias (ya vienen en Colab): ver `requirements.txt`.

## Enlaces a Colab

- Cuaderno 1 (comentarios y sentimiento): notebooks/01_PLN_Comentarios_YouTube.ipynb
- Cuaderno 2 (títulos y estadísticas): notebooks/02_PLN_Titulos_y_Estadisticas_YouTube.ipynb
- Sentimientos y alcance: notebooks/03_PLN_Sentimientos_y_Alcance.ipynb
- Mejoras (emojis, caracteres, K): notebooks/04_PLN_Mejoras.ipynb
- Segmentación K-Means: notebooks/Segmentacion_KMeans.ipynb

## Notas

- Los datos de YouTube no se modifican; las etiquetas de sentimiento no fueron verificadas por personas.
- Los resultados describen esta muestra y no prueban relaciones causales.
