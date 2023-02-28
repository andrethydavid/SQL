# SQL  🛢️

## Breve historia de las bases de datos 🧭

>Originalmente las bases de datos se utilizaban de manera texto, es decir, que se guardaban los datos de manera plana, en archivos de texto ‘.txt’. El problema era que al momento de sacarlos, leerlos y hacer cosas interesantes con los datos se complicaba.

>En ese contexto nacen las bases de datos relacionales fueron un esfuerzo, incluido matemático, para hacer la conjunción de datos y mantenerlos estables, de forma que no solo pudiéramos guardar, sino también extraer y hacer cosas ingeniosas con los datos, como cálculos estadísticos. Ejemplos de estas bases de datos serían: SQLServer, Oracle, PostgreSQL, MariaDB, MySQL.

### Las bases de datos relacionales históricamente  🗺️

> son una navaja Suiza, son la herramienta que arregla en general todos los casos de datos y te permite hacer sistemas muy robustos con una sola herramienta.

>Por otro lado empezó un problema histórico a inicio de los años 2000, en el que teníamos web 2.0, bases de datos gigantes y redes sociales. Fue un gran torrente de datos incrementándose día a día. Para esto se crearon ciencias para manejo de grandes cantidades de datos, como BIG DATA. En respuesta a esto se crearon nuevas bases de datos que fueron específicas para manejar ciertos casos de datos.

### Las Bases de Datos No Relacionales 🎟️

> no son solo un tipo son diferentes. Algunas basadas en documentos, otras basadas en grafos, otras son columnares, algunas se las guarda en memoria.

>Las bases de datos no relacionales no con como las relacionales, son herramientas específicas para ciertos tipos de trabajo como: mantener el estado de la aplicación (base de datos basado en documentos), si se quiere hacer analítica de datos se requiere un datawarehouse (algo basado en grafos), si se quiere tener algo con relaciones muy complejas entre entidades se recomienda las bases de datos basadas en grafos. Dependiendo el caso de uso se utiliza una herramienta diferente.

>Las bases de datos relacionales también evolucionaron con el paso del tiempo, se han acoplado nuevas funcionalidades, como él implementó de funciones, nuevos esquemas de trabajo y varias funcionalidades nuevas para mantenerse vivas en el mundo del manejo de datos.

* Puntos fuertes de las bases de datos relacionales
* Un caso genérico para el uso de una base de datos relacional podría ser cualquier sistema que pueda ser bien definido en sus entidades, estas a su vez en sus atributos y relaciones, es decir, hay una estructura concreta de los datos. Un ejemplo seria la base de datos para una biblioteca, puesto puedo definir una estructura para los datos a través de entidades, atributos y relaciones.
🚀
* Por otro lado para una base de datos no relacional seria algo curioso, se me ocurre un caso de investigación en la que muchas variables puedan ser medidas por un robot que seria enviado a cumplir esta tarea, pero no se sabe si estas variables existirán en el medio estudiado, podría ser como un viaje a marte o algún otro planeta, incluso a los fondos mas oscuros del mar. Se usaría una base de datos no relacional ya que no habrá una estructura definida de los datos que serán emitidos por el robot enviado. Podría ser una base de datos basada en documentos, como Firebase o MongoDB.
🤓

# Diferencias entre otros manejadores y PostgreSQL 🛢️


* Código libre y orientado a la comunidad
* Base de datos adaptada y madura, soporta JSON y funciones estadísticas
* PL/pgSQL (Procedural Language/PostgreSQL)
* Manejo de objetos
* Particiones en las tablas mediante estrategias
* Common table expressions tratamiento de tablas virtuales, más eficiente en tiempo de ejecusión
* Window functions trata de encontrar relaciones entre un registro y el resto de registros


