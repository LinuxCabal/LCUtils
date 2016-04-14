Descripción
-----------
Este programa ayuda a grabar screencasts de manera fácil y sencilla.

Defaults
========
* Formato:      WebM
* Resolución:   1080p @ 10 fps
* Audio:        PulseAudio|Default

Problemas conocidos
===================

Ruido en el audio
-----------------
Un usuario (de los 5 que tenemos; o sea, el 20%!) sufrió de problemas de ruido por usar el codec de ogg vorbis. Cambiando a acc
(nativo para varias webcams con micrófono) pudo resolver el problema.

Para hacer ésto, cambia las variables:

.. code:: bash

    format='mkv'
    audio_codec='libfaac'
    audio_codec_options=''

o

.. code:: bash

    format='mkv'
    audio_codec='aac'
    audio_codec_options='-strict -2'

Y listo. Así de fácil se quitan los ruidos. Recuerda que usamos ``ffmpeg``. Puedes intentar hacer tus propios cambios y reportar
mejorías.
