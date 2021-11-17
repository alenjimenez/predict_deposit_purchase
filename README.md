# venta-plazo-fijo
Análisis de campaña de marketing bancario para vender plazos fijos.

Este proyecto fue realizado en el contexto del curso de Data Science de Digital House durante 2021.

Es el resultado de un trabajado en equipo que contó con 4 integrantes:
- Alen Jiménez (jimenezalen@gmail.com)
- Luz Fox (luzflor2007@gmail.com)
- Enrique Olmos (e.olmosk@gmail.com)
- Mariano Ayerza (nanoayerza@yahoo.com)

El lenguaje elegido de programación fue Python, que se implementó en Jupyter Lab.

Las notebooks incluidas aquí son ediciones hechas por mí de las presentadas originalmente por el equipo de trabajo.

--------------------------------------------------------------------------------------------

Objetivo: Predecir el éxito de campaña de marketing en nuevos clientes. Se intenta contestar preguntas del estilo "¿A quién llamar?", "¿Cuál es la cantidad óptima de llamadas que reduce el costo total de campaña mientras que maximiza el número de ventas?"

Se explota una base de datos en donde cada fila es un cliente de un banco y las columnas refieren a caracteristicas del mismo cliente, del contacto del banco y del contexto macroeconómico.

--------------------------------------------------------------------------------------------

Las notebooks incluidas son:

- Data Wrangling: 1.desafio_final_grupo3_limpieza
- EDA: 2.desafio_final_grupo3_visualizacion
- Matching Learning (Logístico): 3.desafio_final_grupo3_entrenamiento_logistico

--------------------------------------------------------------------------------------------

Las variables de la base son:

- 1 - age (numeric)
- 2 - job : type of job (categorical: "admin.","blue-collar","entrepreneur","housemaid","management","retired","self-employed","services","student","technician","unemployed","unknown")
- 3 - marital : marital status (categorical: "divorced","married","single","unknown"; note: "divorced" means divorced or widowed)
- 4 - education (categorical: "basic.4y","basic.6y","basic.9y","high.school","illiterate","professional.course","university.degree","unknown")
- 5 - default: has credit in default? (categorical: "no","yes","unknown")
- 6 - housing: has housing loan? (categorical: "no","yes","unknown")
- 7 - loan: has personal loan? (categorical: "no","yes","unknown")
related with the last contact of the current campaign:
- 8 - contact: contact communication type (categorical: "cellular","telephone")
- 9 - month: last contact month of year (categorical: "jan", "feb", "mar", …, "nov", "dec")
- 10 - dayofweek: last contact day of the week (categorical: "mon","tue","wed","thu","fri")
- 11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y="no"). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
other attributes:
- 12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
- 13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
- 14 - previous: number of contacts performed before this campaign and for this client (numeric)
- 15 - poutcome: outcome of the previous marketing campaign (categorical: "failure","nonexistent","success")
social and economic context attributes
- 16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)
- 17 - cons.price.idx: consumer price index - monthly indicator (numeric)
- 18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)
- 19 - euribor3m: euribor 3 month rate - daily indicator (numeric)
- 20 - nr.employed: number of employees - quarterly indicator (numeric)
Output variable (desired target):
- 21 - y - has the client subscribed a term deposit? (binary: "yes","no")
Missing Attribute Values: There are several missing values in some categorical attributes, all coded with the "unknown" label. These missing values can be treated as a possible class label or using deletion or imputation techniques.