![image](https://user-images.githubusercontent.com/72534486/219826951-f7a5fbc6-6d94-4070-aab6-d8acd0747604.png)


# Window functions

e ocupan para entender la relación que guarda un registro en particular con respecto al resto del dataset, ya sea una tabla, una partición o un query.
Generalmente se encargan de hacer rankings

![image](https://user-images.githubusercontent.com/72534486/220504445-ea860a4e-eb3b-46de-b0fe-ecd7e90cad67.png)

# PARTICIONES

Particionado - Dividir una tabla en segmentos lógicos. Es una practica común de los manejadores, pero no todos ofrecen la opción para los usuarios de administrar estas particiones. Resulta útil para optimizar las consultas de datos.
Observaciones:

* No todas las tablas deben de ser particionadas, vale la pena hacerlo unicamente cuando hay muchos registros.
* Permite optimizar algunas consultas al no tener que buscar dentro de toda una tabla sino unicamente en un segmento especifico.
* El particionado altera la consistencia de la tablas
* No existen los indices (llaves primarias) en las particiones, o mejor dicho, estos indices cambian basándose en la partición. e.g Si particionas una tabla por fechas, al buscar un dato especifico el primer criterio de búsqueda será la fecha
## **Tipos de operadores**

- **Operadores unarios.-** Requiere una relación o tabla para funcionar.**Proyección (π):** Equivale al comando Select. Saca un número de columnas o atributos sin necesidad de hacer una unión con una segunda tabla.**π**<Nombre, Apellido, Email>(Tabla_Alumno)⠀**Selección (σ):** Equivale al comando Where. Consiste en el filtrado de de tuplas.**σ**<Suscripción=Expert>(Tabla_Alumno)⠀
- **Operadores binarios.-** Requiere más de una tabla para operar.**Producto cartesiano (x):** Toma todos los elementos de una tabla y los combina con los elementos de la segunda tabla.Docentes_Quinto_A **x** Alumnos_Quinto_A⠀**Unión (∪):** Obtiene los elementos que existen en una de las tablas o en la otra de las tablas.Alumnos_Quinto_A **x** Alumnos_Quinto_B⠀**Diferencia (-):** Obtiene los elementos que existe en una de las tablas pero que no corresponde a la otra tabla.Alumnos_planExpertPlus ****

SELECT * 

AS es un numevo nombre o un alias 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d9c11036-5c33-479c-bc23-fc8716059987/Untitled.png)

ORIGEN 

FROM es el nombre de la tabla en donte tenemos los datos funtes 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/23364813-ea53-4340-a381-e532aca18344/Untitled.png)

FROM solo lo puedes colocar una vez  AS td alias para no escribir cada rato la tabla origen 

join es la union con la tabla AS tm ON es la union de [td.pk](http://td.pk) = tm.fk;

pk es la llave primaria y la fk es la llave forania 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d4bf81fa-e66e-4813-a57b-5380d8808613/Untitled.png)

JOIN 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e12671ea-7e6e-4ab4-81b0-4c5ab04829f2/Untitled.png)

WHERE 

 que nos ayuda a filtrar las tuplas dependiendo de las condiciones que se cumplan.

 ORDER BY 

la sentencia ORDER BY tiene que ver con el ordenamiento de los datos dependiendo de los criterios que quieras usar.

- ASC sirve para ordenar de forma ascendente.
- DESC sirve para ordenar de forma descendente.
- LIMIT se usa para limitar la cantidad de resultados que arroja el query.
- HAVING tiene una similitud muy grande con WHERE, sin embargo el uso de ellos depende del orden. Cuando se quiere seleccionar tuplas agrupadas únicamente se puede hacer con HAVING.
- HAVING es similar a WHERE aunque no muy utilizada, pero es necesaria cuando quieres hacer un filtro con datos agrupados por un ORDER BY, HAVING siempre va despues del GROUP BY

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/19fc1bb2-24ac-48ab-ae7c-95d2b542e784/Untitled.png)

****GROUP BY y LIMIT****

