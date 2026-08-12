# Diseño Experimental con Helicópteros de Papel

Trabajo práctico de diseño y análisis estadístico experimental, aplicado a la caracterización del tiempo de vuelo y peso de helicópteros de papel bajo distintas condiciones constructivas.

Trabajo práctico de la materia **Estadística Aplicada (11.67)** — ITBA. Trabajo grupal (4 integrantes). Análisis realizado con **Minitab**.

## Estructura del experimento

El trabajo se desarrolla en 4 partes, de complejidad creciente:

1. **Análisis de 1 muestra**: caracterización estadística de 60 helicópteros de un único modelo constructivo (estadística descriptiva, estimación por intervalos de confianza, validación de supuestos de normalidad e independencia).
2. **Comparación de 2 muestras independientes**: comparación del modelo original contra un "modelo retador" fabricado con papel de otra densidad (prueba t de Welch, prueba F para igualdad de varianzas).
3. **Comparación de más de 2 muestras independientes**: comparación de 4 tipos de papel mediante **ANOVA de un factor** y comparaciones múltiples de **Tukey**.
4. **Análisis de correlación y regresión lineal**: modelo de regresión del tiempo de vuelo en función de la longitud de corte y el número de clips, con depuración del modelo por **multicolinealidad** (criterio jerárquico basado en VIF).

## Principales hallazgos

- El tipo de papel tiene un efecto **estadísticamente significativo** tanto en el tiempo de vuelo como en el peso del helicóptero (ANOVA, p < 0,001 en ambos casos), aunque el efecto es mucho más determinante sobre el peso (R² = 99,15%) que sobre el tiempo de vuelo (R² = 68,06%).
- El peso resultó sistemáticamente una variable más controlada (menor variabilidad relativa) que el tiempo de vuelo a lo largo de todo el experimento.
- El modelo de regresión depurado (`Tiempo de vuelo = 445 − 1,169·Longitud de corte − 23,67·N° de clips`) muestra que tanto una mayor longitud de corte como un mayor número de clips reducen el tiempo de vuelo, resultado consistente con la física del helicóptero (mayor peso y geometría de ala modificada).
- Se detectó y corrigió multicolinealidad severa en el modelo de regresión inicial mediante eliminación jerárquica de términos no significativos.

## Enfoque técnico

- Estadística descriptiva (medidas de tendencia central, dispersión, forma, detección de outliers por criterio de Tukey).
- Inferencia estadística: intervalos de confianza, pruebas t (Welch y pooled), prueba F para varianzas, prueba de normalidad de Kolmogorov-Smirnov, prueba de Levene.
- Diseño experimental: modelos "one-way", ANOVA, comparaciones múltiples de Tukey.
- Regresión lineal múltiple con términos cuadráticos, diagnóstico de multicolinealidad (VIF) y depuración de modelo.
- Análisis y validación de residuos (independencia, normalidad, homocedasticidad) en cada etapa.

## Estructura del repositorio

```
informe_helicopteros_papel.pdf   → informe completo del trabajo práctico
```

*(El análisis se realizó en Minitab; el repositorio contiene el informe con el desarrollo completo, tablas de salida y gráficos, no código fuente.)*
