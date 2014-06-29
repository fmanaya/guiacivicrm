
Cómo instalar CiviCRM de una forma fácil (para hacer pruebas)

Arquitectura de CiviCRM

Como actividad propuesta para iniciar la primera jornada de trabajo (el 11 de febrero de 2014) del grupo de trabajo de CiviCRM en el MediaLab-Prado, proponemos la instalación de una versión de CiviCRM que sea fácil de instalar.

[Arquitectura CiviCRM][img/arquitectura-xamp.png]

En la imagen de arriba, se puede ver un esquema típico de los componentes que hacen falta para que CiviCRM funcione. Como una instalación así es algo compleja y queremos empezar con algo simple, proponemos instalar el stack de Bitnami de CiviCRM.
¿Qué es eso de "el stack de Bitnami de CiviCRM"?

Bitnami es una empresa que se dedica a crear paquetes para hacer más fácil las instalaciones web complejas pero típicas, como la de CiviCRM. En el caso de nuestra propuesta de trabajo, lo que queremos instalar es un paquete que incluye, como en una cajita bien empaquetada: Apache, PHP, MySQL, Drupal y CiviCRM. Así, sólo necesitamos un ordenador con Linux, MacOS o Windows para hacer la instalación. De hecho, la instalación es de las que molan, porque a penas hay que pulsar "Siguiente, siguiente, siguiente".

Para facilitar la sesión de trabajo, llevaremos (quiero decir, que no hace falta que llevéis) en una llave USB, ya descargados, los siguientes archivos:

    Para Linux: bitnami-civicrm-4.4.3-0-linux-installer.run
    Para Linux (64 bit): bitnami-civicrm-4.4.3-0-linux-x64-installer.run
    Para Mac: bitnami-civicrm-4.4.3-0-osx-x86_64-installer.dmg
    Para Windows: bitnami-civicrm-4.4.3-0-windows-installer.exe

La instalación me pregunta cosas, ¿qué hago?

La instalación es bastante sencilla. En particular, estos son los pasos (cuando no especificamos nada, es porque podemos mantener lo que nos ofrece la instalación y continuar, sin más):

    Lo primero, cuando abrimos el archivo (de los anteriores) que corresponde a nuestro sistema operativo, es que Bitnami nos da la bienvenida. ¡Hola! :-)
    A continuación, nos pregunta qué queremos instalar. CiviCRM es obligatorio (lógico, cuando instalas CiviCRM, ¡tienes que instalar CiviCRM!, jejeje). Lo que sí que nos da opción es de instalar phpMyAdmin. Es un programita que nos deja ver los datos de CiviCRM y jugar con ellos de forma "avanzada". No lo necesitaremos por el momento pero tampoco molesta. Casi que mejor instalarlo, salvo que tengamos muy poco espacio en disco.
    Todos los programas que se instalen con este paquete, van a estar dentro de una sola carpeta. Ahora, el instalador nos pregunta en qué carpeta queremos instalar CiviCRM. La opción por defecto suele ser una carpeta "civicrm-4.4.3-0" dentro de "mis documentos". Podemos dejarlo así.
    Cuando nuestro CiviCRM esté funcionando, se accederá a él con usuario y contraseña. El usuario administrador, el que tendrá acceso a todas las opciones de CiviCRM, es el que pongamos aquí. Es importante que pongamos una contraseña y que luego nos acordemos de ella. Este paso, de hecho, es obligatorio. Más adelante, podremos crear otros usuarios que sólo tengan permiso para ciertas cosas. Por el momento, basta con poner la contraseña de "user".
    Lo siguiente, es que el instalador nos preguntará por el nombre de nuestro sitio. Podemos dejar el valor por defecto: "user's Site". No pasa nada, luego podremos cambiarlo.
    Como CiviCRM es capaz de enviar correos electrónicos, se nos preguntará si queremos configurar ahora el servidor de correo que hará los envíos. En general, es recomendable que, en las instalaciones de pruebas, no se configure el envío de correos. Así, si creamos contactos con datos reales, evitamos "accidentes" de tipo enviar correos a toda una base de datos. La opción recomendada para esta sesión, es desmarcar la casilla en la que se nos pregunta si querremos soporte para emails.
    Por último, el instalador nos pregunta si queremos "aprender más sobre Bitnami" pero, como ya hemos aprendido hoy mucho sobre Bitnami, desmarcamos y pulsamos continuar.
    Voilà ! ¡CiviCRM y todos los componentes que hacen falta, se instalarán solitos en nuestro equipo!

Ya tengo el stack de Bitnami instalado. ¿Y ahora, qué?

Una vez termina la instalación anterior, ya podemos abrir CiviCRM. Para hacerlo, tenemos que:

    Ir a la carpeta en la que instalamos (ver paso 3) nuestro stack.
    Ejecutar el programa "manager-windows.exe", "manager-osx" or "manager-linux.run".
    Ir a la segunda pestaña e "iniciar todos los servicios".
    En la primera pestaña, pulsar "ir a la aplicación".

Ojo, estos cuatro pasos tendremos que seguirlos cada vez que reiniciemos nuestro equipo, porque CiviCRM no se quedará funcionando salvo que hagamos una configuración un poco más avanzada.
¿Qué hago cuando ya haya terminado?

Mucha gente, antes de asistir a la primera sesión, mostró dudas sobre la diferencia entre instalar CiviCRM para pruebas, o para trabajo real. Otra gente, sin embargo, tiene ya conocimientos técnicos de sobra para entender todos los conceptos que hemos manejado hoy. Ahora que hemos instalado una versión de pruebas, quizá sea buen momento para que las personas que saben algo más, echen una mano al resto a comprender, a ser posible con ejemplos "en vivo", lo que hacen los distintos componentes que necesita CiviCRM.

Hay una pequeña guía junto al esquema de arquitectura de CiviCRM.

Una vez discutido el esquema, sólo nos quedaría empezar a "juguetear" con CiviCRM pensando en qué cosas querríamos trabajar para la siguiente sesión.
