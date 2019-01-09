==============
lc-parseventos
==============

Descripción
===========
Este pequeño script solo parsea la tabla de Eventos de nuestra página web.

Al hacerlo, te permite obtener los datos en datos populares; tales como: json y yaml.

Instalación
===========

Pre-requisitos
--------------
* ruby
* bundler

Procedimiento
-------------

.. code:: bash

    # ir al directorio que contiene el script
    cd generales/lc-parseventos

    # correr bundler
    bundle install --path vendor/bundle

    # para probarlo, solo córrelo
    bundle exec lc-parseventos
