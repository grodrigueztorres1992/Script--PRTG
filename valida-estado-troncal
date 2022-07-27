#!/bin/bash
#este script valida estado de la trunk atraves de asterisk
#este script se debe usar con el sensor de PRTG ssh secuencia de comando avanzado
#Creado:grodriguez
SERVICIO='GTD'
VAR=false
valor=2
veri=$(/usr/sbin/asterisk -rx "sip show peers" |grep $SERVICIO |awk '{print $7}')
if [[ $veri == OK ]]

then
VAR=true
valor=0
                               MSG='La Troncal '$SERVICIO' esta funcionando OK'
fi
if [ $VAR == false ]
then
                               MSG='La Troncal '$SERVICIO' esta en estado DESCONECTADO'

fi
echo "<?xml version='1.0' enconding='windows-1252' ?>"
echo "<prtg>"
echo "   <result>"
echo "                   <channel>Troncal $SERVICIO </channel>"
echo "                                   <value>$valor</value>"
echo "   </result>"
echo "<text>$MSG</text>"
echo "</prtg>"
