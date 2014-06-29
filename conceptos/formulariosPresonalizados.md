# Personalizar los formularios para añadir información propia de cada organización

## Campos por defecto y campos personalizados

CiviCRM incluye en cada formulario de alta (contactos, eventos, donaciones, etc) una serie de campos básicos que se consideran estándar y útiles para cualquier organización. Por ejemplo:

+ Si queremos dar de alta un contacto, nos encontraremos campos para el nombre, los apellidos o el teléfono.
+ Si es un participante de un evento, veremos que ya existe un campo para el evento en el que va a participar y su rol.

Pero CiviCRM también nos ofrece la posibilidad de personalizar estos formularios para incluir información específica de interés para nuestra organización, que hasta ahora habremos estado recogiendo en otras bases de datos. Por ejemplo, si hemos creado un subtipo de contacto individual “voluntariado” (lo veremos en otra entrada), querremos guardar en qué área colabora y qué horario. O si organizamos un evento que es una carrera solidaria, necesitaremos saber de las personas participantes en qué distancia se inscriben y dónde se han apuntado.
En este artículo vamos a dar unas primeras pautas y consejos de uso que completaremos en la reunión del grupo. [Más información aquí (en inglés)](http://book.civicrm.org/user/current/organising-your-data/custom-fields/), por si queréis ampliar. Y tened en cuenta de que siempre que aparece junto a un campo un circulito con una interrogación dentro, es ayuda. Pinchad y se abrirá un bocadillo.

## ¿Cuál es la mecánica?

Partimos de que ya hemos mirado nuestras bases de datos o las necesidades de nuestro nuevo evento, por ejemplo, y sabemos qué campos necesitamos incluir en CiviCRM porque no viene por defecto. En CiviCRM vamos a crear estos campos, que CiviCRM nos “obliga” a agrupar en conjuntos de campos. Idealmente, usaremos un conjunto por cada bloque de necesidades detectado: uno para la información extra de los voluntarios, otro para la información extra de participantes en la carrera, etc. Tantos como necesitemos.
Además de crear los campos y agruparlos en conjuntos, hay una última cuestión importante: en CiviCRM, cada conjunto de campos se asigna a un tipo de información, que puede ser más general o más concreta (a contactos en general, o a contactos individuales o a contactos individuales “voluntariado”). Una vez asignado, esos campos sólo se mostrarán y se solicitarán para el tipo de información que hayamos decidido.

- Podemos crear un conjunto de campos “Número de identificación”, con un campo que sea “DNI/NIE/Pasaporte” y lo aplicamos sólo a Contactos Individual (no se mostrará para Contactos Organización, pero si para todos los subcontactos que sean Contactos Individual).
- Creamos un conjunto de campos “Voluntariado”, con varios campos (Sede, horario, proyecto en el que colaboran) y lo aplicamos al Contacto Individual Voluntariado que hemos creado previamente (no se mostrará para otros Subcontactos ni para el Contacto Organización).

![](img/fp1.jpg "")

Campos personalizados en el formulario de entrada de datos

![](img/fp2.jpg "")

Campos personalizados rellenado en la ficha de una voluntaria

![](img/fp3.jpg "")

Campos personalizados rellenado en la ficha de una voluntaria (detalle)

## ¿Cómo se crean entonces los campos personalizados?

Los campos personalizados se crean desde el menú `Administrar -> Datos y pantallas personalizados -> Campos personalizados`.

![](img/fp4.jpg "")

Como hemos dicho, la creación de los campos personalizados consta de dos partes. Primero creamos el grupo o conjunto de campos, el contenedor. En este paso, asignamos el conjunto al tipo de información al que va asociado (el evento carrera, el subtipo voluntariado, etc). Una vez creado el conjunto, pasamos al segundo paso, que la creación de los campos.

### Paso 1. Creación del conjunto.

![](img/fp5.jpg "")

De los campos que aparecen, lo fundamental es asignarle el “Nombre del grupo” y establecer el “utilizado para”. El resto se pueden dejar como vienen por defecto. En el campo “utilizado para” si en el primer desplegable escogemos un tipo de información que tenga subtipos, se activará un segundo campo con los subtipos (por ejemplos, tipos de relaciones, subtipos de relaciones, etc). En este segundo desplegable, pulsando la tecla Ctrl y pinchando podemos seleccionar varios subtipos si el campo queremos que se aplique a varios subtipos.
Hay que prestar especial atención a esto y planificarlo bien, porque después no se puede cambiar: en cuanto rellenamos y guardamos un campo personalizado, por ejemplo, con la distancia que recorrió en la carrera un contacto, los valores que hemos introducido en “utilizado para” quedan bloqueados. En este caso, en Movimiento por la Paz, al principio pusimos los campos que queríamos para los participantes de la carrera como “utilizado para: Participantes”. Pero nos dimos cuenta que la pestaña salía en todos los participantes fueran del evento que fueran (seminario, cine, etc), y cuando quisimos cambiarlo a “utilizado para: tipo de evento | Carrera por la Paz” para que sólo aparecieran en este tipo de evento, no pudimos, ni siquiera a través de phpmyadmin, y tuvimos que crear de nuevo el grupo de campos personalizados.

### Paso 2. Creación de los campos.

![](img/fp6.jpg "")

Una vez que hemos creado el conjunto de campos personalizados, salta la pantalla para crear el primer campo personalizado.

Aquí los campos que considero esenciales para empezar son:

- Etiqueta de campo. El texto que acompañará al campo.
- Tipo de campo de entrada. Podemos escoger texto libre, botones radio, botones checkbox, lista desplegable, campo autorrellenable, etc. Si escogemos algún tipo multi-selección, desde aquí sólo podemos poner 11 opciones distintas. Si queremos incluir alguna más, damos a guardar y lo añadimos desde el listado resumen de campos personalizados (ver abajo)
- ¿Requerido? – Si lo marcamos, el campo será obligatorio, y por tanto, deberá ser rellenado siempre, también cuando importemos nuestra base de datos.
- ¿Este campo permite búsquedas? – Si lo marcamos, podremos buscar también por este campo, además de todas las búsquedas por defecto que ofrece CiviCRM.

Una vez creado el primer campo, damos a “Guardar y Nuevo” y se abre el mismo formulario para añadir el segundo y así sucesivamente.

Este es el aspecto que tienen todos los campos creados.

![](img/fp7.jpg "")

Como hemos dicho antes, si queremos añadir alguna opción más en tipo de campo select, o checkbox o radio, lo haremos desde aquí. Pinchamos en “Editar opciones multi-selección”, y seguimos añadiendo opciones.



