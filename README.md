# Prácticas Git

> Todos los comandos que aparecen en estas prácticas pueden ser ejecutados tanto en la CMD/Terminal como en la terminal de Visual Studio Code.

## Práctica 1: creación y conexión de repositorios git

#### En esta práctica, instalaremos Git, lo configuraremos y crearemos un repositorio, tanto local como remoto.

### Pasos a seguir na práctica
#### Instalación
1. Instalaremos Git para Windows con el comando `winget install -e --id Git.Git`.
2. Para comprobar que la instalación se ha realizado correctamente ejecutaremos el comando `git --version`.
#### Configuración
3. Lo siguiente será definir nuestro nombre con el comando `git config --global user.name {"nombre"}`.
4. Ahora nuestro correo electrónico: `git config --global user.email {example@email.com}`.
5. Estos comandos no devolverán nada, así que para comprobarlo usaremos el comando `git config --list`.
#### Creación del repositorio
6. Primero crearemos un directorio en dónde tendremos los archivos y subcarpetas con código.
7. Una vez creada utilizaremos el comando `cd` para dirigirnos a esa carpeta.
8. Dentro, ejecutaremos el siguiente comando: `git init`.
9. Para comprobar que hemos inicializado git correctamentene el directorio podemos usar el comando `ls -h`.
#### Pruebas con el repositorio
10. Ahora crearemos el archivo `index.html` con la estructura básica de un documento html.
 > Si estamos en Visual Studio Code podemos escribir `!` o `html:5` para crear dicha estructura.
11. Para comprobar si Git está haciendo un seguimiento de nuestros archivos podremos usar `git status`. Este comando nos devolverá los archivos que todavía no tenemos _staged_.
12. Para añadir estos archivos que todavía Git no está siguiendo usaremos el comando `git add`.
> Podemos usar `git add` con un `.` -> `git add .`, esto añadiría todos los archivos al modo _staged_.
> Por otra parte si queremos hacer seguimiento a un archivo en concreto podemos usar `git add ejemplo.html`.
13. Ahora haremos nuestro primer commit, este comando es esencial y es: `git commit -m "Mensaje del commit"`. Estos commits confirman y guardan los cambios en los archivos en los que usamos previamente `git add`. Siempre debemos escribir un mensaje con cada commit, este mensaje deberá resumir los cambios realizados en el archivo.
14. Para ver los commits realizados en nuestro repositorio usaremos el comando `git log`. Este comando nos mostrará información sobre todos los commits, además mostrará el nombre y email que configuramos en el apartado previo.
> Este comando es una variante al `git log` simple, mostrará además las ramas y definirá con diferentes colores para diferenciar las cosas más fácilmente:  
> `git log --oneline --graph --decorate --all`.
#### Conexión con GitHub
15. Para conectar nuestro repositorio remoto con el local usaremos este comando: `git remote add origin <link de tu repositorio>`.
16. Una vez hecho esto, subiremos a GitHub nuestro repositorio local, para esto usaremos: `git push -u origin master`.
> Y ya tendremos nuestro repositorio en la nube. Otros comandos muy útiles una vez hemos hecho esto son:
> ```bash
> git pull
> git clone <link>
> ```
> `git pull` descargará todo lo subido a nuestro repositorio local. Muy útil si trabajamos en el mismo proyecto desde varios dispositivos o sitios.
> `git clone <link>` clonará todo lo subido al repositorio remoto.

## Práctica 2: actualizar y deshacer cambios en el repositorio
1. El primer comando para esto será `git diff`. Este comando nos mostrará las diferencias entre el mismo archivo en distintas versiones específicas.
2. Otro comando es `git show` que mostrará también diferencias, pero en este caso las diferencias entre 2 commits. 
3. Un comando muy útil por si a la hora de hacer un commit nos equivocamos escribiendo el mensaje, podemos usar el siguiente comando: `git commit --amend -m "Mensaje de ejemplo"`. Esto cambiará únicamente el último commit.
4. Para poder sacar uno o más archivos del proceso _staged/index_ usaremos el siguiente comando: `git restore <file>/*/.`.
> En la mayoría de comandos de git si únicamente utilizamos el nombre del 
fichero el comando afectará solamente al especificado. Pero si deseamos 
que el comando se aplique a todos los ficheros podremos usar `*` o `.`, 
este último si queremos que los cambios se apliquen en el directorio en el que nos encontramos
5.El comando `git reset --hard` elimina los cambios realizados en el árbol de trabajo y en el área de preparación, restaurando la versión más reciente del commit.
6.Si queremos eliminar los cambios del área de preparación pero mantener los cambios en el árbol de trabajo, podemos utilizar `git reset --soft`. Con este comando, los cambios se mantienen en el árbol de trabajo para que podamos seguir trabajando con ellos, pero se eliminan del área de preparación.
7.Otra opción es `git reset HEAD <file>`, que saca el archivo especificado del área de preparación, pero mantiene los cambios en el árbol de trabajo.

## Práctica 3: Ramas
1. Con git branch podemos ver las ramas disponibles en nuestro repositorio y crear nuevas ramas. Simplemente especificamos el nombre de la nueva rama que queremos crear después del comando.
2. Para movernos entre las diferentes ramas de nuestro repositorio, usamos `git checkout` seguido del nombre de la rama a la que queremos cambiar. Además, con `git checkout -b` podemos crear una nueva rama y cambiar a ella en un solo comando.
3. Para combinar dos ramas en una sola, usamos `git merge`. Al especificar el nombre de la rama que queremos fusionar, Git tomará los cambios de ambas ramas y los combinará en una nueva rama que contendrá los cambios de ambas ramas.

## Práctica 4: Repositorios remotos
1. El comando `git remote` nos permite ver una lista de los repositorios remotos que hemos configurado en nuestro repositorio local. Si no hemos configurado ningún repositorio remoto, este comando no mostrará nada.
2. `git remote` -v nos muestra la lista de los repositorios remotos y también nos indica la URL de cada uno de ellos. Este comando es muy útil para verificar que estamos trabajando con el repositorio correcto y que nuestra conexión es correcta.
3. El comando `git push` se utiliza para enviar nuestros cambios al repositorio remoto.
4. `git clone` se utiliza para clonar un repositorio remoto en nuestro ordenador y crear una copia local del repositorio.
5. `git push origin <rama>` se utiliza para enviar los cambios que hemos hecho en una rama específica a nuestro repositorio remoto. 
