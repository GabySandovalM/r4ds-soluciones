# Iteración





## 21.2 Bucles _for_{-#bucles-for}

### 21.2.1 Ejercicios{-#ejercicios2121}

1.  Escribir bucles _for_ para:

    1. Calcular la media de cada columna en `mtautos`.
    2. Determinar el tipo de cada columna en `vuelos`.
    3. Calcular el número de valores únicos en cada columna de `iris`.
    4. Genera 10 normales aleatorias para cada valor de $\mu = -10$, $0$, $10$ y $100$.
    
    Piensa en el resultado, la secuencia y el cuerpo __antes__ de empezar a escribir
    el bucle.

<div class="solucion">
<h3>Solución</h3>

</div>

2.  Elimina el bucle _for_ en cada uno de los siguientes ejemplos tomando
     ventaja de una función existente que trabaja con vectores:
    
    
    ```r
    out <- ""
    for (x in letters) {
      out <- stringr::str_c(out, x)
    }
    
    x <- sample(100)
    sd <- 0
    for (i in seq_along(x)) {
      sd <- sd + (x[i] - mean(x)) ^ 2
    }
    sd <- sqrt(sd / (length(x) - 1))
    
    x <- runif(100)
    out <- vector("numeric", length(x))
    out[1] <- x[1]
    for (i in 2:length(x)) {
      out[i] <- out[i - 1] + x[i]
    }
    ```

<div class="solucion">
<h3>Solución</h3>

</div>

3.  Combina tus habilidades para escribir funciones y bucles _for_:

    1. Escribe un bucle _for_ que imprima (_`prints()`_) la letra de la canción de niños
       "Cinco ranitas verdes".

<div class="solucion">
<h3>Solución</h3>

</div>

    2. Convierte la canción infantil "10 monitos saltaban en la cama" en una función. Generalizar
       a cualquier cantidad de monitos en cualquier estructura para dormir.

<div class="solucion">
<h3>Solución</h3>

</div>

    3. Convierte la canción "99 botellas de cerveza en la pared" en una función.
       Generalizar a cualquier cantidad, de cualquier tipo de recipiente que contenga 
       cualquier líquido sobre cualquier superficie.

<div class="solucion">
<h3>Solución</h3>

</div>

4.  Es común ver bucles _for_ que no preasignan la salida y en su lugar
    aumentan la longitud de un vector en cada paso:
     
    
    ```r
    output <- vector("integer", 0)
    for (i in seq_along(x)) {
      output <- c(output, lengths(x[[i]]))
    }
    output
    ```
    
    ¿Cómo afecta esto el rendimiento? Diseña y ejecuta un experimento.

<div class="solucion">
<h3>Solución</h3>

</div>

## 21.3 Variaciones de bucles _for_{-#variaciones-bucles}

### 21.3.5 Ejercicios{-#ejercicios-2135}

1.  Imaginemos que tenemos un directorio lleno de archivos CSV que queremos leer.
    Tenemos sus ubicaciones en un vector, 
    `files <- dir("data/", pattern = "\\.csv$", full.names = TRUE)`, y ahora
    queremos leer cada uno con `read_csv()`. Escribe un bucle _for_ que los
    cargue en un solo _data frame_.

<div class="solucion">
<h3>Solución</h3>

</div>

2.  ¿Qué pasa si utilizamos `for (nm in names(x))` y `x` no tiene _names_?
    ¿Qué pasa si solo algunos elementos están nombrados (_named_ en inglés) 
    ¿Qué pasa si los nombres (_names_ en inglés) no son únicos?

<div class="solucion">
<h3>Solución</h3>

</div>

3.  Escribe una función que imprima el promedio de cada columna numérica en un
	  _data frame_, junto con su nombre. Por ejemplo, `mostrar_promedio(iris)` debe imprimir:
    
    
    ```r
    mostrar_promedio(iris)
    #> Sepal.Length: 5.84
    #> Sepal.Width:  3.06
    #> Petal.Length: 3.76
    #> Petal.Width:  1.20
    ```
    
    (Desafío adicional: ¿qué función utilizamos para asegurarnos que los números
    queden alineados a pesar que los nombres de las variables tienen diferentes longitudes?)

