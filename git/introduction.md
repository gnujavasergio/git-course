# GIT

## Que es un Sistema de control de versiones?

Es un sistema que registra los cambios realizados sobre uno o varios archivos a lo largo del tiempo.

### Tipos

**Local**
* ctrl+z
* Netbeans tiene un historico local de los cambios de codigo

**Centralizado**
* Todo se centraliza en un servidor y todo esta en el servidor.
* Se pierde nuestro informacion si pasa algo al servidor.

**Distribuido**
* Todo el codigo esta distribuido en varios lugares muchos repositorios

## Que es Git?

* Fue creado por Linus Torvalds para poder ahi versionar el codigo del nucleo de Linux
* Es un sistema de control de versiones que fue diseñado para GNU/Linux pero actualmente ya funciona en cualquier sistema operativo Windows, Mac.
* Git es un VCS distribuido 
* Trabajo offline con git
* Git tiene integridad => No puedes perder informacion durante su transmision o sufrir corrupción de archivos sin que git lo dectecte
* Git guarda los cambios realizados en el tiempo con un SHA1 de 40 caracteres hexadecimales con esto sabemos la referencia de los cambios realizados

## Caracteristicas

* Velocidad
* Diseño sencillo 
* Fuerte apoyo en el desarrollo no lineal => Para poder hacer ramas nuevas con nuevas caracteristicas y despues añadirlo a la rama principal
* Complementamente distribuido
* Capaz de manejar grandes proyectos

## Los 3 estados de git

1. Working directory
   Creamos nuestro archivo
2. staging area
   Añadimos nuestro archivo con git add -A
3. git directory(repository)
   los subimos a nuestro repositorio con git commit -m "Mensaje"

## Que es Github?

* git es diferente a github

**Diferencias**
* git
  * git sera el software que nos va ayudar a versionar nuestro codigo
* github
  * github sera el software que almacenara nuestro codigo
  * Sera el repositorio nos ayudara para que puedan colaborar nuestro codigo
  * github es como una red social de codigo
  * Pueden orginizar tus tareas que hay
  * Pueden extender los poderes de git