- GROUP BY especifica por qué campos se agrupan las agregaciones
- 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/378418f4-430f-4f9a-bc6c-7fd900ace622/Untitled.png)

- LIMIT especifica la cantidad de registros, en SQL Server se llama TOP y va después de SELECT

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e9dac7a4-3b0f-41b0-b99e-7d50328c023a/Untitled.png)

- OFFSET especifica a partir de qué registro se trae la consulta, luego puede venir LIMIT para cerrar el rango. En SQL Server es FETCH NEXT

primer quiery: es le mas basico donde selcciona  las 5 primeras columnas 

![PRIMER CUERI.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/999e2bbb-c3b6-451a-89f3-4ebfac360fce/PRIMER_CUERI.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8f38c80c-b9ce-4a0d-bec2-84b2c92e4cbf/Untitled.png)

# Segundo query

seleccionamos las primeras 5 con limit 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/680b2e09-32eb-4db6-ae77-e89ccbcad536/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/82ae125c-641c-44e1-9f09-fb3d6a58ff51/Untitled.png)

# Tercer query

 WINDOW FUNCTION 

Es cuando hay un sub SELECT para hacer una subc query

Selecionar las < mayores 6 filas 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/428bfcda-a968-4fd7-99f6-5e2f783bd94a/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fede68f7-2a91-4c90-a39a-b8b494ec8cb6/Untitled.png)

# cuarto query

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d147e681-d08a-4508-9ccb-04e03733b9ad/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48a0c2e7-8661-4c49-beee-5c0dc0f11603/Untitled.png)

# buscar la colegiatura

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3e9de269-58a9-4253-8c1b-9d4548efbdc1/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/88eef657-9af4-4c27-a420-26947d366d64/Untitled.png)

segundo 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/54183da7-c321-4c1e-8a31-0d6b2aa23ea5/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/141ad6c7-dee5-4dbb-9b29-a67f437d4dda/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/57e92c4f-5b9b-4dbe-8034-7a5c44b595e9/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/de9da69b-32d8-4777-90df-adf2ec0c3d19/Untitled.png)

ejercicio de divicion de  la tabla 

# Ejercicio de divicion tabla

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/691048d9-54bf-4397-be95-44385484d798/Untitled.png)

SE CREA UN SUB QUERY : PARA HACER LA PARTICION DE LAS 5 PRIMERAS FILAS 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/07782887-2504-4e21-8153-f42ce7f0ca25/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d214c3f8-6593-459d-84aa-4449b2de7d77/Untitled.png)

FECHA EN POSGRES 

En estos comando buscamos las fexhas para ver cuantas personas estan en el 2018

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cbbf8add-f46a-4bfd-b7a6-6fba84130de9/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9ab63341-4456-42e9-b788-d0b91b7c9c56/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b0090d43-e4c9-41b7-ac54-323c752a1d30/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3b498a9f-4102-44d7-bbdd-c8e510528514/Untitled.png)

OPCION 2

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/13f62034-b76d-45d9-8341-9ead1618e470/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7682fbcc-b151-49d6-ba2f-69b3119f9b8c/Untitled.png)

FECHA, HORA, MINUTOS Y SEGUNDOS

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1f300925-161a-4410-86d7-83dd091c5f23/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3a9226d9-5604-48b1-bd38-51eb0202b30b/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1550dd41-e3c5-44b9-a71e-5c7e0116a74a/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a407a348-91ea-423b-b629-640b7432f74c/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/16fada04-7182-4092-8e92-b345774846e7/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/56c88091-bc95-43c9-a525-e350203d953f/Untitled.png)

DUPLICADOS 

Son todos los datos que se repiten 


![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5f4821c0-e431-4dab-9459-68e5696c7b22/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e2c19ae7-419d-4231-b627-94b132e105bd/Untitled.png)

 ejemplo 2 : duplicados, Se buscan los datos repetidos que no tenga el dato  ID 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/400c241c-d5ad-4ab7-bc40-27020d64950d/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d823fffa-26bc-4518-8c2a-8c2d3fc4903b/Untitled.png)