<div class="solucion">
<h3>Solución</h3>

</div>
    
4.  ¿Qué hace este código? ¿Cómo funciona? 

    
    ```r
    trans <- list( 
      disp = function(x) x * 0.0163871,
      am = function(x) {
        factor(x, labels = c("auto", "manual"))
      }
    )
    for (var in names(trans)) {
      mtcars[[var]] <- trans[[var]](mtcars[[var]])
    }
    ```

<div class="solucion">
<h3>Solución</h3>

</div>

## 21.4 Bucles _for_ vs. funcionales{-for-funcionales#

### 21.4.1 Ejercicios{-#ejercicios-2141}

1.  Lee la documentación para `apply ()`. En el caso 2d, ¿qué dos bucles _for_ generaliza?

<div class="solucion">
<h3>Solución</h3>

</div>

2. Adapta `col_summary ()` para que solo se aplique a las columnas numéricas. 
	Es posible que desees comenzar con la función `is_numeric ()` que devuelve un vector lógico que tenga un _TRUE_ por cada columna numérica.
	
<div class="solucion">
<h3>Solución</h3>

</div>

## 21.5 Las funciones _map_{-#funciones-map}

### 21.5.3 Ejercicios{-#ejercicios-2153}

1. Escribe un código que use una de las funciones de map para:

    1. Calcular la media de cada columna en `mautos`.
    1. Obtener de que tipo es cada columna en `vuelos`.
    1. Calcular la cantidad de valores únicos en cada columna de `iris`.
    1. Generar diez normales aleatorias para cada $\mu = -10$, $0$, $10$, and $100$.

<div class="solucion">
<h3>Solución</h3>

</div>

2.  ¿Cómo puedes crear un vector tal que para cada columna en un cuadro de datos indique si
    corresponde o no a un factor?

<div class="solucion">
<h3>Solución</h3>

</div>

3.  ¿Qué ocurre si usas las funciones map en vectores que no son listas?
    ¿Qué hace `map(1:5, runif)`? ¿Por qué?

<div class="solucion">
<h3>Solución</h3>

</div>

4.  ¿Qué hace `map(-2:2, rnorm, n = 5)`? ¿Por qué?
    ¿Qué hace `map_dbl(-2:2, rnorm, n = 5)`? ¿Por qué?

<div class="solucion">
<h3>Solución</h3>

</div>

5.  Reescribe `map(x, function(df) lm(mpg ~ wt, data = df))` para eliminar
    todas las funciones anónimas.

<div class="solucion">
<h3>Solución</h3>

</div>

## 21.9.1 Otros patrones para los bucles _for_ {-#otros-patrones}

### 21.9.3 Ejercicios{-#ejercicios-2193}

1.  Implementa tu propia versión de `every()` usando un loop for. Comparala con
    `purrr::every()`. ¿Qué hace la versión de purrr que la tuya no hace?

<div class="solucion">
<h3>Solución</h3>

</div>

2.  Crea una mejora de `col_sum()` que aplique una función de resumen a cada
    columna numérica en un data frame.

<div class="solucion">
<h3>Solución</h3>

</div>

3.  Un posible equivalente de `col_sum()` es:

    
    ```r
    col_sum3 <- function(df, f) {
      is_num <- sapply(df, is.numeric)
      df_num <- df[, is_num]
    
      sapply(df_num, f)
    }
    ```
    
    Pero tiene una cantidad de bugs que queda ilustrada con las siguientes entradas:

    
    ```r
    df <- tibble(
      x = 1:3, 
      y = 3:1,
      z = c("a", "b", "c")
    )
    # OK
    col_sum3(df, mean)
    # Tiene problemas: no siempre devuelve un vector numérico
    col_sum3(df[1:2], mean)
    col_sum3(df[1], mean)
    col_sum3(df[0], mean)
    ```
    
    ¿Qué causa los bugs?

<div class="solucion">
<h3>Solución</h3>

</div>
