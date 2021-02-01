# Clase 1 - 09/12/20

## Clonar

Podemos clonar cualqueire repositorio al que tengamos acceso utilizando la url
que podemos obtener de su pagina princiapl y escribiendola en el siguiente comando.

    git clone <url>

## Configurar git en nuestra computadora

Necesitamos configurar nuestro nombre de usurio y email para trabajar con git en el
archivo de configuracion a nivel global. Lo podemos hacer utilizando los comandos;

    git config --global user.name <userName>
    git config --globla user.email <email>

Podemos condirmar los cambio utilizando el siguiente comando para ver la lista 
de variables.

    git config --global -l

Podemos borrar cualquiere variable y su valor utilizando el siguiente comando

    git config --global --unset <variableName>


## Estados de Git

### Working 

Son todos los archivos que estan seguimiento y modifico, o los archivos que acabo de crear y no estan en seguimiento. Para pasar al area de Staging:

    git add .

Me agrega todos los archvios de mi area de Working. Esten en seguimiento o no. 

    git add -u .

Me agrega todos los archivos modificados en mi area de Working. Ignora los que no estan en seguimiento.

    git add <name>
    git add -u <name>

Me agrega solo el archivo con ese nombre. En el segundo caso solo me agregaria un archivo con ese nombre que este en seguimiento y modificado.

    git add <expresion_regular>
    git add -u <expresion_regular>

Me agrega todos los archivos que cumplen con la expresion regular escrita, por ejemplo la siguiente solo me pasaria al area de Staging los archivos con una extencion css;

    git add *.css

Las reglas de de expresion regualar son las mismas que para todos los lenguajes. 


### Staging

Son todos aquellos archivos del area de Wotking que pre selecciono para que formen parte del proximo commit (una nueva version en mi linea de tiempo). Para pasar al area de Repository;

    git commit -m "mensaje"

Tambien podemos escribir el comentario en un editor. Por defualt tenemos el editor Vim, y deberemos realizar la sigueinte combinacion de comandos para guardar y salir del editor: crtl + o, ENTER, ctrl + x. 

    git commit

El editor puede ser configurado en el git config --global. Este comadno es para Windows.

    git config --global core.editor "ubicacion del .exe"


### Repository

Son los archivos seleccionado del area de Staging converidos a una nuava version en mi linea de tiempo, con un numero unico y un comentario asociado. 

Hasta aca todo esta en mi computadora. Si me equivoco lo puedo borrar y nadie se entera, pero si no lo subo no tengo respaldo ante una perdida.

    git push

# Clase 2 - 14/12/20

## Branch

### Como creamos una rama?

El primer comando me crea la rama. El segundo me crea la rama y me mueve a esta. 

    git branch <name_rama>

    git checkout -b <name_rama>

### Como borro una rama?

    git branch -d <name_rama>

    git branch -D <name_rama>

### Como me muevo entre ramas?

    git checkout <name_rama>

### Como fusiono ramas?

Estando parados en al rama en la que quiero que se guarde el resutado de la fusion. 

    git merge <name_rama>

