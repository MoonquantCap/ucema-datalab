# Ejercicio 3 · ¿Este vino es bueno? Un clasificador hecho con IA, y auditado

**Data Science 101: Intro y Aplicaciones · UCEMA · Prof. Alfredo B. Roisenzvit**

## El problema

Una bodega quiere saber, a partir de un análisis de laboratorio, si un vino va a ser calificado como **bueno** o **malo** por los catadores. Usted tiene el dataset **Wine Quality** (6.497 vinos portugueses, tintos y blancos, con 11 mediciones físico-químicas y la calificación sensorial simplificada a «Bueno» / «Malo»).

Su tarea: construir un modelo que clasifique cada vino como bueno o malo, evaluarlo con honestidad y recomendarle a la bodega qué modelo usar. Lo que se evalúa no es que la IA haga el trabajo, sino **cómo usted la dirige y la controla**.

## Herramientas

Use **las dos**:

1. **Una IA con análisis de datos** (ChatGPT, Claude, Gemini u otra que pueda leer un archivo y ejecutar código). Es obligatoria: el anexo con la conversación es parte de la entrega.
2. **El Clasificador del Data Lab**: https://ucema-datalab.vercel.app → dataset **Vinos** → botón **Clasificador ◆** (o las preguntas guiadas 9 y 10). Corre en su navegador, sin programar: muestra la exploración de los datos, entrena tres modelos (regresión logística, árbol de decisión y k vecinos), arma la matriz de confusión, permite mover el umbral de decisión y predecir un vino nuevo.

El Data Lab es su **verificación independiente**: calcula las mismas cifras que le dará la IA, con un método que usted controla. Puede trabajar en el orden que prefiera: pedirle el análisis a la IA y contrastarlo con el Data Lab, o hacer los modelos en el Data Lab y pedirle a la IA que los replique, los explique o los critique. Lo que cuenta es que cada cifra importante del informe esté verificada por una segunda vía.

Para darle el dataset a la IA: en el Clasificador, paso 1, botón **«Descargar el dataset completo (CSV) para su IA»**. Es el mismo archivo con el que trabaja el Data Lab (6.497 filas, columna «Calidad» ya simplificada a «Bueno» / «Malo»), así las cifras se pueden comparar.

## Consignas

### 1. Exploración
Pídale a la IA una descripción de los datos: distribuciones de las variables, valores faltantes, **balance de clases** (qué proporción de vinos es «Bueno») y **filas duplicadas**.
- **Verifique al menos dos cifras por su cuenta** con el paso 1 del Clasificador (proporción de «Bueno», medias por clase, faltantes, duplicados) o con la vista Tabla del Data Lab.
- Pista: el dataset tiene filas repetidas. ¿La IA las detectó? ¿Qué hizo con ellas? ¿Por qué importan para medir un modelo?

### 2. Modelos
Entrene **al menos dos modelos distintos** (con la IA, en el Data Lab o en ambos) y compárelos.
- Indique **qué variables usó y por qué**. El paso 1 del Clasificador muestra cuánto se asocia cada variable con la calidad; puede probar con todas y con un subconjunto.
- Evalúe siempre sobre **datos de prueba** que el modelo no vio. Anote el porcentaje de prueba y la semilla para que el resultado se pueda repetir.
- Compare con: **matriz de confusión**, **exactitud** (*accuracy*: aciertos sobre el total), **precisión** (*precision*: de los que el modelo dice «Bueno», cuántos lo son) y **sensibilidad** (*recall*: de los «Bueno» reales, cuántos detecta). Atención: en español «precisión» se usa a veces para la exactitud; aclare a cuál se refiere y verifique a cuál se refiere la IA.
- Compare todo contra la **línea de base**: ¿cuánto acierta un modelo que diga siempre «Malo»? ¿Sus modelos la superan, y en qué métrica?

### 3. Decisión
La bodega quiere **detectar lotes defectuosos** antes de embotellar.
- ¿Cuál es la clase que se quiere detectar? (En el Clasificador puede elegir «Malo» como clase positiva.)
- ¿Qué error le preocupa más: un **falso positivo** o un **falso negativo**? ¿Por qué, en términos de costo para la bodega?
- ¿Qué modelo elegiría y **con qué umbral**? Use el umbral de decisión para mostrar cómo cambia el balance entre los dos errores, y justifique su elección con números de la matriz de confusión.

### 4. Un vino nuevo
Llegó del laboratorio este vino **tinto**:

| Acidez fija | Acidez volátil | Ácido cítrico | Azúcar residual | Cloruros | SO₂ libre | SO₂ total | Densidad | pH | Sulfatos | Alcohol |
|---|---|---|---|---|---|---|---|---|---|---|
| 7,2 g/L | 0,32 g/L | 0,34 g/L | 2,1 g/L | 0,062 g/L | 16 mg/L | 45 mg/L | 0,9952 g/cm³ | 3,30 | 0,70 g/L | 11,6 % vol |

Pida la clasificación a la IA y cárguelo en el paso 4 del Clasificador con cada uno de sus modelos. Informe la **probabilidad** y la **clase** que da cada uno. ¿Coinciden? Si no coinciden, ¿por qué podría ser? ¿Qué le diría a la bodega sobre este vino?

### 5. Auditoría
- Una **afirmación de la IA que comprobó**: qué dijo, cómo lo verificó y qué encontró.
- Una **afirmación de la IA que corrigió**: qué dijo, qué era lo correcto y cómo lo supo.

## Entrega

- **Informe breve** (una a dos páginas) con las respuestas a las cinco consignas. Incluya al menos una matriz de confusión (en el Clasificador: «Descargar resultado (PNG)») y la tabla comparativa de modelos («Descargar tabla (CSV)»).
- **Anexo**: el registro de la conversación con la IA (texto exportado o capturas). Si usó el Data Lab, puede adjuntar el archivo de «Guardar análisis» (.datalab.json): reabre sus modelos tal como los dejó.

## Cómo se califica (todas las tareas)

Se evalúa la **dirección y auditoría del trabajo realizado con IA**:
- claridad del problema planteado;
- pertinencia de las consignas dadas a la IA;
- verificación independiente de los resultados;
- fundamentación de la decisión.
