
# Lenguaje Regular

## Introducción

Los lenguajes regulares son ampliamente utilizados en el procesamiento de lenguajes de programación y en la búsqueda de cadenas de caracteres o secuencias específicas. Las expresiones regulares (E.R) proporcionan una manera sencilla de describir estas secuencias de caracteres. La búsqueda de caracteres o secuencias concretas de caracteres en documentos forma parte de las tareas estándar y recurrentes de la tecnología de la información. Por lo general, el objetivo es modificar o sustituir fragmentos de texto o líneas de código, cuya complejidad aumenta en función de las veces que la secuencia de caracteres aparece en el documento.

## Lenguaje Regular

Un **lenguaje regular** es una secuencia de elementos que cumple y verifica las siguientes condiciones:

* `a ∈ V` entonces `a` es una E.R. (donde `V` es un alfabeto)
* Si `X` e `Y` son E.R., entonces `X.Y` es una E.R. (parte recursiva)
* Si `X` e `Y` son E.R., entonces `X+Y` es una E.R. (concatenación)
* Si `X` es una E.R., entonces `X*` es una E.R. (clausura de cualquier E.R. es una E.R.)

Esta definición indica que las expresiones regulares pueden contener:

* Letras del alfabeto que forman palabras.
* Concatenaciones, sumas, multiplicaciones y clausuras.
* La cadena vacía `λ` (lambda). Siempre se incluye en las expresiones regulares.

**Ejemplo 1:**

Si `V = {a, b, c}`, algunas de las expresiones regulares que se pueden formar con este alfabeto son:

```
a + b*
(a + c)b
a*c*
a*(b + c)c
b(a + λ)
```

**Ejemplo 2:** 

La expresión regular del lenguaje cuyas palabras están formadas por las letras del alfabeto `V = {a, b}` y terminan en `"b"` es:

```
(a + b)*b
```

**Ejemplo 3:** 

La expresión regular del lenguaje cuyas palabras están formadas por las letras del alfabeto `V = {a, b}`, tienen longitud mayor a 2, la segunda letra es `"a"`, y la antepenúltima es `"b"`, es:

```
(a + b)a(a + b)*b(a + b)
```

Esta expresión regular se puede interpretar de la siguiente manera:

1. La primera letra puede ser `a` o `b`.
2. Luego sigue obligatoriamente una `a`.
3. Después, puede haber cualquier secuencia de `a` o `b` de cualquier longitud.
4. Posteriormente, viene una `b`.
5. Finalmente, una `a` o `b`.

**Ejemplo 4:** La expresión regular del lenguaje cuyas palabras están formadas por las letras del alfabeto `V = {a, b}` y consisten en 3 o más letras `"b"` seguidas de una letra `"a"`, es:

```
bbb*a
```

-----------

#  Operaciones con Cadenas

Claro, aquí tienes el contenido formateado en estilo markdown para un libro mdBook:


# Conceptos Fundamentales de Cadenas

## Concatenación

La concatenación es una operación fundamental en el procesamiento de cadenas. Consiste en combinar dos cadenas para formar una nueva cadena más larga. Es importante tener en cuenta que el orden de las cadenas en la concatenación importa. Por ejemplo:

```plaintext
W = "01"
X = "10"

Concatenación: WX = "0110"
```

Además, la longitud de la cadena resultante de la concatenación es igual a la suma de las longitudes de las cadenas originales:

```plaintext
|WX| = |W| + |X|
```

## Cadenas

En el manejo de cadenas, es común realizar operaciones como calcular el cuadrado de una cadena o encontrar subcadenas. Consideremos las cadenas:

```plaintext
W = "LETRA"
X = "PALABRA"
```

Para calcular el cuadrado de una cadena, simplemente concatenamos la cadena consigo misma:

```plaintext
(W)^2 = "LETRALETRA"
(X)^2 = "PALABRAPALABRA"
```

### Ejemplo de Concatenación y Cuadrado de Cadenas:

```plaintext
W = "01"
X = "10"

Concatenación: WX = "0110"
(WX)^2 = "01100110"
(W)^2 = "0101"
(X)^2 = "1010"
W^2X^2 = "01011010"
```

## Subcadena

Una subcadena es una secuencia de caracteres contenida dentro de una cadena más larga. Para la cadena "LETRA", las subcadenas posibles son:

```plaintext
Y0 = ""
Y1 = "L"
Y2 = "E"
Y3 = "T"
Y4 = "R"
Y5 = "A"
Y6 = "LE"
Y7 = "ET"
Y8 = "TR"
Y9 = "RA"
Y10 = "LET"
Y11 = "ETR"
Y12 = "TRA"
Y13 = "LETR"
Y14 = "ETRA"
Y15 = "LETRA"
```

En total, hay 15 subcadenas posibles para la cadena "LETRA".


Este contenido resalta los conceptos fundamentales de cadenas y proporciona ejemplos claros para una comprensión más profunda.


<!-- ### Fórmula para el número total de subcadenas

Hay una fórmula que te permite calcular el número total de subcadenas de una cadena de longitud \( n \) de manera rápida. Puedes utilizar la fórmula matemática:

\[ \text{Total de subcadenas} = \frac{{n \times (n + 1)}}{2} \]

Esta fórmula se deriva del hecho de que para cada longitud de subcadena \( k \) (donde \( k \) va desde \( 1 \) hasta \( n \)), hay \( n - k + 1 \) subcadenas posibles de longitud \( k \). Sumando estos números para todas las longitudes posibles de subcadenas, obtenemos el total de subcadenas.

Por ejemplo, si tienes una cadena de longitud \( 5 \) (como en tu caso), puedes calcular el número total de subcadenas usando la fórmula:

\[ \text{Total de subcadenas} = \frac{{5 \times (5 + 1)}}{2} = \frac{{5 \times 6}}{2} = \frac{{30}}{2} = 15 \]

Entonces, hay \( 15 \) subcadenas posibles en una cadena de longitud \( 5 \). Esta fórmula te permite calcular rápidamente el número total de subcadenas sin tener que enumerarlas una por una. -->