ejemplo 3 dupliacos  Partición por todos los campos excepto ID 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ab9fd6ad-862d-4e63-8251-82470825e35f/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bea80f32-dc1a-4921-913d-8e80e178f124/Untitled.png)

****Selectores de rango**** 

os tipos de rango que vienen en PostgreSQL son:

- int4range: Que trae un rango de enteros.
- int8range: Es un rango de enteros grandes.
- numrange: Es un rango numérico.
- tsrange: Es un rango del tipo timestamp pero sin la zona horaria.
- tstzrange: Es un rango del tipo timestamp con la zona horaria
- daterange: Es un rango del tipo fecha.Esos son los que podemos usar como selectores de rango dentro de PostgreSQL

EJEMPLO • int4range: Que trae un rango de enteros.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a073c7fa-80dd-4945-bd64-b8b4d7ca97fa/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/92614465-a7fa-4434-a500-daf24e6e97a8/Untitled.png)

EJEMPLOS  numrange: Es un rango numérico.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6f246569-6071-40bb-bc4e-cedd7a6442c7/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/64930594-2129-4b94-9079-213b904d5ab2/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8b33258b-ccb9-4ffc-8788-b61e5f88f780/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/96b9f1c4-ec5f-4d6b-bdd5-dc9bff9b5648/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/077ad882-e7e9-4f03-9d63-4fb79c18451a/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/441b5628-8418-4ce8-9c63-d669a23b43f5/Untitled.png)

**Egoísta (selfish)**

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/06ea55bf-1d2a-447c-b798-0e57e7ce94ab/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6d121dda-6662-4d1a-98aa-49e6eaee8c24/Untitled.png)

Triagunlando

La funcion lpad nos ayuda a hacer querys con figuras para hacer mas dinamicos las consultas

 ejemplo 1

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/62762047-64b3-4a77-ae4a-7708f323ce88/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c76dd33e-75f6-4482-8404-df52ecbc4f43/Untitled.png)

EJEMPLO 2

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1574edfd-2efa-43e5-8b13-e44b35a3cbd3/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/15d04bfb-de15-41e7-92e7-7e49fea013e3/Untitled.png)

EJEMPLO 3

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8bc60ff7-a9e7-432d-b630-fa46f33a8fd6/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e6f4c573-8522-40b6-b949-e6d8aea3cca3/Untitled.png)

Base de datos distribuidas 

Es una coleccion de multiples bases de datos separadas fisicamenteque se comucica mediante una red informatica

 

**VENTAJAS**:

- desarrollo modular.
- incrementa la confiabilidad.
- mejora el rendimiento.
- mayor disponibilidad.
- rapidez de respuesta.
- 

**DESVENTAJAS**:

- Manejo de seguridad.
- complejidad de procesamiento.
- Integridad de datos más compleja.
- Costo.

**TIPOS**:

**Homogéneas**: mismo tipo de BD, manejador y sistema operativo. (aunque esté distribuida).

**Heterogénea**: puede que varíen alguna de los anteriores características.-OS-Sistema de bases de datos.-Modelo de datos.

**ARQUITECTURAS**:-** cliente- servidor**: donde hay una BD principal y tiene varias BD que sirven como clientes o como esclavas que tratarán de obtener datos de la principal, a la que normalmente se hacen las escrituras.

- **Par a par** (peer 2 peer): donde todos los puntos en la red de bd son iguales y se hablan como iguales sin tener que responder a una sola entidad.
- **multi manejador de bases de datos**.

**ESTRATEGIA DE DISEÑO**:

- **top down**: es cuando planeas muy bien la BD y la vas configurando de arriba hacia abajo de acuerdo a tus necesidades.
- **bottom up**: ya existe esa BD y tratas de construir encima.

