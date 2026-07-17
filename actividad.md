# Actividad de recuperación

## Reporte individual de regresión lineal simple con Python

### Valor

**30 puntos extra**

### Modalidad

**Individual**

Cada estudiante deberá realizar su propio análisis, redactar sus propias interpretaciones y entregar un reporte técnico. No se aceptarán trabajos duplicados o con redacciones idénticas.

### Duración estimada

**2 a 3 horas de trabajo**

---

# Objetivo de la actividad

Aplicar regresión lineal simple con Python para analizar cinco relaciones entre variables cuantitativas, evaluar los supuestos del modelo, interpretar los resultados estadísticos y explicar el uso, alcance y limitaciones de cada modelo.

---

# Dataset

Se utilizará el dataset de salud materna trabajado en clase, el cual contiene variables como:

* `Age`
* `SystolicBP`
* `DiastolicBP`
* `BS`
* `HeartRate`
* `RiskLevel`

La variable `RiskLevel` **no debe utilizarse como variable respuesta** en regresión lineal simple, ya que es una variable categórica.

---

# Instrucciones generales

Cada estudiante deberá construir y analizar **cinco modelos de regresión lineal simple**.

Cada modelo debe tener la forma:

[
Y = b_0 + b_1X
]

Donde:

* (Y) es la variable dependiente.
* (X) es la variable independiente.
* (b_0) es el intercepto.
* (b_1) es la pendiente.

---

# Modelos sugeridos

El estudiante puede proponer sus propios modelos, siempre que utilice variables cuantitativas. También puede usar los siguientes:

| Modelo   | Variable X   | Variable Y    | Pregunta de investigación                                                    |
| -------- | ------------ | ------------- | ---------------------------------------------------------------------------- |
| Modelo 1 | `SystolicBP` | `DiastolicBP` | ¿Existe relación lineal entre la presión sistólica y la presión diastólica?  |
| Modelo 2 | `Age`        | `SystolicBP`  | ¿Existe relación lineal entre la edad y la presión sistólica?                |
| Modelo 3 | `Age`        | `BS`          | ¿Existe relación lineal entre la edad y el nivel de glucosa?                 |
| Modelo 4 | `BS`         | `SystolicBP`  | ¿Existe relación lineal entre el nivel de glucosa y la presión sistólica?    |
| Modelo 5 | `HeartRate`  | `SystolicBP`  | ¿Existe relación lineal entre la frecuencia cardiaca y la presión sistólica? |

---

# Contenido del reporte

El reporte deberá estar libre de código.
Debe incluir tablas, ecuaciones, gráficos, estadísticos e interpretaciones, pero **no debe incluir fragmentos de código dentro del cuerpo principal**.

Todo el código utilizado deberá colocarse al final, en un apartado de **Anexo**.

---

# Estructura del reporte

## 1. Portada

Debe incluir:

* Nombre del estudiante.
* Nombre de la asignatura.
* Nombre de la actividad.
* Fecha de entrega.
* Nombre del dataset utilizado.

---

## 2. Introducción breve

El estudiante deberá explicar, en un párrafo breve, el propósito del análisis.

Debe mencionar que se aplicarán modelos de regresión lineal simple para estudiar posibles relaciones lineales entre variables cuantitativas del dataset.

---

## 3. Descripción general de las variables

Debe incluir una tabla con las variables utilizadas.

| Variable      | Descripción                | Tipo de variable |
| ------------- | -------------------------- | ---------------- |
| `Age`         | Edad de la paciente        | Cuantitativa     |
| `SystolicBP`  | Presión sistólica          | Cuantitativa     |
| `DiastolicBP` | Presión diastólica         | Cuantitativa     |
| `BS`          | Nivel de glucosa en sangre | Cuantitativa     |
| `HeartRate`   | Frecuencia cardiaca        | Cuantitativa     |

---

# 4. Desarrollo de los cinco modelos

Para cada modelo se deberá presentar la siguiente información.

---

## 4.X. Modelo

### a) Pregunta de investigación

Ejemplo:

> ¿Existe relación lineal significativa entre la presión sistólica y la presión diastólica?

---

### b) Variables del modelo

| Elemento                 | Variable |
| ------------------------ | -------- |
| Variable independiente X |          |
| Variable dependiente Y   |          |

---

### c) Gráfico de dispersión con recta de regresión ajustada

El estudiante deberá incluir un gráfico de dispersión donde se observe:

* Los puntos de datos.
* La recta de regresión ajustada.
* Nombre de los ejes.
* Título del gráfico.

---

### d) Ecuación del modelo ajustado

Debe escribirse la ecuación obtenida con los valores numéricos correspondientes:

[
\hat{Y} = b_0 + b_1X
]

Ejemplo:

[
\widehat{DiastolicBP} = 18.45 + 0.52(SystolicBP)
]

---

### e) Interpretación del modelo

El estudiante deberá interpretar:

* El signo de la pendiente.
* El valor de la pendiente.
* El significado del intercepto, cuando tenga sentido.
* Qué representa el modelo en el contexto del problema.

Ejemplo:

