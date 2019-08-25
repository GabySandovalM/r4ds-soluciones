# Importación de datos

## Introducción

Trabajar con datos provistos por los paquetes de R es una muy buena forma de conocer las herramientas de la ciencia de datos, pero en cierto punto debes dejar de aprender y comenzar a trabajar con tus propios datos. En este capítulo aprenderás cómo leer archivos rectangulares de texto plano en R. Aquí solo tocaremos superficialmente el tema de importación de datos, pero muchos de los principios se traducen a otras formas de datos. Finalizaremos sugiriendo algunos paquetes que son útiles para otros tipos de datos. 


### Prerrequisitos

En este capítulo aprenderás cómo cargar archivos planos en R con el paquete __readr__, uno de los paquetes principales de **tidyverse**.


```r
library(tidyverse)
```

## Comenzando


### Ejercicios

1. ¿Qué función utilizarías para leer un archivo donde los campos están separados con "|"?

1. Además de `file`, `skip` y `comment` ¿Qué otros argumentos tienen en común `read_csv()` y `read_tsv()`?

1. ¿Cuáles son los argumentos más importantes de `read_fwf()`?

1. Algunas veces, las cadenas de caracteres en un archivo csv contienen comas. Para evitar que causen problemas deben estar rodeadas por comillas, como `"` o `'`. Por convención, `read_csv()` asume que el caracter de separación será `"`, y si quieres cambiarlo necesitarás usar `read_delim()` en su lugar.¿Qué argumentos debes especificar para leer el siguiente texto en un marco de datos? 
  
    
    
    ```r
    "x,y\n1,'a,b'"
    ```

5. Identifica qué está mal en cada una de los siguientes archivos csv alineados. ¿Qué pasa cuando corres el código?    

    
    ```r
    read_csv("a,b\n1,2,3\n4,5,6")
    read_csv("a,b,c\n1,2\n1,2,3,4")
    read_csv("a,b\n\"1")
    read_csv("a,b\n1,2\na,b")
    read_csv("a;b\n1;3")
    ```

## Analizando un vector

### Ejercicios
1.  ¿Cuáles son los argumentos más importantes para `locale()`?
1.  ¿Qué pasa si pruebas y estableces `decimal_mark` y `grouping_mark` al mismo caracter? ¿Qué pasa con el valor por defecto de `grouping_mark` cuando seleccionas `decimal_mark` a `,`? ¿Qué pasa con el valor por defecto de `decimal_mark` cuando estableces `grouping_mark` a `.`?
1.  No discutí las opciones `date_format` y `time_format` para `locale()`. ¿Qué hacen? Construye un ejemplo que muestre cuándo pueden ser útiles.
1.  Si vives fuera de EEUU, crea un nuevo objeto locale que encapsule las opciones para los tipos de archivo que lees más comúnmente.
1.  ¿Cuál es la diferencia entre `read_csv()` y `read_csv2()`?
1.  ¿Cuáles son las codificaciones más comunes empleadas en Europa? ¿Cuáles son las codificaciones más comunes utilizadas en Asia? Googlea un poco para descubrirlo. 
1.  Genera el formato correcto de texto para analizar cada una de las siguientes fechas y horas:
    
    ```r
    d1 <- "January 1, 2010"
    d2 <- "2015-Mar-07"
    d3 <- "06-Jun-2017"
    d4 <- c("August 19 (2015)", "July 1 (2015)")
    d5 <- "12/30/14" # Dec 30, 2014
    t1 <- "1705"
    t2 <- "11:15:10.12 PM"
    ```
