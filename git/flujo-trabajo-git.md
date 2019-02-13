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

## Estado Stage Area

Agregar un archivo al Atage Area
```
blog (master)$ touch index.html
blog (master)$ git add index.html
blog (master)$ git status
```
Quitar un archivo del stage area
```
blog (master)$ git rm --cached index.html
blog (master)$ git status
```

Si queremos agregar varios archivos al Stage Area
```
blog (master)$ touch style.css
blog (master)$ git add -A
```

Borrar el archivo del Stage Area y quitar del proyecto
```
blog (master)$ rm -rf style.css
```

Comprobar que archivos puedo subir al Stage Area
```
blog (master)$ git add -n
```

## Estado Repositorio

Para confirmar que nuestros cambios se añadan a nuestro repositorio local
```
blog (master)$ git commit -m "Inicializar nuestro index"

```