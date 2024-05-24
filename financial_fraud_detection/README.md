<a name="readme-top"></a>

![image](https://github.com/estebanferraz1/analysis_and_data_science_portfolio/blob/2654a722df1a1f2545ebf636b4194729c0a64bff/financial_fraud_detection/financial_fraud_detection.jpg)

<h1 align="center"> FINANCIAL FRAUD DETECTION </h1>
<h2>Detección de Fraudes Financieros mediante Machine Learning</h2>

<h2>Descripción del proyecto</h2>
<p align="justify">
Este proyecto se centra en la detección de fraudes en transacciones móviles mediante el uso de técnicas avanzadas de machine learning. Dada la creciente amenaza del fraude en pagos en línea, nuestro objetivo es desarrollar un modelo que pueda distinguir de manera precisa entre transacciones legítimas y fraudulentas, mejorando la seguridad en el sector financiero móvil global.
</p>


<h2>Estado del proyecto</h2>

![Badge en Desarollo](https://img.shields.io/badge/STATUS-%20FINALIZADO-green)
> 

<h2>Tecnologías utilizadas</h2>
<p align="justify">
Python, Pandas, NumPy, Scikit-learn, Matplotlib, PaySim dataset, Google Colab
</p>

<h2>Problema de negocio</h2>

<table><tr><td> 
<p align="justify">
La urgencia por detectar fraudes en transacciones móviles de dinero ha llevado a una empresa del segmento Fintech a buscar soluciones innovadoras.</p>
<p align="justify">
Nuestro objetivo es desarrollar un modelo de machine learning que pueda distinguir de manera precisa entre transacciones legítimas y fraudulentas, estableciendo así un estándar de seguridad en el sector financiero móvil global.
</p>
</td></tr></table>

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<h2>Obtención de datos</h2>
<p align="justify">
Los datos fueron obtenidos de PaySim, que simula transacciones de dinero móvil basadas en una muestra de transacciones reales. Este conjunto de datos incluye detalles como tipo de transacción, montos, balances antes y después de las transacciones.

https://www.kaggle.com/datasets/ealaxi/paysim1
</p>

<h3>Bases de datos</h3>
<p align="justify">
El conjunto de datos contiene las siguientes columnas:

step: Unidad de tiempo en horas.
type: Tipo de transacción (CASH-IN, CASH-OUT, DEBIT, PAYMENT, TRANSFER).
amount: Cantidad de la transacción.
nameOrig: Cliente que inicia la transacción.
oldbalanceOrg: Saldo inicial antes de la transacción.
newbalanceOrg: Saldo nuevo después de la transacción.
nameDest: Cliente que recibe la transacción.
oldbalanceDest: Saldo inicial del receptor antes de la transacción.
newbalanceDest: Saldo nuevo del receptor después de la transacción.
isFraud: Indica si la transacción es fraudulenta.
isFlaggedFraud: Indica intentos de transferir más de $200,000 en una sola transacción.
</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h3>Tratamiento de datos</h3>
<p align="justify">
Limpieza de datos: Eliminación de valores nulos y manejo de valores atípicos.
Normalización: Ajuste de datos a una escala común.
Codificación: Transformación de variables categóricas a numéricas.
Balanceo de clases: Implementación de técnicas de undersampling y oversampling.
</p>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>EDA: Análisis exploratorio de los datos</h2>
<p align="justify">
Realizamos un análisis exhaustivo para identificar patrones y relaciones clave entre las variables:

Frecuencia de transacciones por día
Frecuencia de fraude por rango horario
Frecuencia de fraude por tipo de transacción
Boxplot del monto de transacciones fraudulentas
Matriz de correlaciones
</p>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Insights</h2>
<p align="justify">
Las transacciones fraudulentas representan el 1.05% del total, pero suman $12,056,415,427.84.
Las transacciones de tipo TRANSFER y CASH_OUT son las más propensas a ser fraudulentas.
La mayoría de las transacciones fraudulentas tienen montos ligeramente superiores a $200,000.
El balanceo de datos es crucial para mejorar la precisión del modelo.
</p>

<h3>Resumen y recomendaciones</h3>
<p align="justify">
El modelo de Random Forest ha demostrado ser altamente efectivo, logrando una precisión y recall superiores al 98%. La alta precisión y recall indican que el modelo no solo es bueno para identificar fraudes, sino que también comete pocos errores al clasificar transacciones no fraudulentas como fraudulentas. El AUC-ROC cercano a 1 muestra que el modelo tiene una excelente capacidad para discriminar entre transacciones fraudulentas y no fraudulentas.

Recomendamos:

Implementar el modelo de Random Forest en producción.
Continuar monitoreando el rendimiento del modelo y ajustar según sea necesario.
Explorar el uso de técnicas adicionales de machine learning y deep learning para mejorar aún más la precisión.</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Desarrolladores del proyecto</h2>

- Jorge Perez [@JorgePere27](https://www.github.com/JorgePere27)
- Jhonatan Rodriguez[@JhonatanRC03](https://github.com/JhonatanRC03)
- Esteban Ferraz [@estebanferraz1](https://github.com/estebanferraz1)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Licencia</h2>

Este proyecto está bajo la Licencia MIT - mira el archivo LICENSE.md para mas detalles

> [!NOTE]
> 
> Utilizar con fines educativos.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Contacto</h2>

Esteban F. - estebanferraz@outlook.cl

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Agradecimientos</h2>

Un agradecimiento especial a Alejandro Gamarra y Silvia Branco

[BOOTCAMP XPERIENCE](https://bootcampxperience.com/)

[![](https://img.shields.io/youtube/channel/subscribers/UCuerQOTskuNkddcT738357g?style=for-the-badge&logo=youtube&label=ElProfeAlejo)](https://www.youtube.com/@ElProfeAlejo)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

