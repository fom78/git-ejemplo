# _GIT y GitHub_

<small class="date">Última actualización: _Jul 09 2021_</small>



_**Git**_ es un software de control de versiones <a href="https://git-scm.com/" target="_blank" rel="noopener">mas info</a> y **GitHub** es una plataforma donde poder alojar los proyectos, ya sea de manera publica o privada. Es necesario crearse una cuenta <a href="https://github.com/" target="_blank" rel="noopener">Aqui</a>


- Para instalarlo, en **windows** descargar el ejecutable desde el link de <a href="https://git-scm.com/" target="_blank" rel="noopener">Git</a>, para **linux** ejecutar:

```sh
$ sudo apt-get install git
```

<br><hr><br>

## Comandos Basicos GIT

Una vez instalado lo primero: 
```sh
git --version
```
Devolvera la version actual, por ejemplo:
```sh
git version 2.32.0.windows.2
```

Lo proximo a realizar y unica vez al instalarlo es crear el usuario local

```sh
git config --global user.name "mi nombre"
git config --global user.email "myemail@example.com"
```

```sh
git config --global user.name "Fernando"
git config --global user.email "fom78@gmail.com"
```
Luego ejecutamos y comprobamos
```sh
$ git config --global user.name
Fernando
```

Para iniciar un proyecto, dentro del directorio de trabajo, se usa
```sh
$ mkdir git-ejemplo
$ cd git-ejemplo
$ git init
```

Luego, podemos agregar un archivo en el directorio y ejecutamos la orden status para ver que nos muestra git
```sh
$ touch primer-archivo
git status
```
Podemos observar la salida siguiente:


```sh
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        primer-archivo

nothing added to commit but untracked files present (use "git add" to track)
```

En este punto debemos hacer dos pasos basicos, agregar el archivo a la zona de stage y luego realizar el comit correspondiente

```sh
git add .
git commit -m "Primer commit!"
```
Con esto ya tenemos realizado nuestro primer commit en local.
## Colocar nuestro repositorio en GitHub
Ahora para poder tenerlo en la plataforma github, ingresamos con nuestras credenciales. En la pestaña de Repositorios le damos clic al boton <a href="https://github.com/new" target="_blank" rel="noopener">Nuevo</a> (o New) 

- En Repository name, va el nombre del repositorio, en este caso colocare git-ejemplo, dejo las opciones por defecto quedando Publico y le damos a Create repository.

Esto ya nos crea el repositorio y solo faltan unos ultimos pasos. como podemos ver se crea ya la ruta con nuestro username y el nombre del repositorio: https://github.com/fom78/git-ejemplo
En la imagen siguiente contemplamos las opciones para el proximo paso:

<img src="https://fom78-web.vercel.app/img/blog/git-01.png" alt="Configuracion GitHub" loading="lazy">

Como ya tenemos el repositorio local, vamos a copiar la segunda opcion y pegarla en la consola:


```sh
git remote add origin git@github.com:fom78/git-ejemplo.git
git branch -M main
git push -u origin main
```
Le estamos diciendo a nuestro repositorio local que el remoto sera:  git@github.com:fom78/git-ejemplo.git, el reciente creado repositorio en la plataforma GitHub.
Le estamos creando su rama principal y por ultimo empujamos lo que tenemos en local a la nube.

La respuesta en la consola deberia ser algo similar a lo sigiente

```sh
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 214 bytes | 214.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:fom78/git-ejemplo.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

Con esto actualizamos en Github la pagina de nuestro repositorio y ya lo tenemos en la nube.
<img src="https://fom78-web.vercel.app/img/blog/git-02.png" alt="Primer repositorio en la nube" loading="lazy">

### Para culminar una imagen como resumen

<img src="https://fom78-web.vercel.app/img/blog/git-resumen.png" alt="Resumen Git" loading="lazy">

<br><hr><br>
