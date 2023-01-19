# Prácticas Git

> Todos los comandos que aparecen en estas prácticas pueden ser ejecutados tanto en la CMD/Terminal como en la terminal de Visual Studio Code.

## Práctica 1: creación e conexión de repositorios git

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
