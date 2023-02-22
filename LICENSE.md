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
