#!/bin/bash
#este script valida intentos fallidos de password
#este script se debe usar con el sensor de PRTG ssh secuencia de comando 
#Creado:grodriguez
status=$(cat /var/log/asterisk/full | grep -c '$(date +"%m/%d")|grep Wrong')
#descomentar linea de abajo para hacer pruebas
#status="10"
if [ "$status" -gt 5 ]

then


echo "$status:2:Error"
else


echo "$status:0:OK"

fi
