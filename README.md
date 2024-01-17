# Práctica Git, Markdown, Github

## Identificación:

#### Nombre y apellidos:
Fabián Domínguez Ceballos

#### Nombre del módulo:
Desarrollo y Aplicaciones Web

#### Nombre del instituto y curso escolar::
IES Aguadulce, Formación Profesional Grado Superior

#### Enlace a la web:

Enlace de la página [Motormania]().

## Uso de Git mediante la terminal git bash:

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

![Ejemplo de texto alternativo](/capturas/crearrepositorio.png)


A continuación procedemos a elegir el nombre de nuestro repositorio, elegimos si es público y privado, y pulsamos el botón de **crear un nuevo repositorio**:

![Segunda captura](/capturas/crearrepositorio2.png)

Nos apareceran los comandos para aplicar el repositorio remoto desde la terminal con el comando `git remote add origin` y el enlace de nuestro repositorio.

```
PS C:\Users\maniana\Downloads\motormania> git remote add origin https://github.com/FabiDC05/motormania.git
```

Ahora usamos el comando `git branch -M main` y `git push -u origin main`

```
PS C:\Users\maniana\Downloads\motormania> git branch -M main
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