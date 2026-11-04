## José Pablo Guerrero Chaves

**Economist · Data analysis and official statistics · Costa Rica**

**[pabloguerrerocr.github.io](https://pabloguerrerocr.github.io)** (interactive dashboards) · [LinkedIn](https://www.linkedin.com/in/pabloguerrerocr) · pabloguerrerocr@gmail.com

*[Español abajo ↓](#-español)*

Bachelor's degree in Economics (Universidad Latina de Costa Rica) and a Licentiate in
progress. I am currently doing my professional internship at the **Central Bank of
Costa Rica**. I turn public economic data into findings that hold up: every figure
traces back to its source, and every limitation is stated.

---

### Economics

- **[How the U.S. reaches Costa Rica's external sector, 2015–2025](https://github.com/pabloguerrerocr/sector-externo-cr-eeuu)** · *my thesis* · [dashboard](https://pabloguerrerocr.github.io/tfg/)
  The Fed's policy rate explains **44.4 %** of the variance of Costa Rica's
  international reserves at 24 months; the U.S. business cycle, **3.3 %**. The financial
  channel wins in **14 of 14** cases, also with an ordering-free decomposition.
  *VAR/VECM in Python, FRED and Central Bank data.*
- **[Costa Rica and its partners do not report the same trade](https://github.com/pabloguerrerocr/brecha-espejo-cr)** · [dashboard](https://pabloguerrerocr.github.io/brecha/)
  In 2024 partners reported importing **$34.0 bn** from Costa Rica, which declared
  **$19.9 bn** in exports. The gap holds for ten straight years and grew from 44 % to
  **71 %**. *SQL on DuckDB.*
- **[Costa Rica's trade concentrated instead of diversifying](https://github.com/pabloguerrerocr/comercio-exterior-cr)** · [dashboard](https://pabloguerrerocr.github.io/comercio/)
  Exports more than doubled in 2010–2024, but the U.S. share rose from 37.4 % to
  **47.9 %** and one product chapter (medical instruments) explains **70.5 %** of the
  increase. *UN COMTRADE, Power BI.*
- **[Nowcasting Costa Rica's GDP: the naive benchmark is hard to beat](https://github.com/pabloguerrerocr/portfolio-data-analytics)** · [dashboard](https://pabloguerrerocr.github.io/nowcast/)
  The nowcast cuts the error **30.6 %** against repeating last quarter but only
  **6.5 %** against the historical mean, and no machine-learning model beats a
  two-variable regression (Diebold-Mariano, p ≥ 0.32). *Python and R.*
- **[World population and economy atlas, 2026](https://github.com/pabloguerrerocr/portfolio-data-analytics/tree/main/poblacion-mundial)** · [atlas](https://pabloguerrerocr.github.io/atlas/)
  Low and lower-middle income countries hold **45 %** of the world's population and
  account for **85 %** of its growth. World Bank and IMF data refreshed every month by
  GitHub Actions.

### Data engineering and analytics

- **[Data warehouse for macro time series](https://github.com/pabloguerrerocr/warehouse-sector-externo)** —
  18 series moved to a DuckDB star schema and a dbt project reconcile with the
  validated Python pipeline to **5.7e-14**; data-quality checks return the failing rows.
  *DuckDB, dbt, SQL.*
- **[Diagnostic engine for time-series blocks](https://github.com/pabloguerrerocr/motor-series)** —
  declare a block in a config file and get unit-root, lag-selection and cointegration
  tests, with a warning wherever the tests contradict each other. *Python, statsmodels.*
- **[Credit card fraud measured in money](https://github.com/pabloguerrerocr/portfolio-data-analytics/tree/main/deteccion-fraude)** —
  on 284,807 real transactions, alerting by expected loss saves **62.0 %** of fraud
  losses against **54.5 %** for the best single threshold. *scikit-learn.*
- **[Automated monthly close from electronic invoices](https://github.com/pabloguerrerocr/contaflow)** —
  Hacienda XML invoices in, the signed Excel and the VAT form out; **9 of 9** real
  invoices reconcile with the totals signed in their XML. *Python.*
- **[Backtest audit](https://github.com/pabloguerrerocr/backtester-mt5)** —
  **0 of 25** popular trading configurations keep a statistical edge after costs;
  in-sample and out-of-sample results correlate at **+0.09**. *Python, MetaTrader 5.*

---

### Tools

`Python` · `pandas` · `numpy` · `statsmodels` · `scikit-learn` · `R` · `SQL` · `DuckDB` · `dbt` · `Power BI` ·
`Excel / Power Query` · `D3.js` · `GitHub Actions` · `Git`

**Methods:** time series, VAR/VECM, cointegration tests (Engle-Granger,
Johansen), Granger causality, regression models, machine learning
(regularization, tree ensembles, time-series cross-validation, imbalanced classification).

**Official statistics:** balance of payments (BPM6), OECD Benchmark Definition
(BD4), foreign direct investment, international accounts.

### How I work

- The finding comes first, with a number.
- Limitations are declared. A result that does not survive scrutiny is a
  finding, not a failure to hide.
- Public data only, with reproducible downloads from the code itself.

📍 Heredia, Costa Rica · Native Spanish, C1 English
[LinkedIn](https://linkedin.com/in/pabloguerrerocr) · pabloguerrerocr@gmail.com

---
---

## 🇨🇷 Español

**Economista · Análisis de datos y estadísticas · Costa Rica**

Bachillerato Universitario en Economía (Universidad Latina de Costa Rica) y
Licenciatura en curso. Actualmente realizo mi práctica profesional en el **Banco
Central de Costa Rica**. Convierto datos económicos públicos en hallazgos que se
sostienen: cada cifra se puede rastrear hasta su fuente y cada limitación se declara.

### Economía

- **[EE. UU. y el sector externo de Costa Rica, 2015–2025](https://github.com/pabloguerrerocr/sector-externo-cr-eeuu)** · *mi trabajo final de graduación* · [tablero](https://pabloguerrerocr.github.io/tfg/)
  La tasa de la Fed explica el **44,4 %** de la varianza de las reservas
  internacionales de Costa Rica a 24 meses; el ciclo económico de EE. UU., el **3,3 %**.
  El canal financiero gana en **14 de 14** casos, también con una descomposición que no
  depende del orden de las variables. *VAR/VECM en Python, datos de FRED y del BCCR.*
- **[Costa Rica y sus socios no reportan el mismo comercio](https://github.com/pabloguerrerocr/brecha-espejo-cr)** · [tablero](https://pabloguerrerocr.github.io/brecha/)
  En 2024 los socios declararon haber importado **$34,0 mm** desde Costa Rica, que
  declaró exportar **$19,9 mm**. La brecha existe los diez años y pasó de 44 % a
  **71 %**. *SQL sobre DuckDB.*
- **[El comercio exterior de Costa Rica se concentró, no se diversificó](https://github.com/pabloguerrerocr/comercio-exterior-cr)** · [tablero](https://pabloguerrerocr.github.io/comercio/)
  Las exportaciones más que se duplicaron entre 2010 y 2024, pero lo destinado a
  Estados Unidos pasó de 37,4 % a **47,9 %** y un solo capítulo (instrumentos médicos)
  explica el **70,5 %** del aumento. *UN COMTRADE, Power BI.*
- **[Nowcasting del PIB de Costa Rica: el referente ingenuo es difícil de vencer](https://github.com/pabloguerrerocr/portfolio-data-analytics)** · [tablero](https://pabloguerrerocr.github.io/nowcast/)
  El nowcast reduce el error **30,6 %** frente a repetir el trimestre anterior, pero
  solo **6,5 %** frente al promedio histórico, y ningún modelo de machine learning le
  gana a una regresión de dos variables (Diebold-Mariano, p ≥ 0,32). *Python y R.*
- **[Atlas de población y economía 2026](https://github.com/pabloguerrerocr/portfolio-data-analytics/tree/main/poblacion-mundial)** · [atlas](https://pabloguerrerocr.github.io/atlas/)
  Los países de ingreso bajo y medio-bajo tienen el **45 %** de la población mundial y
  aportan el **85 %** de su crecimiento. Datos del Banco Mundial y del FMI que se
  actualizan solos cada mes con GitHub Actions.

### Ingeniería de datos y analítica

- **[Warehouse para series macroeconómicas](https://github.com/pabloguerrerocr/warehouse-sector-externo)** —
  18 series llevadas a un esquema estrella en DuckDB y a un proyecto dbt reconcilian
  con el pipeline validado en Python a **5,7e-14**; los chequeos de calidad devuelven
  las filas que fallan. *DuckDB, dbt, SQL.*
- **[Motor de diagnóstico para bloques de series de tiempo](https://github.com/pabloguerrerocr/motor-series)** —
  se declara el bloque en un archivo de configuración y corre las pruebas de raíz
  unitaria, rezagos y cointegración, con una advertencia donde las pruebas se
  contradicen. *Python, statsmodels.*
- **[Fraude con tarjeta medido en dinero](https://github.com/pabloguerrerocr/portfolio-data-analytics/tree/main/deteccion-fraude)** —
  sobre 284.807 transacciones reales, alertar según la pérdida esperada ahorra el
  **62,0 %** del fraude, contra **54,5 %** del mejor umbral único. *scikit-learn.*
- **[Cierre contable mensual desde la factura electrónica](https://github.com/pabloguerrerocr/contaflow)** —
  entran los XML de Hacienda y salen el Excel que firma el cliente y el Formulario 150
  de IVA; **9 de 9** comprobantes reales concilian con el total firmado en su XML. *Python.*
- **[Auditoría de backtests](https://github.com/pabloguerrerocr/backtester-mt5)** —
  **0 de 25** configuraciones de trading populares mantienen ventaja estadística
  después de costos; dentro y fuera de muestra, los resultados correlacionan a
  **+0,09**. *Python, MetaTrader 5.*

### Herramientas

`Python` · `pandas` · `numpy` · `statsmodels` · `scikit-learn` · `R` · `SQL` · `DuckDB` · `dbt` · `Power BI` ·
`Excel / Power Query` · `D3.js` · `GitHub Actions` · `Git`

**Métodos:** series de tiempo, VAR/VECM, pruebas de cointegración (Engle-Granger,
Johansen), causalidad de Granger, modelos de regresión, machine learning
(regularización, ensambles de árboles, validación cruzada temporal, clasificación desbalanceada).

**Estadística oficial:** balanza de pagos (MBP6), OCDE Benchmark Definition (BD4),
inversión extranjera directa, cuentas internacionales.

### Cómo trabajo

- El hallazgo va primero, con número.
- Las limitaciones se declaran. Un resultado que no sobrevive al escrutinio es un
  hallazgo, no un fracaso que esconder.
- Datos públicos, con descarga reproducible desde el propio código.

📍 Heredia, Costa Rica · Español nativo, inglés C1
[LinkedIn](https://linkedin.com/in/pabloguerrerocr) · pabloguerrerocr@gmail.com
