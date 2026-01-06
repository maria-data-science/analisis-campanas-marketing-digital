# ETAPA 2 – Obtención y comprensión de datos

## 📌 Dataset seleccionado
- **Nombre:** Digital Marketing Metrics & KPIs  
- **Archivo:** Marketing.csv  
- **Fuente:** Kaggle  
- **Link:** https://www.kaggle.com/datasets/sinderpreet/analyze-the-marketing-spending  

El dataset contiene información diaria sobre campañas de marketing digital, incluyendo métricas de alcance, interacción, conversión e ingresos. Los datos permiten analizar el desempeño de distintas campañas y canales con el objetivo de evaluar la eficiencia del gasto publicitario.

---

## 🔍 Comprensión inicial de la estructura del dataset

Antes de utilizar Python o herramientas de visualización, se realizó una exploración conceptual del dataset para comprender su estructura, variables y lógica de negocio.

### Número de variables
El dataset contiene **11 columnas**, relacionadas con campañas de marketing digital.

### Agrupación conceptual de variables
Para facilitar su comprensión, las variables pueden agruparse según su función dentro del proceso de marketing:

**Identificación**
- `id`
- `campaign_id`
- `campaign_name`

**Tiempo**
- `c_date`

**Canal / tipo**
- `category`

**Alcance**
- `impressions`

**Inversión**
- `mark_spent`

**Interacción**
- `clicks`
- `leads`

**Resultado**
- `orders`
- `revenue`

Esta clasificación permite entender el recorrido del usuario a lo largo del embudo de marketing, desde la exposición al anuncio hasta la conversión final.

---

## 📖 Diccionario de datos (explicación conceptual)

A continuación se describe cada variable utilizando un lenguaje comprensible tanto para perfiles técnicos como no técnicos:

- **id**  
  Identificador único de cada registro en el dataset.  
  *Uso analítico:* solo referencia; no aporta valor analítico directo.

- **c_date**  
  Fecha en la que se registró el gasto y el desempeño de la campaña.  
  *Uso analítico:* análisis temporal, tendencias y evolución del rendimiento.

- **campaign_name**  
  Nombre descriptivo de la campaña de marketing.  
  *Uso analítico:* comparación de desempeño entre campañas específicas.

- **category**  
  Canal o tipo de marketing utilizado (social, search, influencer, media).  
  *Uso analítico:* comparación de rendimiento entre distintos canales.

- **campaign_id**  
  Identificador único asignado a cada campaña.  
  *Uso analítico:* agrupar registros de una misma campaña en distintas fechas.

- **impressions**  
  Número de veces que el anuncio fue mostrado a los usuarios.  
  *Uso analítico:* medir alcance y calcular métricas como el CTR.

- **mark_spent**  
  Monto invertido en la campaña durante la fecha registrada.  
  *Uso analítico:* evaluación de costos y cálculo de métricas financieras.

- **clicks**  
  Número de clics recibidos por el anuncio.  
  *Uso analítico:* medir el nivel de interés generado por la campaña.

- **leads**  
  Número de usuarios que dejaron sus datos tras hacer clic.  
  *Uso analítico:* evaluar la conversión de clics a prospectos.

- **orders**  
  Número de ventas o transacciones generadas por la campaña.  
  *Uso analítico:* medir el impacto real de la campaña en ventas.

- **revenue**  
  Ingresos generados por las ventas asociadas a la campaña.  
  *Uso analítico:* análisis de rentabilidad y cálculo de ROI.

---

## 👀 Primera exploración visual del dataset (sin cálculos)

Las siguientes observaciones se basan únicamente en una inspección visual inicial del dataset, sin aplicación de fórmulas o métricas avanzadas.

### Observaciones generales
- Las campañas de tipo **influencer** presentan valores elevados tanto de gasto como de ingresos, destacando por su impacto económico.
- La campaña **youtube_blogger** aparece de forma constante y muestra ingresos significativamente altos, lo que sugiere que podría tratarse de una campaña prioritaria dentro de la estrategia.
- La campaña **banner_partner** presenta volúmenes muy altos de impresiones, pero en varios casos con ingresos bajos o nulos, lo que podría indicar un enfoque más orientado a visibilidad que a conversión.
- La categoría **social** muestra un comportamiento muy variable entre campañas, mientras que **search** parece más estable.
- Algunas campañas, como **instagram_tier2**, presentan muchos clics pero pocas órdenes, lo que podría indicar problemas en la etapa de conversión.

---

## 🧹 Calidad inicial de los datos

Durante la revisión visual inicial se identificaron algunos posibles problemas de calidad de datos:

- Nombres de campañas no estandarizados (por ejemplo: `facebOOK_tier2`).
- Presencia frecuente de valores cero en las variables `orders` y `revenue`.
- La variable `c_date` se encuentra en formato texto y requerirá transformación a formato de fecha.

Estas observaciones indican la necesidad de una etapa de limpieza y normalización antes de realizar análisis métricos.

---

## 🧠 Conclusión de la etapa

En esta etapa se logró comprender la estructura, el significado y el comportamiento general del dataset. La exploración inicial permitió identificar patrones visibles, posibles problemas de calidad de datos y formular hipótesis que serán evaluadas en etapas posteriores mediante métricas específicas y análisis exploratorio en Python.