> La pendiente indica que, por cada aumento de 1 mmHg en la presión sistólica, la presión diastólica estimada aumenta en promedio 0.52 mmHg.

---

### f) Prueba de hipótesis para la pendiente

Debe plantear:

[
H_0: \beta_1 = 0
]

[
H_1: \beta_1 \neq 0
]

Debe reportar:

| Elemento                | Resultado |
| ----------------------- | --------: |
| Pendiente estimada      |           |
| Valor-p de la pendiente |           |
| Nivel de significancia  |      0.05 |
| Decisión                |           |
| Conclusión contextual   |           |

---

### g) ANOVA del modelo de regresión

Debe incluir la tabla ANOVA del modelo.

| Fuente de variación | Suma de cuadrados | gl | Cuadrado medio |  F | Valor-p |
| ------------------- | ----------------: | -: | -------------: | -: | ------: |
| Regresión           |                   |    |                |    |         |
| Error               |                   |    |                |    |         |
| Total               |                   |    |                |    |         |

También deberá interpretar la prueba F del modelo.

Hipótesis:

[
H_0: \beta_1 = 0
]

[
H_1: \beta_1 \neq 0
]

Interpretación esperada:

> Si el valor-p del ANOVA es menor que 0.05, se rechaza (H_0), por lo que existe evidencia estadística de que el modelo lineal explica una parte significativa de la variabilidad de la variable respuesta.

---

### h) Coeficiente de determinación

Debe reportar e interpretar:

| Estadístico    | Valor |
| -------------- | ----: |
| (R^2)          |       |
| (R^2) ajustado |       |

Interpretación:

> El valor de (R^2) indica qué porcentaje de la variabilidad de la variable dependiente es explicado por la variable independiente.

---

# 5. Evaluación de supuestos por modelo

Para cada uno de los cinco modelos, el estudiante deberá analizar los siguientes supuestos:

---

## 5.1 Linealidad

Debe incluir:

* Gráfico de dispersión.
* Gráfico de residuos contra valores ajustados.
* Comentario sobre si la relación parece aproximadamente lineal.

Puede apoyarse en una prueba como Ramsey RESET, si fue vista en clase o si se desea complementar.

Debe responder:

> ¿El supuesto de linealidad parece razonable para este modelo?

---

## 5.2 Independencia

Debe comentar si las observaciones parecen independientes considerando el contexto del dataset.

También puede apoyarse en el estadístico Durbin-Watson.

Debe reportar:

| Diagnóstico   | Resultado |
| ------------- | --------: |
| Durbin-Watson |           |

Debe comentar:

> ¿Hay evidencia clara de dependencia entre los residuos?

En este dataset, al no tratarse de una serie de tiempo, la independencia debe discutirse principalmente desde el diseño de los datos y no sólo desde el estadístico.

---

## 5.3 Normalidad de los residuos

Debe incluir:

* Histograma de residuos.
* Gráfico Q-Q de residuos.
* Prueba de Shapiro-Wilk u otra prueba de normalidad.

Hipótesis:

[
H_0: \text{Los residuos siguen una distribución normal}
]

[
H_1: \text{Los residuos no siguen una distribución normal}
]

Debe reportar:

| Prueba       | Valor-p | Decisión |
| ------------ | ------: | -------- |
| Shapiro-Wilk |         |          |

Debe comentar las implicaciones:

> Si los residuos no presentan normalidad, las pruebas de hipótesis y los intervalos de confianza pueden verse afectados, especialmente en muestras pequeñas.

---

## 5.4 Homoscedasticidad

Debe incluir:

* Gráfico de residuos contra valores ajustados.
* Prueba de Breusch-Pagan o prueba equivalente.

Hipótesis:

[
H_0: \text{Los residuos tienen varianza constante}
]

[
H_1: \text{Los residuos no tienen varianza constante}
]

Debe reportar:

| Prueba        | Valor-p | Decisión |
| ------------- | ------: | -------- |
| Breusch-Pagan |         |          |

Debe comentar las implicaciones:

> Si no se cumple la homoscedasticidad, los errores estándar, valores-p e intervalos de confianza pueden no ser confiables.

---

# 6. Tabla resumen de supuestos

Después de analizar los cinco modelos, el estudiante deberá incluir una tabla general como la siguiente:

| Modelo   | Linealidad                  | Independencia               | Normalidad                  | Homoscedasticidad           | Comentario general |
| -------- | --------------------------- | --------------------------- | --------------------------- | --------------------------- | ------------------ |
| Modelo 1 | Cumple / No cumple / Dudoso | Cumple / No cumple / Dudoso | Cumple / No cumple / Dudoso | Cumple / No cumple / Dudoso |                    |
| Modelo 2 |                             |                             |                             |                             |                    |
| Modelo 3 |                             |                             |                             |                             |                    |
| Modelo 4 |                             |                             |                             |                             |                    |
| Modelo 5 |                             |                             |                             |                             |                    |

---

# 7. Uso de cada modelo

Para cada modelo, el estudiante deberá explicar cómo se utilizaría.

Debe incluir:

