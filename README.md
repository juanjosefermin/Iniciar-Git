Iniciar-Git
===========

::::::::::::::::::::::::::::::::::::::::::::::::

PASOS PARA AGREGAR UN REPOSITORIO A GITHUB

:::::::::::::::::::::::::::::::::::::::::::::::

1
ME UBICO EN LA CARPETA DONDE TENGO MI PROYECTO A VERSIONAR , DENTRO DE LA CONSOLA

2
ESTANDO EN EL FICHERO TIPEO EL COMANDO "GIT INIT" PARA INDICAR QUE VOY A EMPEZAR A VERSIONAR ESTA CARPETA CON TODO SU CONTENIDO

3
SEGUIDO TIPEAREMOS EL SIGUIENTE COMANDO "GIT STATUS" ESTE COMANDO NOS MOSTRARA EN COLOR ROJO TODOS LOS ARCHIVOS QUE AUN NO HEMOS HECHO COMMIT O AGREGADO O E MODIFICADO 

4
LUEGO "GIT ADD -- ALL" ME AGREGA TODOS LOS ARCHIVOS QUE ESTAN DENTRO DE MI CARPETA O SIMPLEMENTE AGREGANDO UN ARCHIVO ALA VEZ CON "GIT ADD NOMBREARCHIVO.PHP"

5
LUEGO DAREMOS "GIT STATUS" ESTE COMANDO NOS MOSTRARA EN VERDE LOS ARCHIVOS QUE ESTAN AGREGADOS CON LA PALABRA NEW FILE: 

6
"GIT COMMIT -M" ESTE COMANDO ME HACE COMENTAR CADA VES QUE MODIFIQUE UN ARCHIVO 

7
DESPUES DE HABER COMENTADO PUEDO VOLVER A DAR "GIT STATUS" PARA VER EL ON BRANCH MASTER DEBERIA DE SALIRME (NOTHING TO COMMIT, WORKING DIRECTORY CELAN)

8
"GIT LOG" ESTE COMANDO ES NECESARIO YA QUE ME BRINDA LA INFORMACION DE TODOS LOS COMMIT QUE VOY HACIENDO DESDE EL DIA Y FECHA Y INFORMACION DE EL USUIARO DE QUE HA HECHO LA MODIFICACION

9
AQUI PUEDO TENER ABIERTO MI PROYECTO N EL EDITOR Y PUEDO HACER UN CAMBIO EN ALGUN ARCHIVO PARA VER QUE SE HA MODIFICADO ALGO SOLO CON EL COMANDO "GIT STATUS" ME MOSTRATA EN ROJO EL ARCHIVO QUE E MODIFICADO

10
TAMBIEN ESTA EL COMANDO Y UTIL"GIT DIFF" QUE ME MUESTRA TAL CUAL LA LINEA QUE MODIFIQUE EN VERDE Y LA QUE ANTES ERA EN ROJO, PARA SALIR DE ESA EDICCION SOLO TECLEA LA TECLA ESC Y LA TECLA Q

11
LUEGO DE HACER ALGUNA MODIFICACION HACER LO SIGUIENTE "GIT ADD NOMBREARCHIVO.PHP"

12
PARA LUEGO COMENTAR EL CMABIO QUE HEMOS HECHO CON EL SIGUIENTE COMANDO "GIT COMMIT -M "TEXTO A COMENTAR" ".

13
SI NOS SALE ALGUN ERROR ALA HORA DE COMENTAR ALGO LO SOLUCIONAMOS CON EL SIGUIENTE COMANDO "GIT COMMIT -A -M "Y EL TEXTO A GREGAR" ".

14
AHORA LO QUE HAREMOS ES AGREGARLO A GITHUB CREANDO UN NUEVO REPOSITORIO Y NO PALOMEAMOS EL README

15
ESTO NOS ABRIRA UNAS INSTRUCCIONES PARA AGREGAR EL REPOSITORIO CON EL COMANDO "GIT REMOTE ADD ORIGIN GIT@GITHUB.COM:NICKNAME/NOMBREPORYECTO.GIT" LO EJECUTAMOS Y NO DEBERA SALIR NINGUN ERROR SI TODO VA BIEN

16
LUEGO SERIA AGREGAR EL SIGUIENTE COMANDO "GIT PUSH -U ORIGIN MASTER" ESTO NOS PEDIRA LA CONTRASEÑA QUE CREAMOS PARA LA CLAVE SSH LA DIGITAS 
