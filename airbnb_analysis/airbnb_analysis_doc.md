# Análisis viviendas alquiler Airbnb Madrid

Las bases de datos utilizadas se pueden obtener en la página oficial de Airbnb [aquí](http://insideairbnb.com/get-the-data.html).

Se han empleado 3 bases de datos acerca de las viviendas que se alquilan en la plataforma de
Airbnb en la ciudad de Madrid durante el año 2018 (_calendar_, _listings_ y _reviews_)

1. _Calendar_: Información sobre la disponibilidad, fechas y precios de las viviendas entre el
enero de 2018 hasta enero de 2019.
2. _Listings_: Contiene información detallada de las viviendas y de su perfil en la página web
entre enero de 2018 hasta enero de 2019.
3. _Reviews_: Concentra las valoraciones de los usuarios comprendidas entre el 2010 y 2018

El estudio se ha centrado en los siguientes contenidos:

## 1. Patrón de disponibilidad y precios
Usando la base de datos de _calendar_, se han recogido el número total de
viviendas/habitaciones para alquilar y la media de precios de cada día a lo largo del año.
![image](https://user-images.githubusercontent.com/47507358/190875169-44e07f67-7a73-4a46-a73d-a71700928d0b.png)

PUNTOS CLAVE:

**Oferta disponible:**
- En los 3 primeros meses hubo un incremento del 233% en la cantidad de viviendas
ofertadas.
- Grandes irregularidades en la primera mitad del año.
- A partir de agosto una caída y estabilización de la demanda hasta fin de año.

**Precio de la vivienda medio:**
- Caída en el precio a medida que aumenta la oferta en los primeros dos meses.
- Subida repentina de los precios a partir de septiembre, explicada por el bajón de la
oferta de viviendas, que se mantienen hasta finales de año.
- Se experimentan constantes subidas y bajadas relacionadas con los ciclos semanales.

### Efecto de los ciclos semanales en el precio medio de la vivienda
Según el día de la semana, se producen grandes cambios en los precios. Los sábados es el día
con los precios más caros, la mayoría de gente suele hacer sus reservas para el fin de semana.

Este gráfico nos dice quién es el tipo de usuario que alquila viviendas en Airbnb.
- El usuario promedio de Airbnb alquila y viaja por turismo, es por ello que la mayor
demanda se produce en los fines de semana. Este patrón también existe en los períodos
de verano y semana santa.
- Por otra parte, las personas que viajan por negocio no parecen usar mucho Airbnb, los
días de diario son los días con menor demanda.

![image](https://user-images.githubusercontent.com/47507358/190875262-e9244938-9560-448b-a88d-f5b38a55d627.png)

![image](https://user-images.githubusercontent.com/47507358/190875266-027ed36c-b350-4415-b7c4-168a651c2dd3.png)

- En el período de semana santa (del 25 de marzo al 1 de abril) los precios en los días de
diario aumentaron (aunque se sigue distinguiendo perfectamente donde están los fines
de semana)
- Sin embargo, los precios vuelven a la “normalidad” después del 1 de abril que es cuando
terminan las fiestas.

### Disminución en la cantidad de oferta disponible. ¿Motivos?
Los motivos no son algo que podamos encontrar en esta fuente de datos, pero sí sabiendo que
alrededor de esas fechas se estableció una nueva legislación en el municipio de Madrid con la
intención de disminuir y controlar la cantidad de viviendas disponibles en servicios con Airbnb,
por lo que podemos observar las consecuencias de dichas medidas.

### Disponibilidad de las viviendas a lo largo del año
¿Alquila la gente sus viviendas durante todo el año? ¿O es una actividad casual?
El siguiente gráfico de barras mide cuanta parte del año están las viviendas disponibles.
![image](https://user-images.githubusercontent.com/47507358/190875324-d35a39b0-b4a7-45a2-855d-c5c2612010e7.png)
PUNTOS CLAVE:
- Concentración en los extremos
- Un extremo A en el que una importante cantidad de viviendas solo están disponibles
para alquilar un par de semanas al año.
- Otro extremo en el que otra importante cantidad de viviendas tienen disponibilidad
todo o casi todo el año.
![image](https://user-images.githubusercontent.com/47507358/190875342-f12941c4-2fca-4e57-bf70-bd62667f3278.png)



## 2. Variables con un peso significativo en el precio
### Relación entre precio y valoración de los usuarios
Diagrama de dispersión de la relación entre el precio y las valoraciones de los usuarios después
de quitar los outliers de alquileres de precios muy altos que alteraban los resultados.
![image](https://user-images.githubusercontent.com/47507358/190875422-4fc5ef71-54c4-4ece-b35b-c8945871859d.png)

PUNTOS CLAVE:
- No hay una gran correlación
- Precios más altos tienen mejores valoraciones.
- Por otra parte, un precio bajo no implica necesariamente bajas valoraciones, pues existe
una gran oferta en esos rangos de precio.

No debería ser difícil encontrar pisos disponibles con altas valoraciones, independientemente
de tu presupuesto, la media de valoraciones de los usuarios se sitúa en un 92 de 100. Y
únicamente un 25% de todas las viviendas que se ofertan tienen una calificación inferior a 90
de 100.

### Precios según barrios de Madrid
Entre los factores que tienen un mayor impacto en el precio está sin duda la ubicación. En el
siguiente gráfico se distinguen las enormes diferencias entre los distintos barrios de Madrid, lo
que será sumamente útil a la hora de intentar ahorrar el máximo.

- Los barrios del centro de Madrid tienden a ser los más caros.
- (Los barrios señalados con una flecha, hablaremos de ellos en la siguiente gráfica)

### Valoración de los usuarios según barrios de Madrid
Después de ver los precios según la ubicación, sería interesante ver las valoraciones de los
usuarios ¿merece la pena pagar coste añadido por la ubicación?

Atendiendo a las valoraciones de los usuarios y dejando de lado otros factores por lo que nos
interesaría determinadas ubicaciones (cercanía a puntos de interés, por ejemplo) no hay
grandes diferencias entre las valoraciones.
- Barrios del **Pilar**, **Los Ángeles** y **Águilas** tienen las valoraciones más bajas. Son los
barrios que menos compensa alquilar atendiendo únicamente a la valoración de los
usuarios como factor decisivo.
- **Pilar** y **Águilas** tienen precios bajos, pero cualquier otro barrio de precio humilde tiene
mejores valoraciones.
- **Los Ángeles** ni siquiera está entre los más baratos, se encuentra en la media con
respecto a precio del alquiler por lo que es el que menos merecería la pena
- Destacan las valoraciones del barrio de **Atalaya**, sin embargo, este es el barrio más
pequeño de Madrid, por lo que su escasa oferta y escaso número de valoraciones son
responsables de la diferencia con el resto de los barrios.
- El barrio de **Rosas**, que tienen los precios medios más bajos, tiene una valoración más
que decente, y que hacen de él una excelente elección atendiendo exclusivamente a la
valoración de los usuarios.
![image](https://user-images.githubusercontent.com/47507358/190875520-b75688af-22c8-4886-adac-616e3f84e843.png)

### Precios según tipo de vivienda/habitación alquilada

Al igual que con la ubicación, como es lógico el tipo de habitación o vivienda afecta en gran
medida al precio. Lo más caro serían las villas, mientras que lo más barato son espacios
compartidos.
![image](https://user-images.githubusercontent.com/47507358/190875535-76e38d79-a422-49bc-b77a-d4d15538222e.png)


## 3. Correlación entre variables numéricas
La correlación de las variables numéricas relevantes presentes en la base de datos de listings y
mostradas gráficamente en un mapa de calor de correlaciones.

Nos indica aquellas relaciones más fuertes (coloreadas de rojo), y aquellas correlaciones
débiles o de ausencia de cualquier tipo de correlación (coloreadas en azul).

![image](https://user-images.githubusercontent.com/47507358/190875559-7cc7dee0-82db-46cf-9701-f872918823f9.png)

Algunos datos interesantes:
- Correlación del precio con características de la vivienda como los metros cuadrados,
número de camas, baños.
- Valoración de los usuarios no influye significativamente en el precio, lo que confirma lo
que ya habíamos visto en el diagrama de dispersión (sección 2).
- Sin embargo, paradójicamente, la valoración de los usuarios sí se ve condicionada
ligeramente por las características del piso como pueden ser el número de baños (que
indirectamente suelen encarecer el precio)


