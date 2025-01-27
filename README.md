![Diseño sin título (14)](https://github.com/user-attachments/assets/120d23af-f058-44a1-8765-9efeb982f19e)


<center>
<h1> Analisis industria petrolera 📈 </h1>
</center>

## Proyecto: Analisis Industria petrolera - Sobre Vuelo S.A 🌍

***Herramientas utilizadas:*** Excel, Power Bi Desktop, Power Bi Service.

***Dashboard final en Power Bi:*** [Reporte - Sobre Vuelo S.A](https://app.powerbi.com/view?r=eyJrIjoiMGZjMTBmNWYtM2I0OS00NzU1LWFlOGItYWMxMTBlYmVhZTNjIiwidCI6ImViZTFkZTRkLWIyM2EtNDMxNC1hNGM4LTk3OTRiZGVlNDY5OSIsImMiOjR9)

## 💻 Introduccion
En el presente proyecto, se busca satisfacer las necesidades de análisis de un cliente ficticio, propietario de la agencia de viajes "Sobre Vuelo SA", quien actualmente cuenta con dos sucursales en funcionamiento. El cliente desea tomar decisiones estratégicas para redirigir su modelo de negocio hacia la industria petrolera, específicamente con la instalación de una estación de servicio en Argentina. Para ello, es imprescindible identificar cuál de las dos sucursales presenta un menor rendimiento, de modo que pueda ser vendida y así generar el capital necesario para esta nueva inversión.

Además, se evaluará a los encargados de ambas sucursales para seleccionar al candidato más adecuado para desempeñar el rol de supervisor en la futura estación de servicio, considerando su desempeño y capacidades de gestión.


## 🎯 Objetivo: 
El objetivo principal de este proyecto es analizar el rendimiento de las dos sucursales de "Sobre Vuelo SA" mediante la integración y visualización de datos clave en un dashboard interactivo, con el fin de:

- Identificar la sucursal con menor desempeño para recomendar su venta.
- Evaluar y seleccionar al encargado más capacitado para asumir la supervisión de la nueva estación de servicio.
- Explorar los datos de empresas de combustible registradas en Argentina, identificando tendencias y oportunidades estratégicas para la ubicación de la futura estación de servicio.
Este análisis permitirá al cliente tomar decisiones informadas basadas en datos concretos, optimizando su transición hacia un nuevo modelo de negocio.**

## 👥 Alcance y usuario Final
El dashboard final esta pensado para utilizarse por los dueños e inversores solicitantes de la demanda ficticia, por este motivo se busca dividir la informacion lo mas clara posible para que de este modo funcione como una herramienta para la toma de decisiones.


## 📊 Análsis en Power BI 
Para el analisis final, se desarrolo un tablero de control con 3 paginas diferentes con el fin de dividir la informacion de forma clara.

Poder acceder al dashboard final desde el siguiente link: [Reporte - Sobre Vuelo S.A](https://app.powerbi.com/view?r=eyJrIjoiMGZjMTBmNWYtM2I0OS00NzU1LWFlOGItYWMxMTBlYmVhZTNjIiwidCI6ImViZTFkZTRkLWIyM2EtNDMxNC1hNGM4LTk3OTRiZGVlNDY5OSIsImMiOjR9)

**🎯Objetivos del tablero:**
- Identificar visualmente la sucursal con menor rendimiento
- Presentar los datos de los encargados y una comparativa entre los 5
- Exponer las diferentes empresas del rubro del combustible, visualizando sus ubicaciones y las zonas con mas y menos competencia.

**📠 Medidas calculadas:** 

1) **Cantidad de banderas:** Count realizado para conocer la cantidad de banderas petroletas registradas.
```
Cant. Banderas = DISTINCTCOUNT(Banderas[Nombre]) 
```
---

2) **Cantidad de ciudades:** Count para conocer la cantidad de ciudades que ya cuentan con alguna empresa petrolera.
```
Cant. Localidades = DISTINCTCOUNT(Ciudades[Ciudad]) 
```
---

3) **Edad promedio:** funcion Average para identificar el promedio de edad de los empleados.
```
Edad promedio = AVERAGE(Empleados[Edad])
```
---

