# 🎮 Análisis Exploratorio de Ventas de Videojuegos

## Descripción del proyecto

Este proyecto forma parte del máster en análisis de datos y tiene como objetivo realizar un **análisis exploratorio** de un conjunto de datos utilizando **Google Sheets**, visualizando los resultados en un **dashboard**, y documentando todo el proceso de transformación, limpieza y análisis descriptivo.

El dataset elegido contiene información sobre ventas de videojuegos por título, plataforma, año, género, editor y ventas por región (Norteamérica, Europa, Japón y globales).

---

## Contenido del repositorio

- `README.md`: Este documento, que explica el proceso completo.
- `video_games_sales.csv`: Archivo original con los datos analizados.
- URL de la hoja de Google Sheets (ver abajo).

---

## Fuente de los datos

- [Kaggle Dataset: Video Game Sales](https://www.kaggle.com/datasets/gregorut/videogame-sales-with-ratings](https://www.kaggle.com/datasets/ulrikthygepedersen/video-games-sales))
- Archivo trabajado: `video_games_sales.csv`

---

## Herramientas utilizadas

-  **Google Sheets** para limpieza, transformación, análisis y dashboard.
-  Funciones como: `IF()`, `ISNUMBER()`, `COUNTIF()`, `QUERY()`, `SUM()`, `AVERAGE()`
-  Tablas dinámicas y gráficos (barras, líneas, pastel)
-  Filtros y segmentación de datos

---

##  Transformación y limpieza de datos

1. **Celdas vacías** en las columnas `Year` y `Publisher`:
   - Rellenadas con `"Not Specified"` (no Unknown ya que existen editores llamados `"Unknown"`).

2. **Creación de nuevas variables**:
   - `Decade`: derivada de `Year` usando fórmula `=IF(ISNUMBER(D2), INT(D2/10)*10 & "s", "Not Specified")`.

3. **Duplicados con ventas distintas**:
   - Se conservaron porque representan lanzamientos multi-región o multiplataforma con ventas separadas.

---

## Análisis descriptivo

Se realizaron las siguientes exploraciones con tablas dinámicas y fórmulas:

1. **Total de ventas globales por plataforma**
2. **Total de ventas por género**
3. **Ventas por año**
4. **Top videojuegos por ventas globales**
5. **Promedio de ventas por región**
6. **Juegos más vendidos por década**

---

## Dashboard

Se ha creado un dashboard en Google Sheets que muestra:

- Gráfico circular: Ventas por plataforma
                    Ventas por género
- Gráfico barras: Participación de ventas por región
                  Ventas globales por año
- Línea temporal: Evolución de ventas por décadas

Enlace al dashboard:  
🔗 [Google Sheets - Video Game Sales Dashboard (modo lectura)]((https://docs.google.com/spreadsheets/d/1rZN-74t_IDJFLd0j2Jyu0D5LVOxKELAAQDH31E8MNCU/edit?usp=sharing))

---

## Conclusiones clave

- **Las plataformas con más ventas** fueron PS2, X360 y PS3.
- **El género más vendido** fue Action, seguido de Sports.
- **2008 y 2009** fueron los años con mayor volumen de ventas.
- **Norteamérica** representa la mayor parte de las ventas globales (~49%).
- Existen múltiples juegos con el mismo nombre pero distintas cifras de ventas, lo cual refleja su rendimiento en diferentes plataformas.

---

## Recomendaciones para trabajos futuros

- Unir los datos con ratings de crítica y usuarios para estudiar correlaciones.
- Realizar análisis de clustering por género y región.
- Visualizar relaciones entre editoras y tipos de juegos más vendidos.

