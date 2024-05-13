<a name="readme-top"></a>

<h1 align="center"> STORE SALES ANALYSIS </h1>
<h2>Análisis de ventas en una tienda de E-Commerce</h2>

<h2>Índice</h2>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Tabla de Contenidos</summary>
  <ol>
    <li><a href="#Índice">Índice</a></li>
    <li><a href="#Descripción del proyecto">Descripción del proyecto</a></li>
    <li><a href="#Estado del proyecto">Estado del proyecto</a></li>
    <li><a href="#Tecnologías utilizadas">Tecnologías utilizadas</a></li>
    <li><a href="#Problema de negocio">Problema de negocio</a></li>
    <li><a href="#Obtención de datos">Obtención de datos</a></li>
    <li><a href="#Bases de datos">Bases de datos</a></li>
    <li><a href="#Tratamiento de datos">Tratamiento de datos</a></li>
    <li><a href="#EDA: Análisis exploratorio de los datos">EDA: Análisis exploratorio de los datos</a></li>
    <li><a href="Insights">Insights</a></li>
    <li><a href="Resumen y recomendaciones">Resumen y recomendaciones</a></li>
    <li><a href="Desarrolladores del proyecto">Desarrolladores del proyecto</a></li>
    <li><a href="Licencia">Licencia</a></li>
    <li><a href="#Contacto">Contacto</a></li>
    <li><a href="#Agradecimientos">Agradecimientos</a></li>
  </ol>
</details>


<h2>Descripción del proyecto</h2>
<p align="justify">
Este es un proyecto realizado para el desarrollo de habilidades de analítica y ciencia de datos donde se realizó un análisis exhaustivo de los datos de una destacada tienda online situada en Brasil. Nuestro objetivo es responder a preguntas críticas de negocio, explorar profundamente el comportamiento en el mercado nacional y proporcionar insights que promuevan el crecimiento y la optimización de recursos dentro de la organización. A través de un enfoque analítico riguroso, buscamos identificar oportunidades, optimizar operaciones y fortalecer la posición de la tienda en su sector competitivo. Este análisis no solo clarificará los desafíos actuales sino que también, guiará las decisiones empresariales hacia horizontes futuros.
</p>


<h2>Estado del proyecto</h2>

![Badge en Desarollo](https://img.shields.io/badge/STATUS-%20FINALIZADO-green)
> 

<h2>Tecnologías utilizadas</h2>

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) ![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)



<h2>Problema de negocio</h2>

<table><tr><td> 
<p align="justify">
Ante la necesidad imperativa de prever y optimizar el gasto de los usuarios, una prominente empresa de comercio electrónico ha iniciado la búsqueda de soluciones innovadoras. En este contexto, nuestro equipo de científicos de datos ha sido convocado para llevar a cabo un análisis exhaustivo del comportamiento de ventas de la empresa. Este estudio no solo abarcará las operaciones de ventas generales, sino que también se extenderá al desempeño de los vendedores, la dinámica de los productos y las tendencias emergentes del mercado.</p>
<p align="justify">
El objetivo es proporcionar un entendimiento profundo que permita a la empresa no solo anticipar las tendencias futuras, sino también implementar estrategias efectivas para maximizar los beneficios y mejorar la satisfacción del cliente. A través de este análisis, buscamos identificar patrones clave, detectar oportunidades de crecimiento y ofrecer recomendaciones basadas en datos que guíen a la empresa hacia decisiones estratégicas acertadas en su competitivo entorno de mercado.
</p>
</td></tr></table>

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<h2>Obtención de datos</h2>
<p align="justify">
Los datos analizados fueron obtenidos de fuentes internas, esta información se encontraba almacenada en diversos archivos .csv, esta data fue analizada, tratada y procesada para ser utilizada como fuente principal de información.
</p>

<h3>Bases de datos</h3>
<br>
<p>  df_itens_pedidos = pd.read_csv('https://raw.githubusercontent.com/ElProfeAlejo/Bootcamp_Databases/main/itens_pedidos.csv')

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/50e314e0-a2c3-4ba7-b9ce-9cd58be75666)

<p> df_pedidos = pd.read_csv('https://raw.githubusercontent.com/ElProfeAlejo/Bootcamp_Databases/main/pedidos.csv')

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/e236b252-ca59-4c77-bf70-0ab10e1ac915)

<p>df_productos = pd.read_csv('https://raw.githubusercontent.com/ElProfeAlejo/Bootcamp_Databases/main/productos.csv')

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/1f32c945-ead8-4793-8242-69a126194dc3)

<p> df_vendedores = pd.read_csv('https://raw.githubusercontent.com/ElProfeAlejo/Bootcamp_Databases/main/vendedores.csv')</p>

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/198e2636-a8f5-4354-ac73-2af5a590763e)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h3>Tratamiento de datos</h3>
<p align="justify">
En general la información contenida en las bases de datos se encontraba limpia, facilitando el proceso de tratamiento, no se encontraron valores duplicados, escasa cantidad de valores nulos y los tipos de datos tampoco revistieron mayor complejidad en su tratamiento. Se identifican valores 'NAN' en columnas "PRODUCTO" Y "SKU", los datos faltantes son los dos últimos registros lo que podría indica que hubo algún problema en el proceso de registro de esos productos. Esto podría deberse a diversas razones, como errores en la entrada de datos, problemas técnicos durante el registro, o simplemente que esos productos no fueron registrados correctamente en la base de datos. Es importante corregir este tipo de problemas, ya que es fundamental para la integridad de la información. Una posible recomendación inicial sería revisar el proceso de registro de productos para identificar la causa de los posibles fallos y asegurarse de que todos los productos sean registrados de manera adecuada.
</p>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>EDA: Análisis exploratorio de los datos</h2>

