# Asistente de anuncios para Vinted con IA

Herramienta en Python que escribe anuncios de Vinted a partir de los datos de una prenda, usando la API de Gemini. Es la segunda fase de mi proyecto [Análisis de mis ventas en Vinted](https://github.com/Eugenia311/analisis-vinted), donde descubrí que los artículos sin vender no tenían un precio más alto, sino muy pocas visitas.

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Eugenia311/agente-vinted/blob/main/agente_vinted.ipynb)

## Qué hace

- Escribe título y descripción siguiendo unas normas: no inventar datos, tono cercano, ideas para combinar la prenda y títulos con las palabras que usaría un comprador al buscar.
- Si un modelo está saturado o sin cuota, prueba automáticamente con el siguiente.
- La clave de API se guarda en los secretos de Colab, nunca en el código.

## Experimento: ¿funciona el anuncio nuevo?

Cambié el anuncio de un artículo y dejé otros dos sin cambiar como grupo control. Visitas ganadas en el mismo periodo (9-24 de noviembre de 2026):

| Artículo | Grupo | Visitas por día |
|---|---|---|
| Abrigo de pelo | Anuncio nuevo | ~0,7 |
| Falda plisada | Control | ~0,1 |
| Pantalón palazzo | Control | ~0,1 |

**Primeros resultados:** el artículo con el anuncio nuevo ganó visitas unas 7 veces más rápido que los del grupo control.

**Limitaciones:** es un solo artículo, y además ya era el que más interés despertaba y es un abrigo en temporada de frío. Son resultados preliminares: sigo registrando datos y he añadido un segundo artículo al grupo del anuncio nuevo.

## Herramientas

Python, API de Gemini (`google-genai`), Google Colab, con Claude como apoyo para el aprendizaje.
