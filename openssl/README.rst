Descripción
-----------
Aquí hay una colección de comandos para hacer taréas comúnes con openssl; tales como:

## Generar un CSR ( si tienes una llave privada existente )
    openssl req -out CSR.csr -key /path/a/mi_llave_privada.key -new

## Generar un CSR y una llave privada
    openssl req -out midominio.tld.csr -new -newkey rsa:2048 -nodes -keyout /etc/pki/tls/private/midominio.tld.key
    chmod 440 /etc/pki/tls/private/midominio.tld.key

## Generar un CSR para un certificado existente ( renovación )
    openssl x509 -x509toreq -in /etc/pki/tls/certs/midominio.tld.crt -out midominio.tld.csr -signkey /etc/pki/tls/private/midominio.tld.key

## Generar un certificado propio
    openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/pki/tls/private/midominio.tld.key -out /etc/pki/tls/certs/midominio.tld.crt

    # hacerlos legibles solamente por el dueño y el grupo
    chmod 440 /etc/pki/tls/{certs,private}/midominio.tld.{crt,key}

    # hacer dueño a root y al grupo apache/cherokee/nginx
    chown root:nginx /etc/pki/tls/{certs,private}/midominio.tld.{crt,key}

## Remover la passphrase de una llave
    openssl rsa -in /etc/pki/tls/private/midominio.tld.key -out /etc/pki/tls/private/nueva.key

    # sobre-escribir la llave con passphrase
    cd /etc/pki/tls/private/
    mv nueva.key midominio.tld.key

## Convertir un archivo DER (.crt .cer .der) a PEM
    openssl x509 -inform der -in certificado.crt -out certificado.pem

## Convertir un archivo PEM a DER
    openssl x509 -outform der -in certificado.pem -out certificado.crt

Referencias
----------
* http://www.sslshopper.com/article-most-common-openssl-commands.html
