# Análisis Léxico: La Puerta de Entrada al Compilador

El análisis léxico representa el primer paso en el proceso de compilación, donde el programa fuente es sometido a un minucioso escrutinio para identificar sus elementos básicos y significativos. Esta fase, también conocida como frontend del compilador, desempeña un papel fundamental al transformar el código fuente en una secuencia de tokens, los cuales servirán como base para las etapas posteriores del proceso de compilación.


## Proceso de Análisis Léxico

El análisis léxico se desarrolla en varias etapas que garantizan una adecuada interpretación del código fuente:

1. **Lectura del Programa Fuente**: En esta etapa inicial, el compilador lee el programa fuente en su totalidad.

2. **Eliminación de Espacios en Blanco y Comentarios**: Se eliminan los espacios en blanco, tabulaciones y saltos de línea para simplificar el código. Asimismo, los comentarios son descartados, ya que no son relevantes para el proceso de análisis.

3. **Agrupación en Tokens**: Los caracteres restantes se agrupan en unidades llamadas tokens. Un token es una secuencia de caracteres que representa una unidad semántica significativa dentro del código.

### Tipos de Tokens

- **Palabras Reservadas**: Representan instrucciones o comandos predefinidos en el lenguaje de programación, como IF, THEN, ELSE.

- **Operadores**: Incluyen símbolos que denotan operaciones o relaciones entre entidades, como +, >=, :=.

- **Identificadores**: Son cadenas de caracteres que representan nombres de variables, funciones o elementos definidos por el usuario, como Plazo, Tasa.

- **Constantes**: Representan valores fijos, como números enteros o decimales, por ejemplo, 30, 100.

## Interacción con el Análisis Sintáctico

La interacción entre el análisis léxico y el análisis sintáctico es crucial para garantizar la comprensión correcta del código. Esta interacción puede tomar varias formas:

- Ambas actividades se ejecutan en modo batch, procesando todo el código de una sola vez.
- Son actividades concurrentes, lo que permite una mayor eficiencia en el análisis.
- Ambas actividades pueden integrarse como rutinas del generador de código.
- El análisis léxico puede ser una rutina del análisis sintáctico, proporcionando los tokens necesarios para su procesamiento.

## Ejemplo Práctico

Esta tabla muestra cómo se identifican los tokens en un programa fuente.

| Token | Identificación del token |
|-------|---------------------------|
| ID    | 27                        |
| CTE   | 28                        |
| IF    | 59                        |
| THEN  | 60                        |
| ELSE  | 61                        |
| +     | 70                        |
| /     | 73                        |
| >=    | 80                        |
| :=    | 85                        |

ID es un identificador, CTE es una constante y los demás son palabras reservadas u operadores.



Tomemos como ejemplo el siguiente código:

```
if Plazo >= 30
then Tasa := Base + Recargo / 100  
else Tasa := Base
```

Aquí, podemos observar cómo se divide en tokens:

```
[IF] [Plazo] [>=] [30] 
[THEN] [Tasa] [:=] [Base] [+] [Recargo] [/] [100] 
[ELSE] [Tasa] [:=] [Base]
```

Este código se convierte en una secuencia de tokens significativos para el compilador, donde cada token se asocia con una identificación única:

```
[59] [27] [80] [28] 
[60] [27] [85] [27] [70] [27] [73] [28] 
[61] [27] [85] [27]
```

En este ejemplo, el token "IF" se identifica con el número 27 y el identificador "Plazo" con 27.


---

El análisis léxico es una etapa fundamental en el proceso de compilación, ya que prepara el terreno para el análisis sintáctico y semántico subsiguientes. Al descomponer el código fuente en tokens significativos, permite al compilador entender y procesar el programa de manera eficiente y precisa.