# R Markdown


## 27.2 R Markdown básico{-#rmarkdown-basico}


### 27.2.1 Ejercicios{-#ejercicios-2721}

1. Crea un nuevo *notebook* usando _File > New File > R Notebook_. Lee las
 instrucciones. Practica ejecutando los bloques. Verifica que puedes modificar el código, re-ejecútalo, y observa la salida modificada.

<div class="solucion">
<h3>Solución</h3>

</div>

2. Crea un nuevo documento R Markdown con _File > New File > R Markdown..._
 Haz clic en el icono apropiado de *Knit*. Haz *Knit* usando el atajo de teclado apropiado. Verifica que puedes modificar el *input* y la actualizacion del *output*.

<div class="solucion">
<h3>Solución</h3>

</div>

3. Compara y contrasta el *notebook* de R con los archivos de R markdown que has
 creado antes. ¿Cómo son similares los outputs? ¿Cómo son diferentes? ¿Cómo son similares los inputs? ¿En qué se diferencian? ¿Qué ocurre si copias el encabezado YAML de uno al otro?

<div class="solucion">
<h3>Solución</h3>

</div>

4. Crea un nuevo documento R Markdown para cada uno de los tres formatos
 incorporados: HTML, PDF and Word. Haz *knit* en cada uno de estos tres documentos. ¿Como difiere el output? ¿Cómo difiere el input? (Puedes necesitar instalar LaTeX para poder compilar el output en PDF--- RStudio preguntará si esto es necesario).

<div class="solucion">
<h3>Solución</h3>

</div>

## 27.3 Formateo de texto con Markdown{-#formateo-texto}

### 27.3.1 Ejercicios{-#ejercicios-2731}

1. Practica lo que has aprendido crando un CV breve. El título debería ser tu nombre,
 y deberías incluir encabezados para (por lo menos) educación o empleo. Cada una de las secciones debería incluir una lista con viñetas de trabajos/ títulos obtenidos. Resalta año en negrita.

<div class="solucion">
<h3>Solución</h3>

</div>

1. Usando la referencia rapida de R Markdown, descubre como:

        1. Agregar una nota al pie.
        1. Agregar una linea horizontal.
        1. Agregar una cita en bloque.

<div class="solucion">
<h3>Solución</h3>

</div>

3. Copia y pega los contenidos de `diamond-sizes.Rmd` desde
 <https://github.com/hadley/r4ds/tree/master/rmarkdown> a un documento local de R Markdown. Revisa que puedes ejecutarlo, agrega texto despues del poligono de frecuencias que describa sus características más llamativas.

<div class="solucion">
<h3>Solución</h3>

</div>

## 27.4 Bloques de código{-#bloques-codigo}

### 27.4.7 Ejercicios{-#ejercicios-2747}

1. Incluye una seccion que explore como los tamaños de diamantes varian por corte, color y claridad. Asume que escribes un reporte para alguien que no conoce R, y en lugar de fijar `echo = FALSE` en cada bloque, fijar una opción global.

<div class="solucion">
<h3>Solución</h3>

</div>

2. Descarga `diamond-sizes.Rmd` de <https://github.com/hadley/r4ds/tree/master/rmarkdown>. Agrega una sección
 que describa los 20 diamantes mas grandes, incluyendo una tabla que muestre sus atributos más importantes.

<div class="solucion">
<h3>Solución</h3>

</div>

3. Modifica `diamonds-sizes.Rmd` para usar `comma()` para producir un formato de *output* ordenado. También incluye el porcentaje de diamantes que son mayores a 2.5 quilates.

<div class="solucion">
<h3>Solución</h3>

</div>

4. Fija una red de bloques donde `d` depende de `c` y `b`, y
 tanto `b` y `c` dependen de `a`. Haz que cada bloque imprima `lubridate::now()`, fijar `cache = TRUE`, y verifica entonces tu comprensión del almacenamiento en *cache*.

<div class="solucion">
<h3>Solución</h3>

</div>
