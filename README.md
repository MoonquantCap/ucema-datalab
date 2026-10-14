# UCEMA Data Lab · Data Science 101

Explorador de datos de la materia **Data Science 101: Intro y Aplicaciones** (MBA, UCEMA), del Prof. Alfredo B. Roisenzvit.

**Usarlo en línea:** https://ucema-datalab.vercel.app

## Qué hace

- Trae dos datasets de clase con preguntas guiadas: Wine Quality (vinho verde, UCI) y departamentos de São Paulo (abril de 2019: precio, expensas, superficie, ambientes, barrio, venta o alquiler y ubicación), cargado tal como viene, sin limpiar.
- Permite cargar cualquier archivo CSV propio. Detecta separador, formato de números (1234.5 o 1.234,5), fechas y tipos de variable, y arma preguntas y hallazgos automáticos.
- Gráficos: tabla y estadística descriptiva, histograma, dispersión con recta de regresión, box plot, barras con agregación, línea (series de tiempo), mapa de calor, matriz de correlación y mapa (si hay latitud y longitud).
- **Clasificador**: entrena un modelo que predice una variable categórica (por ejemplo, la calidad del vino, «Bueno» o «Malo») a partir de las demás. Tiene cuatro pasos:
  1. **Exploración**: balance de clases, línea de base, faltantes, duplicados y la asociación de cada variable con la clase.
  2. **Variables y validación**: elección de variables, quitar duplicados, división estratificada en entrenamiento y prueba con semilla reproducible.
  3. **Modelo y métricas**: regresión logística, árbol de decisión o k vecinos; matriz de confusión, exactitud, precisión, sensibilidad, F1 y AUC; umbral de decisión ajustable; pesos, reglas del árbol e importancia de variables; tabla comparativa de modelos exportable (CSV y PNG).
  4. **Predecir un caso nuevo**: probabilidad, clase y explicación de cómo llegó el modelo a esa respuesta.

  Los modelos están escritos a mano en el mismo archivo, sin librerías. Funciona con los datasets de clase y con cualquier CSV que tenga una columna de 2 a 12 categorías.

- **Regresión**: el mismo panel, con una variable numérica a predecir (por ejemplo, el precio). Tres modelos (regresión lineal, árbol de regresión y k vecinos), métricas RMSE, MAE y R² contra la línea de base de predecir el promedio, gráfico de valores predichos contra reales, explicación de cada modelo, comparación exportable y predicción de casos nuevos.
- **Validación cruzada** (clasificación y regresión): entrena el modelo en 5 partes y muestra las métricas de entrenamiento y de prueba de cada una, con promedio y desvío, para detectar sobreajuste.
- **Mapa con contornos**: países de Sudamérica, estados de Brasil y el municipio de São Paulo debajo de los puntos. «Vista: Datos» acerca la vista a la mayoría de los puntos; «Vista: Brasil» muestra todos, incluidas las coordenadas fuera de lugar.
- **Filas**: filtro que analiza sólo una parte de los datos (por ejemplo, «Negotiation Type = rent»). Se aplica a todos los gráficos, la tabla y los modelos, y se guarda con el análisis.
## Ejercicios

- [Ejercicio 3 · Clasificador de vinos con IA, auditado](ejercicios/ejercicio-3-clasificador.md)

## Privacidad

Todo corre en el navegador. Los archivos que se cargan **no se envían a ningún servidor**: la página no hace ninguna llamada de red con los datos. Cada persona que abre el enlace trabaja con su propia copia; nadie más puede ver sus datos.

## Guardar el trabajo

- **Descargar gráfico:** guarda el gráfico actual como imagen PNG. En la vista Tabla, descarga la tabla como CSV.
- **Guardar análisis:** guarda los datos, la vista actual y el clasificador (configuración y modelos de la comparación) en un archivo `.datalab.json` en su computadora.
- **Abrir análisis:** vuelve a abrir ese archivo y recupera datos y vista, sin volver a cargar el CSV.

## Usarlo sin conexión

`index.html` es un único archivo autocontenido (HTML, CSS y JavaScript, sin librerías externas; sólo las tipografías se cargan de Google Fonts, con alternativas locales). Descárguelo y ábralo con doble clic en cualquier navegador moderno.

## El código

Todo el código está en `index.html`, sin minificar: se puede leer, modificar y reutilizar. Los datasets de clase están incluidos en el mismo archivo como JSON.

## Fuentes de datos

- Cortez, P., Cerdeira, A., Almeida, F., Matos, T. y Reis, J. (2009). *Modeling wine preferences by data mining from physicochemical properties*. Decision Support Systems. UCI Machine Learning Repository.
- Departamentos de São Paulo, abril de 2019: archivo `sao-paulo-properties-april-2019.csv` del campus de la materia (13.640 publicaciones de venta y alquiler).
- Contornos del mapa: Natural Earth (dominio público), países y estados de Brasil; límite del municipio de São Paulo: IBGE (malhas territoriales). Simplificados e incluidos en el archivo.
