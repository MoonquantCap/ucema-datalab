# UCEMA Data Lab · Data Science 101

Explorador de datos de la materia **Data Science 101: Intro y Aplicaciones** (MBA, UCEMA), del Prof. Alfredo B. Roisenzvit.

**Usarlo en línea:** https://ucema-datalab.vercel.app

## Qué hace

- Trae tres datasets de clase con preguntas guiadas: Wine Quality (vinho verde, UCI) y EcoBici 2025 (datos abiertos del GCBA: viajes, serie diaria con clima, usuarios).
- Permite cargar cualquier archivo CSV propio. Detecta separador, formato de números (1234.5 o 1.234,5), fechas y tipos de variable, y arma preguntas y hallazgos automáticos.
- Gráficos: tabla y estadística descriptiva, histograma, dispersión con recta de regresión, box plot, barras con agregación, línea (series de tiempo), mapa de calor, matriz de correlación y mapa (si hay latitud y longitud).

## Privacidad

Todo corre en el navegador. Los archivos que se cargan **no se envían a ningún servidor**: la página no hace ninguna llamada de red con los datos. Cada persona que abre el enlace trabaja con su propia copia; nadie más puede ver sus datos.

## Guardar el trabajo

- **Descargar gráfico:** guarda el gráfico actual como imagen PNG. En la vista Tabla, descarga la tabla como CSV.
- **Guardar análisis:** guarda los datos y la vista actual en un archivo `.datalab.json` en su computadora.
- **Abrir análisis:** vuelve a abrir ese archivo y recupera datos y vista, sin volver a cargar el CSV.

## Usarlo sin conexión

`index.html` es un único archivo autocontenido (HTML, CSS y JavaScript, sin librerías externas; sólo las tipografías se cargan de Google Fonts, con alternativas locales). Descárguelo y ábralo con doble clic en cualquier navegador moderno.

## El código

Todo el código está en `index.html`, sin minificar: se puede leer, modificar y reutilizar. Los datasets de clase están incluidos en el mismo archivo como JSON.

## Fuentes de datos

- Cortez, P., Cerdeira, A., Almeida, F., Matos, T. y Reis, J. (2009). *Modeling wine preferences by data mining from physicochemical properties*. Decision Support Systems. UCI Machine Learning Repository.
- Gobierno de la Ciudad de Buenos Aires, datos abiertos: recorridos y usuarios de EcoBici 2025. Clima: Open-Meteo.
