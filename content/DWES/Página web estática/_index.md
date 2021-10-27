---
title: "Página web estática"
linkTitle: "Página web estática"
weight: 2
description: >
  Como crear una página web estática
---

A continuación dejaré unos pasos a seguir para que puedas crear tu sitio estático con HUGO

## Instalamos HUGO

    ~$ sudo apt-get install hugo
	
## Creamos un nuevo proyecto

    ~$ hugo new site daw2
  
  **Esto comando creará una nueva carpeta en el directorio que estás ubicado**.
     Te debería salir esto a continuación:

      Congratulations! Your new Hugo site is created in /home/leila/daw2.

      Just a few more steps and you're ready to go:
      1. Download a theme into the same-named folder.
      Choose a theme from https://themes.gohugo.io/ or
      create your own with the "hugo new theme <THEMENAME>" command.
      2. Perhaps you want to add some content. You can add single files
      with "hugo new <SECTIONNAME>/<FILENAME>.<FORMAT>".
      3. Start the built-in live server via "hugo server".

      Visit https://gohugo.io/ for quickstart guide and full documentation.

## Seleccionamos un tema

Dando click a este [enlace](https://themes.gohugo.io/) puedes encontrar varios temas que elegir.

Para descargar el tema e instalarlo directamente en nuestra carpeta haremos lo 
	que indicaré a continuación:

	~/daw2$ git init 
 	~/daw2$ git submodule init 
 	~/daw2$ git submodule add https://github.com/google/docsy.git ./themes/docsy

Lo que hacen estos comandos es:
  1. Inicializar el git en el directorio en el que nos ubicamos
  2. Inicializar git para instalar submódulos
  3. Instala el tema que has elegido en la carpeta themes de nuestro sitio

En nuestro caso, hemos elegido la plantilla 'Docsy'. A diferencia de otros temas, para poder usarlo necesitamos instalar unas cuantas funciones más para poder trabajas con CSS. 

{{< alert title="Tip" >}}Si están siguiendo los pasos y usando la misma plantilla que nosotros, desde la terminal      ejecuta los siguientes comandos:{{< /alert >}}

    ~/daw2$ sudo apt install npm	
    ~/daw2$ sudo npm install -D autoprefixer
    ~/daw2$ sudo npm install -D postcss-cli
    ~/daw2$ sudo npm install -D postcss

  
Antes de dar por "finalizada" la creación de tu sitio edita el archivo **config.toml** :

    ~/daw2$ echo 'theme = "docsy"' >> config.toml 

Y para guardar los cambios y cualquier posible actualización que necesitemos ejecutamos:

    ~/daw2$ git submodule update --init --recursive #para que se actualice

Listo. Ya puedes empezar a customizarla a tu gusto y subir la documentación e información que quieras.