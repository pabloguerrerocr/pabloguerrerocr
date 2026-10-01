## José Pablo Guerrero Chaves

**Economist · Data analysis and official statistics · Costa Rica**

**[pabloguerrerocr.github.io](https://pabloguerrerocr.github.io)** (interactive dashboards) · [LinkedIn](https://www.linkedin.com/in/pabloguerrerocr) · pabloguerrerocr@gmail.com

*[Español abajo ↓](#-español)*

Bachelor's degree in Economics (Universidad Latina de Costa Rica) and a
Licentiate in progress. I am currently doing my professional internship at the
**Central Bank of Costa Rica**, in the Data Analysis and Statistics Division,
International Accounts Statistics area.

I work at the intersection of applied economics and data analysis: time series,
official statistics, and questions that end in a decision rather than a table.
Every figure I report can be traced back to its source, and gaps are declared as
gaps.

---

### Projects

**U.S. shocks and Costa Rica's external sector, 2015–2025** *(private — thesis in progress)*
Does Costa Rica feel the United States through trade or through the Fed's policy
rate? Three VAR/VECM blocks on public data from FRED and the Central Bank of
Costa Rica. **The financial channel dominates the real one in all 14**
variable-horizon combinations. At 24 months, the federal funds rate explains
**44.4 %** of the variance in international reserves and **43.2 %** of the real
effective exchange rate; the U.S. industrial cycle explains 3.3 % and 4.5 %.
Unit root tests flagging ambiguous cases, Engle-Granger and Johansen
cointegration, Granger causality, bootstrapped impulse responses and variance
decomposition. Reproducible end to end.

**[Data warehouse and quality engine for macro time series](https://github.com/pabloguerrerocr/warehouse-sector-externo)**
DuckDB star schema over a macroeconomic panel, with **proof that moving the data into
SQL did not alter a single number**: 18 series reconcile against the validated
Python pipeline. The Central Bank publishes trade figures accumulated within the
year; deaccumulation is done in SQL with a window partitioned by year and
reconciles to `5.7e-14`. The transformations also ship as a **dbt** project — same rows, verified with
`EXCEPT` in both directions — so lineage comes from `ref()` and the tests run
inside the graph. Seven data-quality checks that return the failing rows,
not a boolean — 0 errors and 3 warnings on this data, all three genuine
macroeconomic shocks rather than capture errors.

**[Costa Rica and its partners do not report the same trade](https://github.com/pabloguerrerocr/brecha-espejo-cr)** · [interactive dashboard](https://pabloguerrerocr.github.io/brecha/)
In 2024 Costa Rica declared **$19.9 bn** in exports; its partners declared importing
**$34.0 bn** from Costa Rica. The **$14.1 bn** mirror gap is not noise: it holds for
ten straight years, never drops below 25 %, and grew from 44 % to 71 %. Three
partners explain half of it, and each one is a different phenomenon — the United
States a stable **+17.3 %** level shift, China a **+627 %** gap with a standard
deviation of 396, Belgium a **−37.7 %** gap that is the most stable of all. The
analysis runs in SQL over DuckDB.

**[Costa Rica's trade concentrated, it did not diversify](https://github.com/pabloguerrerocr/comercio-exterior-cr)** · [interactive dashboard](https://pabloguerrerocr.github.io/comercio/)
Exports more than doubled between 2010 and 2024 — and became far more dependent on
one country and one product. The share going to the United States rose from 37.4 %
to **47.9 %**, the Herfindahl index of destinations from 0.160 to **0.248**, and
harmonized-system chapter 90 (medical and precision instruments) alone accounts for
**70.5 %** of the entire increase. UN COMTRADE data, with a Power BI model.

**[Diagnostic engine for time-series blocks](https://github.com/pabloguerrerocr/motor-series)**
Declare the block in a config file — which series, which transformation, which
specification — and the engine runs the full battery: ADF and KPSS **flagging where
they contradict each other**, lag selection across four criteria, Engle-Granger and
Johansen, and sample slack against the ten-observations-per-parameter rule. What makes
it useful is that **it warns instead of obeying**: ask for a VECM on series that do not
cointegrate and it estimates it anyway, with the warning on top of the report. It
deliberately does not choose the specification, the Cholesky ordering, or what to do
when the unit-root tests disagree — those are economic calls, and the engine's job is
to make explicit what each one costs.

**[The naive benchmark is hard to beat, and almost nobody reports it](https://github.com/pabloguerrerocr/portfolio-data-analytics)** · [interactive dashboard](https://pabloguerrerocr.github.io/nowcast/)
Nowcasting Costa Rica's quarterly GDP from OECD short-term indicators. The
nowcast cuts the error **30.6 %** against repeating last quarter — the benchmark
everyone publishes — but only **6.5 %** against the historical mean, which is the
one that decides whether the model adds anything. An earlier version showed
+13.7 %; excluding 2020 it collapsed to +0.6 %, so the entire result was the
pandemic. Both numbers are in the README, with the R² of 0.154 and the quarter
the model missed by 8.7 points.

**[World population and economy atlas, 2026](https://github.com/pabloguerrerocr/portfolio-data-analytics/tree/main/poblacion-mundial)** · [interactive atlas](https://pabloguerrerocr.github.io/atlas/)
Low and lower-middle income countries hold **45 %** of the world's population and
account for **85 %** of its growth; in **20 countries** population grows faster than
the economy in 2026, so income per person falls. 234 countries, 18 indicators,
World Bank and IMF data refreshed **automatically every month** by GitHub Actions,
with internal consistency checks that stop the pipeline if the source contradicts
itself.

**[Automated monthly bookkeeping close from Costa Rica's electronic invoices](https://github.com/pabloguerrerocr/contaflow)**
A folder of Hacienda XML invoices (versions 4.3 and 4.4) goes in; the Excel the
client signs and the figure for VAT Form 150 come out. Rule-based classification,
double-entry journal with input and output VAT kept apart, and one invariant: the
journal imbalance must be **0.00**. On the demo set (88 documents, 149 lines)
**94 %** is automated; anything no rule recognises goes to a suspense account and
an exceptions sheet — the tool warns instead of guessing.

**[Backtest audit: how much return survives costs, overfitting and look-ahead](https://github.com/pabloguerrerocr/backtester-mt5)**
Five popular trading models turned into mechanical rules and measured on five
markets with real MetaTrader 5 data and retail costs. **0 of 25** author
configurations show a statistical edge after costs; across **1,120** variants,
in-sample and out-of-sample results correlate at **+0.09**, and 11 of the 14 best
variants lose out of sample. Along the way: a demo price feed frozen for three
months, detected and excluded with an objective rule. 44 automated tests.

---

### Tools

`Python` · `pandas` · `numpy` · `statsmodels` · `SQL` · `DuckDB` · `dbt` · `Power BI` ·
`Excel / Power Query` · `D3.js` · `GitHub Actions` · `Git`

**Methods:** time series, VAR/VECM, cointegration tests (Engle-Granger,
Johansen), Granger causality, regression models.

**Official statistics:** balance of payments (BPM6), OECD Benchmark Definition
(BD4), foreign direct investment, international accounts.

---

### How I work

- The finding comes first, with a number.
- Limitations are declared. A result that does not survive scrutiny is a
  finding, not a failure to hide.
- Public data only, with reproducible downloads from the code itself.

📍 Costa Rica · Native Spanish, C1 English
[LinkedIn](https://linkedin.com/in/pabloguerrerocr) · pabloguerrerocr@gmail.com

---
---

## 🇨🇷 Español

**Economista · Análisis de datos y estadísticas · Costa Rica**

Bachillerato Universitario en Economía (Universidad Latina de Costa Rica) y
Licenciatura en curso. Actualmente realizo mi práctica profesional en la División de
Análisis de Datos y Estadísticas del **Banco Central de Costa Rica**, en el área de
Estadísticas de Cuentas Internacionales.

Trabajo en la intersección entre economía aplicada y análisis de datos: series de
tiempo, estadística oficial y preguntas que terminan en una decisión, no en una tabla.

### Proyectos

**EE. UU. y el sector externo de Costa Rica, 2015–2025** *(privado — TFG en curso)*
¿Costa Rica siente a Estados Unidos por el comercio o por la tasa de la Fed? Tres
bloques VAR/VECM sobre datos de FRED y del portal público del BCCR. **El canal
financiero domina al real en las 14 combinaciones de variable y horizonte.** A 24
meses, la tasa de fondos federales explica el **44,4 %** de la varianza de las
reservas internacionales y el **43,2 %** del tipo de cambio efectivo real; el ciclo
industrial estadounidense, 3,3 % y 4,5 %. Pipeline completo: ADF y KPSS marcando
las filas ambiguas, Engle-Granger y Johansen, causalidad de Granger,
impulso-respuesta con banda bootstrap y descomposición de varianza.

**[Warehouse y motor de calidad para series macro](https://github.com/pabloguerrerocr/warehouse-sector-externo)**
Esquema estrella en DuckDB sobre un panel macroeconómico, con **la prueba de que pasar
los datos a SQL no alteró ni un número**: 18 series reconcilian contra el pipeline
validado en Python. El BCCR publica el comercio acumulado dentro del año; la
desacumulación se hace en SQL con una ventana particionada por año y reconcilia a
`5,7e-14`. Las transformaciones también están como proyecto **dbt** —mismas filas, verificado
con `EXCEPT` en ambas direcciones—, así que el linaje sale de `ref()` y las pruebas
corren dentro del grafo. Siete chequeos de calidad que devuelven las filas que fallan — 0 errores
y 3 avisos, y los tres avisos son choques macro reales, no errores de captura.

**[Costa Rica y sus socios no reportan el mismo comercio](https://github.com/pabloguerrerocr/brecha-espejo-cr)** · [tablero interactivo](https://pabloguerrerocr.github.io/brecha/)
En 2024 Costa Rica declaró exportar **$19,9 mm**; sus socios declararon haber
importado **$34,0 mm**. Los **$14.140 millones** de brecha espejo no son ruido:
existen los diez años, nunca bajan de 25 % y pasaron de 44 % a 71 %. Tres socios
explican la mitad y cada uno es un fenómeno distinto — Estados Unidos un desnivel
estable de **+17,3 %**, China una brecha de **+627 %** con desviación de 396,
Bélgica una brecha de **−37,7 %** que es la más estable de todas. El análisis
corre en SQL sobre DuckDB.

**[El comercio exterior de Costa Rica se concentró, no se diversificó](https://github.com/pabloguerrerocr/comercio-exterior-cr)** · [tablero interactivo](https://pabloguerrerocr.github.io/comercio/)
Las exportaciones más que se duplicaron entre 2010 y 2024 — y se volvieron mucho
más dependientes de un país y de un producto. Lo destinado a Estados Unidos pasó
de 37,4 % a **47,9 %**, el índice Herfindahl de destinos de 0,160 a **0,248**, y
el capítulo 90 del sistema armonizado (instrumentos médicos y de precisión)
explica por sí solo el **70,5 %** de todo el aumento. Datos de UN COMTRADE, con
modelo en Power BI.

**[Motor de diagnóstico para bloques de series de tiempo](https://github.com/pabloguerrerocr/motor-series)**
Se declara el bloque en un archivo de configuración —qué series, qué transformación,
qué especificación— y el motor corre la batería completa: ADF y KPSS **marcando dónde
se contradicen**, selección de rezagos por cuatro criterios, Engle-Granger y Johansen,
y la holgura muestral contra la regla de diez observaciones por parámetro. Lo que lo
hace útil es que **advierte en vez de obedecer**: si se le pide un VECM sobre series
que no cointegran, lo estima igual y deja la advertencia arriba del reporte. No decide
la especificación, ni el orden de Cholesky, ni qué hacer cuando las pruebas de raíz
unitaria discrepan: son decisiones económicas, y el trabajo del motor es dejar
explícito lo que cuesta cada una.

**[El referente ingenuo es difícil de vencer, y casi nadie lo reporta](https://github.com/pabloguerrerocr/portfolio-data-analytics)** · [tablero interactivo](https://pabloguerrerocr.github.io/nowcast/)
Nowcasting del PIB trimestral de Costa Rica con indicadores de coyuntura de la
OCDE. El nowcast reduce el error **30,6 %** frente a repetir el trimestre anterior
—el referente que todos publican— pero solo **6,5 %** frente al promedio histórico,
que es el que decide si el modelo aporta algo. Una versión previa daba +13,7 %;
excluyendo 2020 caía a +0,6 %, o sea que todo el resultado era la pandemia. Ambos
números están en el README, con el R² de 0,154 y el trimestre que el modelo erró
por 8,7 puntos.

**[Atlas de población y economía 2026](https://github.com/pabloguerrerocr/portfolio-data-analytics/tree/main/poblacion-mundial)** · [atlas interactivo](https://pabloguerrerocr.github.io/atlas/)
Los países de ingreso bajo y medio-bajo tienen el **45 %** de la población mundial y
aportan el **85 %** de su crecimiento; en **20 países** la población crece más rápido
que la economía en 2026, así que el ingreso por persona cae. 234 países, 18
indicadores, datos del Banco Mundial y el FMI que se **actualizan solos cada mes** con
GitHub Actions, con chequeos de coherencia que detienen el proceso si la fuente se
contradice.

**[Cierre contable mensual automatizado desde la factura electrónica](https://github.com/pabloguerrerocr/contaflow)**
Entra una carpeta de XML de Hacienda (versiones 4.3 y 4.4); sale el Excel que el
cliente firma y el número del Formulario 150 de IVA. Clasificación por reglas,
partida doble con IVA acreditable y por pagar separados, y un invariante: el
descuadre del diario tiene que dar **0,00**. En el set de demo (88 comprobantes,
149 líneas) se automatiza el **94 %**; lo que ninguna regla reconoce va a una
cuenta puente y a una hoja de excepciones: la herramienta avisa en vez de adivinar.

**[Auditoría de backtests: cuánto retorno sobrevive a costos, sobreajuste e información futura](https://github.com/pabloguerrerocr/backtester-mt5)**
Cinco modelos de trading populares llevados a reglas mecánicas y medidos en cinco
mercados con datos reales de MetaTrader 5 y costos retail. **0 de 25**
configuraciones de autor tienen ventaja estadística después de costos; en
**1.120** variantes, el resultado dentro y fuera de muestra correlaciona a
**+0,09**, y 11 de las 14 mejores variantes pierden fuera de muestra. En el camino:
un feed de precios de la demo congelado tres meses, detectado y excluido con una
regla objetiva. 44 pruebas automatizadas.

### Herramientas

`Python` · `pandas` · `numpy` · `statsmodels` · `SQL` · `DuckDB` · `dbt` · `Power BI` ·
`Excel / Power Query` · `D3.js` · `GitHub Actions` · `Git`

**Métodos:** series de tiempo, VAR/VECM, pruebas de cointegración (Engle-Granger,
Johansen), causalidad de Granger, modelos de regresión.

**Estadística oficial:** balanza de pagos (MBP6), OCDE Benchmark Definition (BD4),
inversión extranjera directa, cuentas internacionales.

### Cómo trabajo

- El hallazgo va primero, con número.
- Las limitaciones se declaran. Un resultado que no sobrevive al escrutinio es un
  hallazgo, no un fracaso que esconder.
- Datos públicos, con descarga reproducible desde el propio código.

📍 Costa Rica · Español nativo, inglés C1
[LinkedIn](https://linkedin.com/in/pabloguerrerocr) · pabloguerrerocr@gmail.com
