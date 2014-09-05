## **Iniciar Git en Ubuntu && Windows con Githud Y Bitbucket** ##

Primero iremos al site de git en descarga [aqui](http://git-scm.com/downloads) dependiendo de tu O.s.

**Instalar en Windows**
en windows descargas el ejecutable y lo instalas comun y corriente como cualquier programa, luego en el asistente del instalador llegaras a una opcion que dice algo referente sobre instalarlo en el cmd osea en la consola de windows. 

**Instalar en Ubuntu** 
En ubuntu es algo diferente solo va a la opcion Linux y esta la distro **Debian/Ubuntu** y copia esta linea

    sudo apt-get install git

 abres una  terminal con el atajo de teclado <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd> T</kbd> y pegas el comando que sale en la lista de **Debian/Ubuntu**. y das intro, te pedira tu contraseña de ubuntu, y luego preguntara si quieres decargar esos paquetes solo escribes **yes** y intro, y a esperar a que todo descargue e instale.

Ya descargado Git en nuestro O.s lo siguiente es ir y crearte una cuenta en [Github](https://github.com) y [Bitbucket](https://bitbucket.org/) te aconsejo que primero la crees en Github para que cuando vayas a crearla en bitbucket solo es asociarla a la cuenta de github 
> **Tip:** Esto se hace para ahorrar al  escribir informacion en ambas cuentas la otra cuestion es que en bitbucket puedes crear respositorios privados y gratis, claro con ciertos limites

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

 hay te muestra la ruta donde va a crearse la llave SSH en donde esta ruta es para la distro de ubuntu para windows seria la siguiente

    C:\DocumentsandSettings\username\.ssh\ 
    o 
    C:\Users\username\.ssh
Donde en username es tu nombre de usuario en tu O.s, Esta carpeta de .ssh estara oculta asi que no la veras si quieres ver archivo y carpetas ocultas, busca como mostrar archivos ocultos en windows. Ya estando en la carpeta .ssh en Ubuntu escribe 

    cat id_rsa.pub
    
   esto te mostrara la llave publica que deberas copiar para asociarla a ambos repositorios remotos de gitHub y Bitbucket. En github vas al icono <i class="icon-cog"></i> **Settings** que es el de configuraciones y en la opcion de SSH keys añades tu llave publica donde le colocas un nombre cualquiera, esto se hace para cuando trabajas con varios equipos los identifique de donde haces las modificaciones, por ejemplo un equipo en la casa y el trabajo
