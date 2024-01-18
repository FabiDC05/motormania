# Práctica Git, Markdown, Github

## Identificación:

#### Nombre y apellidos:
Fabián Domínguez Ceballos

#### Nombre del módulo:
Desarrollo y Aplicaciones Web

#### Nombre del instituto y curso escolar::
IES Aguadulce, Formación Profesional Grado Superior

#### Enlace a la web:

Enlace de la página [Motormania](https://fabidc05.github.io/motormania/).

## Uso de Git mediante la terminal git bash:

#### Antes de nada comprobaremos la versión de Git:

Con el comando `git --version` comprobaremos la version, que en este caso es **git 2.42.0.windows.2**.

```
PS C:\Users\maniana\Downloads\motormania> git --version
git version 2.42.0.windows.2
```

#### Creación del repositorio en nuestro ordenador (init)

A continuación utilizamos el comando `git init` para crear el repositorio desde nuestro ordenador. Este seria el resultado:

```
PS C:\Users\maniana> cd .\Downloads\
PS C:\Users\maniana\Downloads> git init motormania
Initialized empty Git repository in C:/Users/maniana/Downloads/motormania/.git
```

#### Creación de un commit inicial (add, status, commit, log):

Una vez creados los archivos iniciales de **README.md**, **index.hmtl**, **style.css**, y la carpeta para imágenes **img** con las imágenes necesarias, procedemos a utilizar el comando `git add` para añadir los archivos al status.

```
PS C:\Users\maniana\Downloads\motormania> git add .\index.html .\README.md .\img\ .\style.css
```

La siguiente línea aparecera vacía, por lo que vamos a comprobar que se han subido los archivos al status (que significa que están preparados para ser commiteados). Usaremos el comando `git status`.

```
PS C:\Users\maniana\Downloads\motormania> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   img/logo motormania final.png
        new file:   img/logobmw.png
        new file:   img/logohonda.png
        new file:   img/logohyundai.png
        new file:   img/logokawasaki.png
        new file:   img/logomercedes.png
        new file:   img/logomotormania.png       
        new file:   img/logopeugeot.png
        new file:   img/logoseat.png
        new file:   img/logoyamaha.png
        new file:   img/neymar.jpg
        new file:   index.html
        new file:   style.css
```

Ahora una vez comprobado que están los archivos que queremos commitear, procedemos a usar `git commit` y usamos `-m` para añadir un primer mensaje.

```
PS C:\Users\maniana\Downloads\motormania> git commit -m "Primeros archivos" 
[master (root-commit) ef68550] Primeros archivos
 14 files changed, 342 insertions(+)
 create mode 100644 README.md
 create mode 100644 img/logo motormania final.png
 create mode 100644 img/logobmw.png
 create mode 100644 img/logohonda.png
 create mode 100644 img/logohyundai.png
 create mode 100644 img/logokawasaki.png
 create mode 100644 img/logomercedes.png
 create mode 100644 img/logomotormania.png
 create mode 100644 img/logopeugeot.png
 create mode 100644 img/logoseat.png
 create mode 100644 img/logoyamaha.png
 create mode 100644 img/neymar.jpg
 create mode 100644 index.html
 create mode 100644 style.css
 ```

 Por último, para comprobar que el commit se ha realizado correctamente vamos a utilizar el comando `git log`, y si queremos que condense cada commit en una sola línea, es útil utilizar el comando `git log --oneline` y así obteneos una descripción general de los cambios (este será más útil en un futuro).

 ```
PS C:\Users\maniana\Downloads\motormania> git log --oneline
ef68550 (HEAD -> master) Primeros archivos
PS C:\Users\maniana\Downloads\motormania> git log
commit ef685501a47f7ab8ae67832a044759355feaca4a (HEAD -> master)
Author: Fabian <fabiyeli2020@gmail.com>
Date:   Tue Jan 16 09:47:59 2024 +0100

    Primeros archivos
```

**Se puede apreciar la diferencia entre los dos tipos de log (aunque hay mas tipos)**

#### Creación del repositorio en Github:

Vamos a crear el repositorio que estamos usando en Github para mostrar los commit de forma gráfica. Para ello debemos entrar en Github, iniciar sesión y en el apartado de la izquierda nos aparecen nuestros repositorios actuales. En la parte superior hay un botón que pone **New**, al pulsar en el entraremos en el apartado de crear un repositorio nuevo.

![Creando el repositorio](/capturas/crearrepositorio.png)


A continuación procedemos a elegir el nombre de nuestro repositorio, elegimos si es público y privado, y pulsamos el botón de **crear un nuevo repositorio**:

![Nombre del repositorio](/capturas/crearrepositorio2.png)


#### Añadir el remoto al repositorio local (branch, remote):

Nos apareceran los comandos para aplicar el repositorio remoto desde la terminal con el comando `git remote add origin` y el enlace de nuestro repositorio.
```
PS C:\Users\maniana\Downloads\motormania> git remote add origin https://github.com/FabiDC05/motormania.git
```

Ahora usamos el comando `git branch -M main`.
```
PS C:\Users\maniana\Downloads\motormania> git branch -M main
```

#### Subir el repositorio a Github (push):

El comando `git push` en Git se utiliza para cargar cambios locales en un repositorio remoto. En este caso lo usaremos para subir el repositorio.

```
PS C:\Users\maniana\Downloads\motormania> git push -u origin main
Enumerating objects: 17, done.
Counting objects: 100% (17/17), done.
Delta compression using up to 12 threads
Compressing objects: 100% (17/17), done.
Writing objects: 100% (17/17), 1.78 MiB | 1.37 MiB/s, done.
Total 17 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/FabiDC05/motormania.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

#### Comprobar que está subido a Github:

![Comprobado](/capturas/comprobado.png)

En este caso comprobamos que el repositorio se ha subido correctamente y estan todos los archivos.


#### IMPORTANTE: Agregamos al usuario del profesor como colaborador del repositorio:

![Settings](/capturas/settings.png)

Entramos en el apartado de settings de Github en nuestro repositorio y accedemos al apartado de **access**.

![Añado a Jmoba](/capturas/añadojmoba.png)

Ahora pulsamos el botón de **add people** y añadimos el usuario que queremos invitar, en nuestro caso Jmoba.
Una vez realizado esto el usuario ya estará invitado a nuestro repositorio.

## Publicación en Github Pages:

#### Configurar el repositorio para que publique el directorio raíz en Github Pages:

Entramos en el apartado de settings de Github en nuestro repositorio y accedemos al apartado de **pages**.

![Settings page](/capturas/settingspage.png)

A continuación debemos agregar el main para que detecte el index.

![Añado a main](/capturas/añadimosmain.png)

Nos aparecera la opción de visitar sitio. Pulsaremos para comprobar que la página se detecta correctamente.

![Visitar sitio](/capturas/visitar%20sitio.png)

#### Mostrar los despliegues (deployments):

En la parte inferior derecha de la pantalla principal de nuestro repositorio aparecerá un apartado llamado **deployments**.

![Apartado Deployments](/capturas/deployments.png)

Al pulsar nos llevara a un apartado en el que podremos ver lso despliegues:

![Muestro Deployments](/capturas/muestrodeployments.png)

#### Mostrar la página web.

![Pagina motormania](/capturas/paginamotormania.png)

**Esta sería la página abierta desde el repositorio como podemos obersvar en el url**

## Uso de Git mediante la interfaz de VSCode:

#### Creación de otro commit:

Una vez dentro de Visual Studio Code, podemos ver que al realizar cambios en los archivos de nuestro repositorio, o al crear o añadir archivos, en el apartado de **control de código de fuente** apareceran los cambios que vamos realizando. Para poder aplicar esos cambios deberemos realizar unos pasos.

Primero, al acceder al apartado de **control de código de fuente** veremos los cambios.

![Apartado contros](/capturas/apartado.png)

Nos saldan los archivos nuevos, y los modificados, y si ponemos el cursor encima apareceran diferentes iconos. Con el de **+** podemos almacenar provisionalmente los archivos para un commit.

![Almacenar provisionalmente](/capturas/almacenar.png)