<h3>Análisis de la evolución de las ventas</h3>

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/d33979c1-f51f-481c-8f37-be1475f2cf88)

<h3>Análisis de los vendedores</h3>

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/60fc4fe8-45a8-45bb-9adc-caa6264c63f2)
![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/01be4d48-77c6-4376-995a-d4388fa07139)

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/3a417d2e-df58-473c-8d3d-962d14db75f7)
![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/00e9cafc-bc2a-43d2-9709-a1c093c01e81)

<h3>Análisis de los productos</h3>

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/da6ec9b2-51fc-4e93-b363-f82727169284)

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/2a392ef1-dd83-4cb4-a221-e6ab6e9776cc)

![image](https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/6a557211-ff7a-4f8b-8751-86b02f773741)

<h3>Tratamiento de datos con SQLite</h3>

<img src="https://github.com/Xavieroc93/-Store_Sales_Analysis_SQL_FINAL./assets/93497146/5c0591f9-632d-4aa1-9936-1dd5fc0556d9" alt="Tratamiento de datos SQLite" width="500" height="auto">

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Insights</h2>

<h3>¿Cual es el Top 5 productos más vendidos históricamente?</h3>

<img src="https://i.imgur.com/g5DYZYe.png" alt="Top 5 productos" width="500" height="auto">


<h4>Conclusión</h4>

Históricamente el producto más vendido es el producto **Saia Midi
Cinto** con **549** ventas, a pesar de ello el que más ingresos generó
es el producto **Vestido Nude Reta** llegando a los **\$301K**


<h3>¿Cual es la evolución histórica de las ingresos netos?</h3>

<img src="https://i.imgur.com/JzS2aZa.png" alt="Evolución ingresos netos" width="500" height="auto">

<h4>Conclusión</h4>

El análisis de los ingresos netos históricos muestra un valor promedio
de **\$80 mil** de ingresos netos diarios desde el **2020**. También
podemos visualizar en el histórico que el día **24’Nov del
2019**, se reportó un ingreso neto de **\$280 mil** generando por la
venta de algunas marcas famosas.

<h3>¿Cuáles son los ingresos netos por vendedor por año?</h3>

<img src="https://i.imgur.com/2ctUaAP.png" alt="Ingresos netos por vendedor por año" width="500" height="auto">

<h4>Conclusión</h4>

Aunque **Paulo** es el mejor vendedor histórico ha mantenido un nivel de
ventas constante, ya que en el año 2020 fue el que menos vendió, sus
demás compañeros crecieron todos sus ingresos netos destacando a **Ana**
y **Daniel** sobrepasando los **\$5M** en el año en cuestión.


<h3>¿Cuáles son las ciudades que proporcionan mayores ingresos netos?</h3>

<img src="https://i.imgur.com/bIvV7fg.png" alt="Ingresos netos por ciudad" width="500" height="auto">

<h4>Conclusión</h4>

Destacando a las ciudades **Alagoas** y **Pernambuco**, con ingresos
netos superiores a **\$1.5M** durante todo el periodo histórico.
Mientras que **Mato Grosso do Sul** y **Acre** ocupan los últimos
lugares de la lista con ingresos netos inferiores a **\$1.2**, donde se
debe mejorar las acciones de ventas.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h3>Resumen y recomendaciones</h3>
<p align="justify">
* El análisis de la información precedentemente expuesta refleja importantes observaciones sobre la problemática de negocios y su evolución histórica que permite influir en la toma de decisiones estratégicas, con el objeto de impulsar el rendimiento.</p>
<p align="justify">  
* Se analizó la evolución histórica de las ventas por productos, el comportamiento por vendedor y la distribución geográfica a nivel nacional, lo que permite tener un conocimiento cabal del desarrollo histórico de las ventas y la representatividad asociada a cada vendedor y región del país.</p>
<p align="justify">  
* Con el objeto de impulsar el rendimiento, mejorar la eficiencia y reducir costos se sugiere implementar diversas campañas promocionales como la llevada a cabo el día 24/11 (Black Friday) distribuidas a lo largo del año. Capacitar o fortalecer las competencias de los vendedores menos eficientes. Eliminar la distribución de productos en las regiones menos rentables, fortalecer y sobreponderar la distribución logística en las regiones que representan menores costes de envío y mayor rentabilidad para la empresa.
</p>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Desarrolladores del proyecto</h2>

| [<img src="https://avatars.githubusercontent.com/u/81886133?v=4" width=115><br><sub>Lucel Da Silva</sub>](https://github.com/luceldasilva) |  [<img src="https://avatars.githubusercontent.com/u/93497146?v=4" width=115><br><sub>Christian Fernandez</sub>](https://github.com/Xavieroc93) |  [<img src="https://avatars.githubusercontent.com/u/125892411?v=4" width=115><br><sub>Esteban Ferraz</sub>](https://github.com/estebanferraz1) |
| :---: | :---: | :---: |


<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Licencia</h2>

Este proyecto está bajo la Licencia MIT - mira el archivo LICENSE.md para mas detalles

> [!NOTE]
> 
> Utilizar con fines educativos.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Contacto</h2>

Esteban Ferraz - estebanferraz@outlook.cl

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<h2>Agradecimientos</h2>

Un agradecimiento especial a Alejandro Gamarra y Silvia Branco

[BOOTCAMP XPERIENCE](https://bootcampxperience.com/)

[![](https://img.shields.io/youtube/channel/subscribers/UCuerQOTskuNkddcT738357g?style=for-the-badge&logo=youtube&label=ElProfeAlejo)](https://www.youtube.com/@ElProfeAlejo)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