4) **Empleados:** count para cononer la cantidad de empleados de las 2 sucursales.
```
Empleados = COUNT(Empleados[Id_ empleado])
```
---

5) **Empresas:** realizada para conocer la cantidad de empresas registradas al momento del analisis (una bandera puede contener muchas empresas bajo su nombre)
```
Empresas = DISTINCTCOUNT(Empresas_registradas[Id_ Cuit_empresa]) 
```
---

6) **Facturacion:** Sum para realizar la suma de todas las ventas en ambas sucursales.
```
Facturacion = SUM(Facturacion[Monto facturado])
```
---

7) **Faltantes:** Sum para realizar la suma de los faltantes de caja en ambas sucursales.
```
Faltantes = SUM(Facturacion[Faltante_caja]) 
```
---

8) **Sucursal 1:** Calculate para sumar unicamente las ventas realizadas por la sucursal N°1
```
Sucursal 1 = CALCULATE(SUM(Facturacion[Monto facturado]),Facturacion[Sucursal] = 1) 
```
---

9) **Sucursal 2:** Calculate para sumar unicamente las ventas realizadas por la sucursal N°2

```
Sucursal 2 = CALCULATE(SUM(Facturacion[Monto facturado]),Facturacion[Sucursal] = 2) 
```


## 📉 Vista previa del tablero: 
### **Portada**
![image](https://github.com/user-attachments/assets/c34666c7-cdeb-4a62-a751-e816374ad78f)

--- 

### **Pagina 1: Reporte de facturacion** 
![image](https://github.com/user-attachments/assets/def250f9-ac82-4673-b9f9-9952e22b24b1)

---

### **Pagina 2: Reporte de empleados** 
![image](https://github.com/user-attachments/assets/130ab0da-f237-45eb-84ad-98e3c645e4e7)

--- 

### **Pagina 3: Reporte de mercado**
![image](https://github.com/user-attachments/assets/f7395555-2fb0-424c-b528-5df80f635415)

---

## 📝 Conclusiones
Se puede observar que la sucursal N°2 facturó más de un millón de pesos en el período de 2017 y 2021 respecto con la sucursal N°1 pero ambos tuvieron la misma cantidad de faltante de caja, aún sabiendo que la sucursal N°2 tiene más gente trabajando. Los trabajadores de ambas sucursales tienen un rango de edad desde los 25 hasta los 34 años, siendo hombres en su mayoría. 
También podemos observar que la sucursal N°1 a partir del año 2020 descreció notablemente en comparación de la sucursal N°2, el cuál en 2020 tambien 
decayeron sus ingresos pero en 2021 no hizo más que incrementarlos. 

La mayor cantidad de empresas se concentra en Bs As siendo YPF la primera bandera en el ranking, siguiendolo Blanca y Shell, respectivamente.
En lineas generales, la sucursal N°2 es la más rentable ya que la misma cuenta con mayores ingresos y mayor personal para la distribución de turnos.

**Futuras lineas**
Algunos puntos que se pueden añadir a futuro siguiendo la problemática inicial.
* incluir, analizar y solucionar el por qué del faltante de caja por cada personal. 
* Incluir los gastos de logística, distribución del combustible, el cuál también podría estar afectando a la rentabilidad de cada sucursal

## ‼️Aclaracion
Este proyecto se ha desarrollado utilizando un conjunto de datos ficticios con el objetivo de implementar y demostrar mis conocimientos. Debido a que no será utilizado por usuarios reales, no se hará un énfasis detallado en la documentación de las medidas, tablas, ni en las instrucciones de uso del tablero.

<h2 align="center">¡Muchas gracias por tu atención! <img src="https://github.com/ABSphreak/ABSphreak/blob/master/gifs/Hi.gif" width="30px"></h2>







