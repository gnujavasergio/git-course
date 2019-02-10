# Flujos de Trabajo en git

## Crear un repositorio

Iniciar un repositorio con nombre
```
$ git init repo1
$ cd repo1
repo1 (master)$ 
```

Iniciar un repositorio creando la carpeta
```
$ mkdir blog
$ cd blog
$ git init
blog (master)$  
```

Eliminar el repositorio
```
repo2 (master)$ ls -la
drwxr-xr-x  5 gnujavasergio gnujavasergio 4096 Feb  9 13:59 .
drwxr-xr-x 17 gnujavasergio gnujavasergio 4096 Feb  9 11:54 ..
drwxr-xr-x  8 gnujavasergio gnujavasergio 4096 Feb  9 23:17 .git
repo2 (master)$ rm -rf .git
```

## Agregando, quitando y viendo el estado de un archivo

Agregar un archivo al stage area
```
blog (master)$ touch index.html
blog (master)$ git add index.html
```
Quitar un archivo del stage area
```
blog (master)$ 
```