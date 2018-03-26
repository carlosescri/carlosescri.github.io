---
layout: post
title: "Año nuevo, diseño nuevo"
image_small: /assets/images/2015/octojekyll.png
image_small_alt: El Octocat de Jekyll
intro: >
    Comenzamos 2015 con un nuevo diseño del blog. Ese es el motivo de no haber
    escrito nada desde hace mucho tiempo: estaba ocupado buscando una plantilla
    que se adaptara a mis gustos y que pudiese modificar. ¿Quieres saber más?
date: 2015-02-03 23:20 0100
---
Los que pasáis de vez en cuando por aquí habréis visto cambiar la apariencia de esta web varias veces.

Hasta hoy se basaba en [WordPress](http://www.wordpress.org), un gestor de contenidos orientado a _blogging_ pero que puede utilizarse virtualmente para cualquier tipo de web (incluso tiendas on-line).

Aunque WordPress es una gran herramienta, tiene ciertas desventajas:

- **Es tan complejo como potente:** crear un tema para WordPress implica saber mucho más que HTML y conocer la estructura del sistema al dedillo (al menos para mi, que me gusta hacer bien las cosas). He tratado suficiente con este sistema como para saber que no es en lo que deseo invertir el tiempo.
- **Es una golosina para los hackers:** Se dedican a planifican ataques por fuerza bruta contra la página de identificación del panel de administración y a buscar vulnerabilidades en el código fuente de la aplicación, ya que es _Open Source_. Al final hace que tu servidor web consuma recursos inútilmente y que tú mismo pierdas el tiempo. Eso si, las actualizaciones son constantes, lo que es un punto a su favor.

Pero el principal motivo es que yo no necesitaba tanta parafernalia, solamente un sitio donde publicar mis artículos, a ser posible, de forma elegante.

Buscando alternativas más sencillas me encontré con [Jekyll](http://jekyllrb.com), un sistema que, a partir de una serie de artículos escritos en formato [Markdown](http://daringfireball.net/projects/markdown/), unas plantillas HTML y un poco de CSS y Javascript, genera un sitio web completo sin códigos dinámicos en el servidor. Todo son ficheros de texto decorados mediante hojas de estilo, así que no hay tanto peligro de ser hackeado, no hay nada que procesar antes de servir el artículo y todo es mucho más rápido.

Los entresijos los contaré en mi [blog de desarrollo](https://nettoys.es), pero básicamente esto me permite escribir mis artículos en mi portátil sin necesidad de una conexión a Internet, guardarlos en un repositorio de código en [Github](http://github.com) y tener una plantilla fácil de personalizar con muy pocos ficheros.

Cuando subo los cambios de mis artículos a Github, inmediatamente Github le envía un aviso a mi servidor web, que se encarga de descargar los cambios y actualizar la página automáticamente.

Solamente me tengo que preocupar de escribir. Sencillamente maravilloso.

*[YAML]: YAML Ain't Markup Language
*[CSS]: Cascading Style Sheets
