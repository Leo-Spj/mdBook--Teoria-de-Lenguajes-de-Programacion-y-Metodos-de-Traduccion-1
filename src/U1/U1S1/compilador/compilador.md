# Compilador: Conceptos Básicos

## Compilar y Compilador

| Compilar | Compilador |
|----------|------------|
| **Definición:** La compilación es el proceso de transformar un programa fuente en un programa objeto ejecutable. | **Definición:** Un compilador es una herramienta que se utiliza para traducir un programa fuente escrito en un lenguaje de alto nivel a un programa objeto ejecutable, puede ser en `binario` o en `código intermedio como el bytecode`. |
| **Objetivo:** El objetivo de la compilación es generar un programa ejecutable a partir del código fuente. | **Objetivo:** El objetivo de un compilador es generar un programa ejecutable a partir del código fuente. |
| **Resultado:** El resultado de la compilación es un programa objeto que puede ser ejecutado por la máquina objetivo. | **Funcionamiento:** Un compilador consta de varias etapas, como el análisis léxico, sintáctico, semántico, la generación de código intermedio y la optimización de código. |
| **Pasos:** La compilación consta de varias etapas, como el análisis léxico, sintáctico, semántico, la generación de código intermedio y la optimización de código. | **Tipos:** Existen diferentes tipos de compiladores, como los compiladores de una sola pasada, los compiladores de múltiples pasadas, los compiladores de optimización, etc. |
| **Herramientas:** Para compilar un programa, se utiliza un compilador específico para el lenguaje de programación en el que está escrito el programa. | **Ejemplos:** Algunos ejemplos de compiladores populares son GCC (GNU Compiler Collection), Clang, Visual C++, etc. |


## Diferencias entre compilador e intérprete

| **Diferencias** | **Compilador** | **Intérprete** |
|-----------------|----------------|----------------|
| **Proceso**     | El compilador traduce todo el programa a código máquina antes de ejecutarlo. | El intérprete traduce y ejecuta el programa línea por línea en tiempo real. |
| **Ejecución**   | El programa compilado se ejecuta más rápido ya que no necesita realizar la traducción en tiempo real. | El programa interpretado puede ser más lento ya que realiza la traducción en tiempo real durante la ejecución. |
| **Dependencias** | El programa compilado no depende del compilador una vez que se ha generado el programa objeto. | El programa interpretado depende del intérprete para su ejecución. |
| **Portabilidad** | El programa compilado puede ser ejecutado en cualquier máquina compatible con la arquitectura del programa objeto. | El programa interpretado puede requerir un intérprete específico para cada plataforma en la que se desee ejecutar. |
| **Errores**     | Los errores de compilación se detectan antes de la ejecución del programa. | Los errores de interpretación se detectan durante la ejecución del programa. |
| **Modificaciones** | Para realizar cambios en el programa, es necesario recompilarlo. | Los cambios en el programa pueden realizarse directamente sin necesidad de recompilarlo. |
| **Ejemplos de Lenguajes**    | C, C++, Java, etc. | Python, Ruby, JavaScript, etc. |

## Estructura de un compilador

De manera general el proceso de compilacion consta de 2 fases principales: 

1. **Análisis:** En esta fase, el compilador analiza el código fuente para identificar la estructura del programa y generar una representación intermedia del mismo. Esta fase se divide en tres subfases: análisis léxico, análisis sintáctico y análisis semántico.

2. **Síntesis:** En esta fase, el compilador genera el código objeto a partir de la representación intermedia generada en la fase de análisis. Esta fase también puede incluir la optimización del código generado.


