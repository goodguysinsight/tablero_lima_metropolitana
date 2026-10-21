# Tablero Lima Metropolitana en cifras — Compendio Estadístico 2025 (INEI)

Tablero interactivo y autocontenido (`index.html`) organizado por **temáticas**, a partir de los 25 cuadros temáticos del *Compendio Estadístico Lima Metropolitana 2025* (INEI). Elaboración: **Good Guys Insight**.

## Temáticas (pestañas)
| Pestaña | Mapa distrital (43 distritos) | Gráficos |
|---|---|---|
| Territorio y población | Población 2018-2025, densidad, crecimiento 2018-2025 | Población total, hechos vitales |
| Vivienda y servicios | — | Agua y alcantarillado, tipo de vivienda, titulación/hacinamiento, combustible, producción de agua SEDAPAL, TIC |
| Educación y salud | Analfabetismo 2007/2017, educación superior 2017, seguro de salud 2017 | Matrícula, ECE, analfabetismo, años de estudio, seguro, ENDES |
| Empleo y bienestar | Usuarios de Pensión 65 | PEA, tasas laborales, informalidad, pobreza, ingreso y gasto |
| Seguridad ciudadana | Denuncias (absolutas y por 10 mil hab.), serenazgo (absoluto y por 10 mil hab.) | Denuncias totales, percepción de inseguridad, por área interdistrital |
| Economía y empresas | Licencias de funcionamiento, empresas de comercio | VAB por actividad, variación, estructura, empresas por tamaño, parque automotor, turismo |
| Finanzas y precios | Créditos banca múltiple, oficinas de cajas municipales, recaudación municipal por habitante | Inflación, créditos y depósitos, recaudación SUNAT |
| Medio ambiente | Residuos sólidos (total y per cápita) | Residuos totales, PM10 por zona |

Cada pestaña incluye 4 KPI, mapa coroplético con selector de indicador y año, ficha del distrito con serie histórica, ranking distrital, y gráficos con vista de tabla y descarga CSV. Modo claro/oscuro.

## Publicación en GitHub Pages
Subir `index.html` a un repositorio (p. ej. `goodguysinsight/tablero_lima_metropolitana`) y activar **Settings → Pages → Deploy from a branch → main / (root)**.

## Regenerar
```
cd scripts
python build_all.py   # requiere openpyxl; lee los .xlsx de la carpeta del compendio
```
`extract.py` define qué cuadro y qué filas alimentan cada indicador; `template.html` contiene el diseño.

## Notas
- Las tasas por habitante son cálculos propios con la población proyectada al 30 de junio (cuadro 3.11).
- Algunos cuadros del compendio corresponden al departamento de Lima o al total país; se indica en el título.
- Cartografía: RENLIM (SDOT–PCM), referencial. Callao se muestra en gris como contexto.
