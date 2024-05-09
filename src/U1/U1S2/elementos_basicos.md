# Elementos Básicos de los Lenguajes Formales Alfabetos, Cadenas y Lenguajes

Lenguajes Regulares y Fundamentos Lingüísticos

## Alfabetos

Un alfabeto se define como un conjunto no vacío de símbolos o caracteres. Se denota con la letra griega mayúscula Σ (sigma), y se cumple que `Σ ≠ ∅`, lo que significa que su cardinalidad `(|Σ|)` es mayor que cero.

Ejemplos de alfabetos:

- Σ = {a, b, c, ..., z}: Alfabeto del lenguaje español.
- Σ = {0, 1, 2, ..., 9}: Alfabeto numérico.
- Σ = {0, 1}: Alfabeto binario computacional.
- Σ = {0, 1, ..., 9, A, B, ..., F}: Alfabeto hexadecimal.

Un símbolo o carácter es un elemento perteneciente a un alfabeto dado. Por ejemplo, si `X ∈ Σ`, entonces `X` es un símbolo del alfabeto `Σ`.

## Cadenas

Las cadenas, también conocidas como palabras o strings, son yuxtaposiciones de elementos de un alfabeto. Una cadena se forma mediante la concatenación de símbolos de un alfabeto dado.

Ejemplos de cadenas en el alfabeto binario `Σ = {0, 1}`:

- W1 = 0, 1, 1, 0, 1
- W2 = 0
- W3 = ε (cadena vacía, representada por el símbolo épsilon)

El tamaño de una cadena se determina por el número de símbolos que la componen. 

Por ejemplo:

- |W1| = 5
- |W2| = 1
- |ε| = 0

## Concatenación de Cadenas

La operación de concatenación de cadenas se denota mediante la yuxtaposición de las mismas. Si `X = a1, a2, ..., an y Y = b1, b2, ..., bm`, entonces la concatenación de `X` e `Y` se representa como `XY = a1, a2, ..., an, b1, b2, ..., bm`.

Además, se pueden definir operaciones sobre conjuntos de cadenas, como la clausura de Kleene `(Σ*)` y la clausura de Kleene positiva `(Σ+)`. La clausura de Kleene de un alfabeto `Σ` se define como `Σ* = Σ0 ∪ Σ1 ∪ Σ2 ∪ ...`, donde `Σ0 = {ε}` y `Σn` representa todas las cadenas de longitud `n` formadas con símbolos de `Σ`. Por otro lado, la clausura de Kleene positiva excluye la cadena vacía: `Σ+ = Σ* - {ε}`.

Es importante tener en cuenta que el orden de las cadenas en la concatenación importa. Por ejemplo:

```plaintext
W = "01"
X = "10"

Concatenación: WX = "0110"
```

Además, la longitud de la cadena resultante de la concatenación es igual a la suma de las longitudes de las cadenas originales:

```plaintext
|WX| = |W| + |X|
```

## Ejemplo de Concatenación de Cadenas


En el manejo de cadenas, es común realizar operaciones como 'calcular el cuadrado de una cadena' o 'encontrar subcadenas'. 

Consideremos las cadenas:

```plaintext
W = "LETRA"
X = "PALABRA"
```

Para calcular el cuadrado de una cadena, simplemente concatenamos la cadena consigo misma:

```plaintext
(W)^2 = "LETRALETRA"
(X)^2 = "PALABRAPALABRA"
```

Y para encontrar la concatenación de los cuadrados de dos cadenas, simplemente concatenamos los cuadrados de las cadenas originales:

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

Una subcadena es una secuencia de caracteres contenida dentro de una cadena más larga. Por ejemplo, para la cadena "LETRA", las subcadenas posibles incluyen "LE", "ET", "TRA", entre otras. Es importante mencionar que la cadena vacía también se considera una subcadena.

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
```

En total, hay 15 subcadenas posibles para la cadena "LETRA". 
No se incluye la cadena 'LETRA' como subcadena dado que es la cadena original.


## Lenguajes

Un lenguaje sobre un alfabeto `Σ` es cualquier subconjunto de la clausura de Kleene de ese alfabeto `(Σ*)`. Se denota como `L ⊆ Σ*`. Por ejemplo, el lenguaje español es un subconjunto de todas las combinaciones posibles del alfabeto formado por las letras seria **[A-Za-zñÑ]**.

Es posible realizar operaciones sobre los lenguajes, como la concatenación. Si **L1** y **L2** son lenguajes, su concatenación se define como `L1L2 = {XY | X ∈ L1, Y ∈ L2}`.

