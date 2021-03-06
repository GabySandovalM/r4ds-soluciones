# Vectores




## 20.3 Tipos importantes de vectores atómicos{-#vectores-atomicos}

### 20.3.5 Ejercicios{-#ejercicios-2035}

1. Describe la diferencia entre `is.finite(x)` y `!is.infinite(x)`.

<div class="solucion">
<h3>Solución</h3>

</div>

2. Lee el código fuente de `dplyr:: near()` (Consejo: para ver el código fuente, escribe lo siguiente `()`) ¿Funcionó?

<div class="solucion">
<h3>Solución</h3>

</div>

3. Un vector de tipo lógico puede tomar 3 valores posibles. ¿Cuántos valores posibles puede tomar un vector de tipo entero? ¿Cuántos valores posibles puede tomar un vector de tipo real? Usa Google para realizar buscar información respecto a lo planteado anteriormente.

<div class="solucion">
<h3>Solución</h3>

</div>

4. Idea al menos 4 funciones que te permitan convertir un vector del tipo real a entero. ¿En qué difieren las funciones? Precisa tu respuesta.

<div class="solucion">
<h3>Solución</h3>

</div>

5. ¿Cuáles funciones del paquete readr te permiten convertir un vector del tipo string en un vector del tipo lógico, entero y doble?

<div class="solucion">
<h3>Solución</h3>

</div>

## 20.4 Usando vectores atómicos{-#uso-vectores}

### 20.4.6 Ejercicios{-#ejercicios-2046}

1. La expresión `mean(is.na(x))`, ¿qué dice acerca del vector 'x'? ¿y qué sucede con la expresión `sum(!is.finite(x))`?

<div class="solucion">
<h3>Solución</h3>

</div>

2. Detenidamente lee la documentación de `is.vector()`. ¿Para qué se prueba la función realmente? ¿Por qué la función `is.atomic()` no concuerda con la definición de vectores atómicos vista anteriormente?

<div class="solucion">
<h3>Solución</h3>

</div>

3. Compara y contraste `setNames()` con `purrr::set_names()`.

<div class="solucion">
<h3>Solución</h3>

</div>

4. Crea funciones que tomen un vector como entrada y devuelva:
	1. El último valor. ¿Deberás usar `[` o `[[`?.
	1. Los elementos en posiciones pares.
	1. Cada elemento excepto el último valor.
	1. Sólo las posiciones pares (y sin valores perdidos (missing values)).

<div class="solucion">
<h3>Solución</h3>

</div>
5. ¿Por qué `x[-which(x > 0)]` no es lo mismo que `x[x <= 0]`?

<div class="solucion">
<h3>Solución</h3>

</div>

6. ¿Qué sucede cuando realizas un subset (subdivisión) con un entero positivo que es mayor que la longitud del vector? ¿Qué sucede cuando realizas un subset (subdivisión) con un nombre que no existe?

<div class="solucion">
<h3>Solución</h3>

</div>


## 20.5 Vectores Recursivos (listas){-#listas}


### 20.5.4 Ejercicios{-#ejercicios-2054}

1.Dibuja las listas siguientes como sets anidados:

  1.	`list(a, b, list(c, d), list(e, f))`
  1.	`list(list(list(list(list(list(a))))))`

<div class="solucion">
<h3>Solución</h3>

</div>

2.¿Qué pasaría si subdividieras un tibble como si fuera una lista? ¿Cuáles son las principales diferencias entre una lista y un tibble?

<div class="solucion">
<h3>Solución</h3>

</div>


## 20.7 Vectores Aumentados{-#vectores-aumentados}

### 20.7.4 Ejecicios{-#ejercicios-2074}

1. ¿Qué valor retorna la siguiente expresión hms::hms(3600)? ¿Cómo se muestra? ¿Cuál es la tipo primario sobre el cual se basa el vector aumentado? ¿Qué atributos utiliza el mismo?

<div class="solucion">
<h3>Solución</h3>

</div>


2. Intenta y crea un tibble que tenga columnas con diferentes longitudes. ¿Qué es lo que ocurre?

<div class="solucion">
<h3>Solución</h3>

</div>

3. Teniendo en cuenta la definición anterior, ¿está bien tener una lista como columna en un tibble?

<div class="solucion">
<h3>Solución</h3>

</div>
