##Menu

-[Iniciar Git con Ubuntu](https://github.com/LearningTools/Iniciar-Git#iniciar-git-en-ubuntu--windows-con-githud-y-bitbucket)

-[Comprobar llave SSH](https://github.com/LearningTools/Iniciar-Git#comprobar-llave-ssh)

-[Clonar un repositorio](https://github.com/LearningTools/Iniciar-Git#clonar-un-repositorio)

-[Inicar un repositorio vacio](https://github.com/LearningTools/Iniciar-Git#iniciar-un-repositorio-vacio)


## **Iniciar Git en Ubuntu && Windows con Githud Y Bitbucket** ##

Primero iremos al site de git en descarga [aqui](http://git-scm.com/downloads) dependiendo de tu O.s.

**Instalar en Windows**
en windows descargas el ejecutable y lo instalas común y corriente como cualquier programa, luego en el asistente del instalador llegaras a una opción que dice algo referente sobre instalarlo en el CMD osea en la consola de windows. 

**Instalar en Ubuntu** 
En ubuntu es algo diferente solo va a la opción Linux y esta la distro **Debian/Ubuntu** y copia esta linea

    sudo apt-get install git

 abres una  terminal con el atajo de teclado <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd> T</kbd> y pegas el comando que sale en la lista de **Debian/Ubuntu**. y das intro, te pedirá tu contraseña de ubuntu, y luego preguntara si quieres descargar esos paquetes solo escribes **yes** y intro, y a esperar a que todo descargue e instale.

Ya descargado Git en nuestro O.s lo siguiente es ir y crearte una cuenta en [Github](https://github.com) y [Bitbucket](https://bitbucket.org/) te aconsejo que primero la crees en Github para que cuando vayas a crearla en bitbucket solo es asociarla a la cuenta de github 
> **Tip:** Esto se hace para ahorrar al  escribir información en ambas cuentas la otra cuestión es que en bitbucket puedes crear repositorios privados y gratis, claro con ciertos limites

**Usando la Terminal en Ubuntu o Consola en Windows**
 
 Esto es para ambas estos comando:

    git config --global user.name "username"

donde en "username" colocaras tu nombre incluyendo las comillas y das intro

    git config --global user.email email@gmail.com
el siguiente es dar un correo donde en email@gmail.com va tu correo  y das intro.

lo siguiente es crearnos una llave SSH para conectar nuestro equipo con el repositorio remoto tanto en gitHub como en Bitbucket  en la terminal o consola escribimos

    ssh-keygen
    
   donde esto mostrar el siguiente mensaje 
   

    Generating public/private rsa key pair.
    Enter file in which to save the key
    (/home/you/.ssh/id_rsa):

 hay te muestra la ruta donde va a crearse la llave SSH en donde esta, y te pdira una contraseña para la llave coloca una que no se te vaya a olvidar, la  ruta  para windows seria la siguiente

    C:\DocumentsandSettings\username\.ssh\ 
    o 
    C:\Users\username\.ssh
Donde en username es tu nombre de usuario en tu O.s, Esta carpeta de .ssh estará oculta así que no la veras si quieres ver archivo y carpetas ocultas, busca como mostrar archivos ocultos en windows. Ya estando en la carpeta .ssh busca el archivo de la llave publica que es id_rsa.pub

Y para Ubuntu la ruta seria la siguiente tecleando en una terminal 

    /home/user/.ssh
    
 en esa carpeta quedara solo copiar la llave publica que es el mismo archivo id_rsa.pub y para ver su contenido teclea en la terminal 

    cat id_rsa.pub
    
esto te mostrara la llave publica que deberás copiar para asociarla a ambos repositorios remotos de gitHub y Bitbucket. En github vas al icono <i class="icon-cog"></i> **Settings** que es el de configuraciones y en la opción de SSH keys añades tu llave publica donde le colocas un nombre cualquiera, esto se hace para cuando trabajas con varios equipos los identifique de donde haces las modificaciones, por ejemplo un equipo en la casa y el trabajo. 
Y en Bitbucket cuando creamos  la cuenta te mostrara opción de iniciar sesión la puedes asociar a la cuenta que primero creaste en github o si no la puedes hacer independiente las cuentas, ahora solo tocara ir a asociar tu llave ssh a este sitio también vas a tu perfil de la esquina derecha superior donde aparece tu NickName o tu avatar y escoges la opción de administrar cuenta y en la parte del menú Vertical esta la opción clave ssh, das en agregar clave y lo mismo le das un nombre para identificar,  esto se hace para cuando trabajas con varios equipos los identifique de donde haces las modificaciones la guardas y listo

#Comprobar llave SSH

Cuando ayas introducido tus llaves a los diferentes servicios de repositorios en la consola cmd de Windows o la terminal de Ubuntu  digita esto para verificar si tu llave esta asociada con Github

    ssh -T git@github.com
esto saldrá un mensaje como el siguiente

    The authenticity of host 'github.com (207.97.227.239)' can't be established. RSA key fingerprint is16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48. Are you sure you want to continue connecting (yes/no)?

donde le darás Yes y enter, esto de devolverá un mensaje como el siguiente 

    Hi username! You've successfully authenticated, but GitHub does not provide shell access.
 con esto seria  todo para asociar las llaves publcas y poer empezar a versionar tus proyectos 


#Clonar un repositorio
si quieres clonar un repositorio primero ubicate en la carpeta o ruta de donde quieres clonar el repositorio y escribe el siguiente comando:

    git clone git@bitbucket.org:LearningTools/ubuntugit.git
para un repositorio mio en bitbucket y para clonar un repositorio en github seria el siguiente

    git clone git@github.com:LearningTools/App-1.git
si te pide contraseña coloca la  que colocaste cuando se creo la llave ssh al comienzo con esto ya tienes un proyecto y puedes empezar a versionarlo.

#Iniciar un repositorio vacio
si no quieres clonar un repositorio y quieres empezar uno desde cero vuelve a la consola o terminal y ubicate a donde quieras crear un nuevo proyecto crea una carpeta y entro de la carpeta creada escribe el siguiente comando 

    git init
   esto devolvera algo asi
   

    Initialized empty Git repository in /ruta/del/proyecto/creado/.git/


esto significa que vas a empezar a versionar tu proyecto empieza creando un archivo del lenguaje que tu uses y cuando lo crees y tenga contenido en ese archivo guarda y en la consola escribe el siguiente comando para ver que en que archivos huvieron cambios

    git status

con  este comando veras en color rojo los archivos modificados, para agregar ese cambio de un archivo solo escribe

    git add nombreArchivo.html
y si son varios archivos cambiados escribe

    git add .
esto agregara todos los archivos modificados ahora solo deberemos dar una pequeña descripcion de lo que se hizo en ese archivo con el siguiente comando

    git commit -m "descripcion del cambio"
las comillas "" son exenciales ya que hay va la descripcion de lo que se hizo en ese archivo o los archivos que se modificaron

ahora solo deberemos agregar este proyecto que hicimos en local ahora ve a las cuentas de github o bibucket y crea un repositorio, dale un nombre y dale en crear, cuando este creado nos dara unas instrucciones en nuestro caso solo veremos la de esta opcion
**or push an existing repository from the command line**
que primero agregamos el ropositorio a el remoto con el comando

    git remote add origin git@github.com:userName/nombreRepositorio.git

y solo impulsamos el contenido con el comando 

    git push -u origin master

> Written with [StackEdit](https://stackedit.io/).
