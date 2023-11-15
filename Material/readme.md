# **C**

## **C Introduction**

### ¿Qué es C?

- C es un lenguaje de programación de propósito general creado por Dennis Ritchie en los Laboratorios Bell en 1972.
- Es un idioma muy popular, a pesar de ser antiguo. La principal razón de su popularidad es que es un lenguaje fundamental en el campo de la informática.
- C está fuertemente asociado con UNIX, ya que fue desarrollado para escribir el sistema operativo UNIX.

### ¿Por qué aprender C?

- Es uno de los lenguajes de programación más populares del mundo.
- Si sabes C, no tendrás problemas para aprender otros lenguajes de programación populares como Java, Python, C++, C#, etc, ya que la sintaxis es similar.
- C es muy rápido, en comparación con otros lenguajes de programación, como Java y Python.
- C es muy versátil; Se puede utilizar tanto en aplicaciones como en tecnologías.

### Diferencia entre C y C++
- C++ fue desarrollado como una extensión de C y ambos lenguajes tienen casi la misma sintaxis.
- La principal diferencia entre C y C++ es que C++ admite clases y objetos, mientras que C no.

## **C Syntax**

### Sintaxis

Vamos a desglosarlo el siguiente código para entenderlo mejor:

```c
#include <stdio.h>

int main() {
  printf("Hello World!");
  return 0;
}
```

- Línea 1: #include <stdio.h> es una biblioteca de archivos de encabezado que nos permite trabajar con funciones de entrada y salida, como printf() (usada en la línea 4). Los archivos de encabezado agregan funcionalidad a los programas C.
- Línea 2: una línea en blanco. C ignora los espacios en blanco. Pero lo usamos para hacer que el código sea más legible.
- Línea 3: Otra cosa que siempre aparece en un programa C es main(). Esto se llama función . {}Se ejecutará cualquier código dentro de sus llaves .
- Línea 4: printf() es una función utilizada para enviar/imprimir texto en la pantalla. En nuestro ejemplo, aparecerá "¡Hola mundo!". Tenga en cuenta que: Cada declaración C termina con un punto y coma;
- Línea 5: return 0 finaliza la main()función.
- Línea 6: No olvide agregar la llave de cierre }para finalizar la función principal.

Nota: El cuerpo de int main() también podría escribirse como:
```c
int main(){printf("Hello World!");return 0;}
```

## **C Output**

### Imprimir una salida

- Para generar valores o imprimir texto en C, puede usar la función printf(). Puedes utilizar tantas funciones printf() como quieras. Sin embargo , tenga en cuenta que no inserta una nueva línea al final del resultado:

```c
#include <stdio.h>

int main() {
  printf("Hello World!");
  return 0;
}
```

### Nueva línea 

- Para insertar una nueva línea, puedes usar el carácter \n:

```c
#include <stdio.h>

int main() {
  printf("Hello World!\n");
  printf("I am learning C.");
  return 0;
}
```

- También puede generar varias líneas con una sola función printf(). Sin embargo, esto podría hacer que el código sea más difícil de leer:

```c
#include <stdio.h>

int main() {
  printf("Hello World!\nI am learning C.\nAnd it is awesome!");
  return 0;
}
```

**Consejo:** Dos caracteres \n uno detrás del otro crearán una línea en blanco:

```c
#include <stdio.h>

int main() {
  printf("Hello World!\n\n");
  printf("I am learning C.");
  return 0;
}
```

- \n    Agrega un salto de línea
- \n\n  Agrega una línea en blanco
- \t	  Agrega un tabulado al comienzo de la línea
- \\	  Inserta un carácter de barra invertida (\)	
- \"	  Inserta un carácter de comilla doble

## **C Coments**

### Comentarios de una línea

