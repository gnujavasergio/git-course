# Múltiples claves SSH para diferentes cuentas de Github o Gitlab
- A veces necesita varias cuentas para acceder a Github o Gitlab o herramientas similares. 
- Por ejemplo, puede tener una cuenta para sus proyectos de su empresa y una segunda cuenta para sus proyectos personales.

## Generar las llaves ssh de gitlab y Github
- Crear ssh keys con diferentes nombres.
```bash
cd /home/user_name/.ssh
ssh-keygen -t rsa -C "your_name@company.com"
```

- Cuando veas este mensaje
```bash
Generating public/private rsa key pair. 
Enter file in which to save the key (/home/user_name/.ssh/id_rsa):
```

- Ingrese un nombre unico
```
id_rsa_gitlab 
```

- A continuación, le pedirá que ingrese una contraseña.
- Entonces, habrá creado una clave SSH para la cuenta de su contraseña, ahora puede generar una clave SSH para la cuenta de sus proyectos personales.

- Continuarmos generando la segunda clave para sus proyectos personales.
```bash
ssh-keygen -t rsa -C "your_name@gmail.com"
```

- Cuando veas este mensaje
```bash
Generating public/private rsa key pair. 
Enter file in which to save the key (/home/user_name/.ssh/id_rsa):
```
- Ingrese un nombre unico
```
id_rsa_github
```
## Verificación
- Después de todos los pasos, puede verificar que se hayan creado todas las claves.
```bash
ls /home/user_name/.ssh
# Debería ver una lista de archivos similar a esta
id_rsa_gitlab  id_rsa_github  id_rsa_gitlab.pub  id_rsa_github.pub
```

## Configuración
- Ahora necesita un archivo de configuración para organizar las claves generadas.
```bash
cd ~/.ssh/
touch config
nano config
```

- Agregar al archivo de configuración:
```bash
# gitlab company account
Host https://gitlab.company.com/
  HostName gitlab.company.com
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/id_rsa_home

# Github account
Host https://github.com/
  HostName github.com
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/id_rsa_company
```

- A continuación, eliminará las claves almacenadas en caché.
```bash
ssh-add -D
```
- A continuación, puede verificar que se agregaron sus claves:
```bash
ssh-add -l
2048 SHA256:Tldp2gbqHFm1sNLeadfasdfasdfantc3jMAyuS053c /home/user_name/.ssh/id_rsa_gitlab (RSA)
2048 SHA256:iejTCri7urfasdfasdfasdfzUbfZwj3PAUpPxg /home/user_name/.ssh/id_rsa_github (RSA)
```

- Si no tiene ninguna mensaje, entonces debe agregar sus claves
```
ssh-add ~/.ssh/id_rsa_gitlab
ssh-add ~/.ssh/id_rsa_github
```

## Conexión
- Ahora puedes verificar la conexión
```bash
ssh -T git@gitlab.company.com
Welcome to GitLab, @user_name!
ssh -T git@github.com
Welcome to GitHub, @user_name!
```