**ALMACENAMIENTO DISTRIBUIDO**:

- **Fragmentación**: qué datos van en dónde.

**fragmentación horizontal**: (sharding) partir la tabla que estás utilizando en diferentes pedazos horizontales.

**fragmentación vertical**: cuando parto por columnas.

**fragmentación mixta**: cuando tienes algunas columnas y algunos datos en un lugar y algunas columnas y algunas tuplas en otro lugar.

- **Replicación**: tienes los mismos datos en todas ala BBDD no importa donde estén.
- **replicación completa**: cuando toda al BD está en varias versiones a lo largo del globo, toda la información está igualita en todas las instancias de BD.**replicación parcial**: cuando algunos datos están replicados y compartidos en varias zonas geográficas**sin replicación**: no estás replicando nada de los datos, cada uno está completamente separa y no tienen que estarse hablando para sincronizar datos entre ellas.

**DISTRIBUCIÓN DE DATOS**:

- **Distribución**: cómo va a pasar la data entre una BD y otra. Tiene que ver mucho con networking, tiempos, latencia, etc. Pueden ser:

**Centralizada**: cuando la distribuyes des un punto central a todas las demás**Particionada**: está partida en cada una de las diversas zonas geográficas y se comparten información entre ellas.**Replicada**: tener la misma información en todas y entre ellas se hablan para siempre tener la misma versión.

## Sharding

Es un tipo de partición horizontal para nuestras bases de datos. Divide las tuplas de nuestras tablas en diferentes ubicaciones de acuerdo a ciertos criterios de modo que para hacer consultas, las tendremos que dirigir al *shard* o parte que corresponda.

## Cuándo usar

Cuando tenemos grandes volúmenes de información estática que representa un problema para obtener solo unas cuantas tuplas en consultas frecuentes.

## Inconvenientes

- Cuando debamos hacer joins frecuentemente entre shards
- Baja elasticidad. Los shards crecen de forma irregular unos más que otros y vuelve a ser necesario usar *sharding (subsharding)*
- La llave primaria pierde utilidad

Window Functions

¿Qué son?

Realizan cálculos en algunas tuplas que se encuentran relacionadas con la tupla actual.

¿Para que sirven?

Evitan el uso de self joins y reduce la complejidad alrededor de la analítica, agregaciones y uso de cursores.

Realizan cálculos que relacionan una tupla con el resto dentro de un mismo scope o partición.

- Evita el uso del self joins
- Reduce la complejidad alrededor de la analítica, agregaciones y cálculos
- Luego de una agregación, la función OVER dicta el scope de la window function, al realizar un PARTITION BY campo
- Si no se especifica un PARTITION BY, la funcion OVER() por default tomará toda la tabla
- También se puede usar ORDER BY campo, esto agrega un campo de granularidad al cálculo, a la vez que agrupa todos los valores iguales dentro de la partición, que ahora se encuentran ordenados

**ROW_NUMBER()**: nos da el numero de la tupla que estamos utilizando en ese momento.

**- OVER([PARTITION BY column] [ORDER BY column DIR])**: nos deja Particionar y Ordenar la window function.

**- PARTITION BY(column/s)**: es un group by para la window function, se coloca dentro de OVER.

**- FIRST_VALUE(column)**: devuelve el primer valor de una serie de datos.

**- LAST_VALUE(column)**: Devuelve el ultimo valor de una serie de datos.

**- NTH_VALUE(column, row_number)**: Recibe la columna y el numero de row que queremos devolver de una serie de datos

**- RANK()**: nos dice el lugar que ocupa de acuerdo a el orden de cada tupla, deja gaps entre los valores.

**- DENSE_RANK()**: Es un rango mas denso que trata de eliminar los gaps que nos deja RANK.

 **PERCENT_RANK()**: Categoriza de acuerdo a lugar que ocupa igual que los anteriores pero por porcentajes.