1. Para qué sirve el modelo.
2. Qué variable se necesita conocer.
3. Qué variable permite estimar.
4. Un ejemplo numérico usando la ecuación obtenida.
5. Interpretación del resultado estimado.
6. Advertencia o limitación del uso del modelo.

Ejemplo:

> El modelo permite estimar la presión diastólica a partir de la presión sistólica.
>
> Si una paciente tiene una presión sistólica de 120 mmHg, entonces:
>
> [
> \widehat{DiastolicBP} = 18.45 + 0.52(120)
> ]
>
> [
> \widehat{DiastolicBP} = 80.85
> ]
>
> De acuerdo con el modelo, se estima que una paciente con presión sistólica de 120 mmHg tendría una presión diastólica aproximada de 80.85 mmHg.
>
> Esta estimación debe interpretarse con cuidado, ya que el modelo sólo describe una asociación lineal y no sustituye una valoración médica.

---

# 8. Limitaciones de cada modelo

Para cada modelo, el estudiante deberá explicar sus limitaciones.

Debe considerar:

* Si la relación lineal es fuerte o débil.
* Si el valor de (R^2) es alto o bajo.
* Si se cumplen o no los supuestos.
* Si existen valores atípicos.
* Si el modelo puede usarse para predicción o sólo para describir una relación.
* Por qué no debe interpretarse como causalidad.

---

# 9. Comparación general de modelos

El estudiante deberá elaborar una tabla comparativa final:

| Modelo   | Ecuación | Valor-p pendiente | Valor-p ANOVA | (R^2) | Supuestos cumplidos | Uso principal | ¿Recomendable? |
| -------- | -------- | ----------------: | ------------: | ----: | ------------------- | ------------- | -------------- |
| Modelo 1 |          |                   |               |       |                     |               |                |
| Modelo 2 |          |                   |               |       |                     |               |                |
| Modelo 3 |          |                   |               |       |                     |               |                |
| Modelo 4 |          |                   |               |       |                     |               |                |
| Modelo 5 |          |                   |               |       |                     |               |                |

Después deberá responder:

1. ¿Cuál modelo presentó mejor ajuste?
2. ¿Cuál modelo tuvo mayor (R^2)?
3. ¿Cuál modelo tuvo menor valor-p?
4. ¿Cuál modelo cumplió mejor los supuestos?
5. ¿Cuál modelo recomendarías usar y por qué?
6. ¿Hay algún modelo que no recomendarías usar? ¿Por qué?

---

# 10. Conclusión final

El reporte debe cerrar con una conclusión general que responda:

* Qué modelos fueron analizados.
* Qué relaciones lineales fueron significativas.
* Qué modelo fue el más adecuado.
* Qué tan confiables son los modelos considerando los supuestos.
* Qué limitaciones generales tiene el análisis.
* Por qué los resultados no deben interpretarse como causalidad.

---

# 11. Anexo: código en Python

El código utilizado debe colocarse al final del reporte, en un apartado llamado:

## Anexo: código utilizado en Python

El código debe estar completo, ordenado y comentado.

El cuerpo principal del reporte no debe contener código.

---

# Producto a entregar

El estudiante deberá entregar un archivo PDF que contenga:

1. Portada.
2. Introducción.
3. Descripción de variables.
4. Desarrollo de cinco modelos.
5. Gráficos de dispersión con recta ajustada.
6. Ecuaciones de regresión.
7. Pruebas de hipótesis de la pendiente.
8. ANOVA de cada modelo.
9. Evaluación de supuestos.
10. Explicación de uso de cada modelo.
11. Ejemplo numérico de cada modelo.
12. Limitaciones de cada modelo.
13. Comparación general.
14. Conclusión final.
15. Código en Python como anexo.

---

# Rúbrica de evaluación

| Criterio                                                                          |        Puntos |
| --------------------------------------------------------------------------------- | ------------: |
| Propone correctamente cinco modelos de regresión lineal simple                    |             3 |
| Presenta gráficos de dispersión con recta de regresión ajustada                   |             4 |
| Reporta correctamente ecuaciones, pendientes, valor-p, (R^2) y ANOVA              |             5 |
| Plantea e interpreta correctamente las pruebas de hipótesis                       |             4 |
| Evalúa los supuestos de linealidad, independencia, normalidad y homoscedasticidad |             5 |
| Explica cómo usar cada modelo e incluye un ejemplo numérico                       |             3 |
| Describe las limitaciones de cada modelo                                          |             2 |
| Compara los cinco modelos y justifica cuál es el mejor                            |             2 |
| Presenta un reporte claro, ordenado, sin código en el cuerpo principal            |             1 |
| Incluye el código completo en el anexo                                            |             1 |
| **Total**                                                                         | **30 puntos** |

---

# Restricciones importantes

No se aceptará un reporte que sólo contenga código.

No se aceptará código dentro del cuerpo principal del reporte.

El reporte debe contener tablas, ecuaciones, gráficos, estadísticos e interpretaciones.

El código debe colocarse únicamente en el anexo.

No se debe utilizar `RiskLevel` como variable respuesta.

No se deben afirmar relaciones causales.

El análisis debe hablar de asociación lineal, ajuste del modelo, significancia estadística, cumplimiento de supuestos y limitaciones.
