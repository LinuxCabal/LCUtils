=========
Generales
=========

install-kivy
============

Instala Kivy en un ambiente virtual.  Realiza
los siguientes pasos:

- Crea una carpeta de proyecto
- Crea el ambiente virtual con Python 3.3
- Emula la opción --always-copy de virtualenv
  que no funciona, requerida para instalar
  pygame.
- Descarga e instala Cython, pygame y Kivy.
- Inicia el repositorio de git en la carpeta
  del proyecto.

Ha sido probado en Fedora 20.

tbg
===

Cambia el esquema de colores de la terminal
en Xfce.  Cada vez que se ejecuta alterna
entre texto claro sobre fondo obscuro y
texto obscuro y fondo claro.  Es útil para
adaptar entre entornos con mucha o poca luz.

Copiar el archivo ``tbg`` a la carpeta ~/bin
y agregar permiso de ejecución.
