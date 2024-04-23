
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
* La cadena vacía `λ` (lambda).

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