- Los comentarios de una sola línea comienzan con dos barras diagonales ( //).
- Este ejemplo utiliza un comentario de una sola línea antes de una línea de código:

```c
// This is a comment
printf("Hello World!");

printf("Hello World!"); // This is a comment
```

### Comentarios de varias líneas

- Los comentarios de varias líneas comienzan con /* y terminan con */. El compilador ignorará cualquier texto entre /* y :*/

```c
/* The code below will print the words Hello World!
to the screen, and it is amazing */
printf("Hello World!");
```

## **Variables in C**

- Las variables son contenedores para almacenar valores de datos, como números y caracteres.
- En C, existen diferentes tipos de variables (definidas con diferentes palabras clave), por ejemplo:

1. int    Almacena números enteros (números enteros), sin decimales, como 123 o -123
2. float  Almacena números de coma flotante, con decimales, como 19.99 o -19.99
3. cha    Almacena caracteres individuales, como 'a' o 'B'. Los valores de caracteres están entre comillas simples.

### Declaración (creación) de variables

- Para crear una variable, especifique el tipo y asígnele un valor:

```c
type variableName = value;
```

- *type*          Tipo de variable, cmo int o float.
- *variableName*  Nombre de la variable (como x o miNombre).
- *=*             El signo igual se utiliza para asignar un valor a la variable.

```c
int myNum = 15;
```

- También puedes declarar una variable sin asignar el valor y asignar el valor más tarde:

```c
// Declare a variable
int myNum;

// Assign a value to the variable
myNum = 15;
```

### Variables de salida

- Se puede generar la salida de valores o imprimir texto con la función printf():
- En muchos otros lenguajes de programación (como Python , Java y C++ ), normalmente se usa una función de impresión para mostrar el valor de una variable. Sin embargo, esto no es posible en C:

```c
int myNum = 15;
printf(myNum);  // Nothing happens
```

- Para imprimir variables en C se utilizan los especificadores de formato.

### Especificadores de formato

- Los especificadores de formato se utilizan junto con la función printf() para indicarle al compilador qué tipo de datos está almacenando la variable. Básicamente es un marcador de posición para el valor de la variable.
- Un especificador de formato comienza con un signo de porcentaje %, seguido de un carácter. Por ejemplo, para generar el valor de una variable int se debe usar el especificador de formato *%d* o *%i* entre comillas dobles, dentro de la función printf():

```c
int myNum = 15;
printf("%d", myNum);  // Outputs 15
```

- Para imprimir otros tipo se utiliza lo siguiente:

```c
int myNum = 15;            // Integer (whole number)
float myFloatNum = 5.99;   // Floating point number
char myLetter = 'D';       // Character

// Print variables
printf("%d\n", myNum);
printf("%i\n", myNum);
printf("%f\n", myFloatNum);
printf("%c\n", myLetter);
```

- Para combinar texto y una variable, sepárelos con una coma dentro de la función printf():

```c
int myNum = 15;
printf("My favorite number is: %d", myNum);
```

- Para imprimir diferentes tipos en una sola función printf():

```c
int myNum = 15;
char myLetter = 'D';
printf("My number is %d and my letter is %c", myNum, myLetter);
```

### Cambiar valores de variables

**Nota:** Si asigna un nuevo valor a una variable existente, sobrescribirá el valor anterior

```c
int myNum = 15;  // myNum is 15
myNum = 10;  // Now myNum is 10
```

- También se le puede asignar el valor de una variable a otra:

```c
int myNum = 15;

int myOtherNum = 23;

// Assign the value of myOtherNum (23) to myNum
myNum = myOtherNum;

// myNum is now 23, instead of 15
printf("%d", myNum);
```

- O copie valores a variables vacías:

```c
// Create a variable and assign the value 15 to it
int myNum = 15;

// Declare a variable without assigning it a value
int myOtherNum;

// Assign the value of myNum to myOtherNum
myOtherNum = myNum;

// myOtherNum now has 15 as a value
printf("%d", myOtherNum);
```

### Agregar variables juntas

- Para agregar una variable junto a otra variable puede utiliza el operador *+*:

```c
int x = 5;
int y = 6;
int sum = x + y;
printf("%d", sum);
```

### Declarar múltiples variables

- Para declarar más de una variable del mismo tipo se utiliza una lista separada por comas:

```c
int x = 5, y = 6, z = 50;
printf("%d", x + y + z);
```

- También se puede asignar el mismo valor a múltiples variables del mismo tipo:

```c
int x, y, z;
x = y = z = 50;
printf("%d", x + y + z);
```

### Nombres de las variables

- Todas las variables C deben identificarse con nombres únicos. Estos nombres únicos se denominan identificadores.
- Los identificadores pueden ser nombres cortos (como xey) o nombres más descriptivos (edad, suma, volumen total).

**Nota:** Se recomienda utilizar nombres descriptivos para crear código comprensible y mantenible:

```c
// Good
int minutesPerHour = 60;

// OK, but not so easy to understand what m actually is
int m = 60;
```

- Reglas generales para nombrar variables:

  1. Los nombres pueden contener letras, dígitos y guiones bajos.
  2. Los nombres deben comenzar con una letra o un guión bajo (_)
  3. Los nombres distinguen entre mayúsculas y minúsculas (*myVar* y *myvar* son variables distintas)
  4. Los nombres no pueden contener espacios en blanco ni caracteres especiales como !, #, %, etc.
  5. Las palabras reservadas (como int) no se pueden utilizar como nombres.

## **Data Types in C**
















































