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
