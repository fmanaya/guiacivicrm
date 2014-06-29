# Esquema básico de los componentes que hacen falta en un servidor para que CiviCRM funcione:

![Arquitectura civiCRM, instalacion XAMP](img/arquitectura-xamp.png "Arquitectura")


* __Sistema operativo__: Ya sea Linux, MacOs, Windows, u otro sistema. Sin entrar en más detalles, debemos elegir un sistema operativo sobre el que funcionen las tres piezas fundamentales para CiviCRM (las explicamos a continuación): Apache, MySQL y PHP. Para una instalación de pruebas, podemos instalar CiviCRM en nuestro escritorio habitual. Sin embargo, para una instalación de producción, lo más recomendable y normal, es hacerlo sobre Linux (y, si es Debian, mejor).
* __Apache__: Es la pieza que encarga de que nuestro servidor se entienda con los navegadores web. En un esquema muy simple, a Apache, una vez instalado en un sistema operativo cualquiera, le podemos "dar" una carpeta y se encargará de que sea accesible desde un navegador.
* __PHP__: Apache, por sí sólo, es capaz de hablarse con un navegador y *enseñarle* documentos que tengamos en nuestro sistema. PHP es algo así como lo que da inteligencia a Apache y le permite hacer cálculos. Así, los navegadores pueden interactuar con algo que no sólo es capaz de devolverles documentos sino, además, hacer cosas: enviar emails, crear documentos, etc.
* __MySQL__: En el caso de aplicaciones de datos, PHP empieza a quedarse corto y necesita que los datos se guarden, de alguna manera ordenada. MySQL se encarga justo de eso: de facilitar que los datos puedan obtenerse de forma rápida, agrupados de una u otra manera, modificados, con diferentes órdenes, etc.
* __CMS__: Ya sea [Drupal](https://www.drupal.com), [Wordpress](https://www.Wordpress.com) o [Joomla!](https://www.joomla.com). Con aplicaciones web complejas (como CiviCRM), es normal que queramos tener accesos controlados por usuario y contraseña, o que queramos que algunos de los datos de nuestra base de datos se muestren en una página web, etc. De ese tipo de tareas se encarga el CMS. En el caso de Drupal, la integración con CiviCRM está mucho más conseguida (tanto en cómo se gestionan los permisos que tendrá cada usuario, como en la capacidad de crear formularios que dejen datos directamente en CiviCRM, etc).
* __CiviCRM__*: Por fin, CiviCRM se encargará sólo de gestionar nuestros contactos: ayudarnos a crearlos, a mantener su información actualizada, enviarles emails, etc.

