#!/bin/bash

grep -i "x[[:digit:]]" grepdata.txt 

echo "aca use este comando para imprimir todas las lineas de telefono que terminan con una 'x' predecidad de 4 digitos"

grep -E "^[[:digit:]][[:digit:]][[:digit:]][[:space:]]{1}" grepdata.txt 

echo "Imprime todas las líneas que comiencen con tres dígitos seguidos de un espacio en blanco"


grep -E "[[:alpha:]][[:alpha:]][[:alpha:]][.][[:space:]][[:digit:]]{1,2}.[[:space:]][2-9]" grepdata.txt

echo  "Imprime todas las líneas que contienen una fecha"

grep -Ei  "[a][[:alnum:]][a]|[e][[:alnum:]][e]|[o][[:alnum:]][o]|[i][[:alnum:]][i]|[u][[:alnum:]][u]"  grepdata.txt

echo "Imprime todas las líneas que contienen una vocal (a,e,i,o,u) seguidas de un solo carácter seguido de la misma vocal nuevamente ej: ava,epe"

grep -Ev "^S" grepdata.txt 

echo "imprime todas las lineas que no empiezan con S mayuscula"

grep -Eio "\b[[:alnum:]]+@[a-z\-\.]+[[:alpha:]]+\b" grepdata.txt 

echo "Imprime las lineas que contienen direcciones de correo electronico"
