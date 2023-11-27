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

### Trabajar con C

- Lo hago desde una máquina virtual con OS ArchLinux, en la cual poseo instalada los repositorios de gcc para la compilación

  1. **COMPILAR FICHERO file.c:**<br>
  gcc file.c<br>
  // Genera un fichero de compilado de nombre a.c
  2. **COMPILAR FICHERO file.c Y GENERAR FICHERO DE SALIDA CON NOMBRE ESPECÍFICO:**<br>
  gcc file.c -o filename.c
  3. **EJECUTAR FICHERO COMPILADO:**<br>
  ./filename.c

## **Syntax in C**

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

- **\n** Agrega un salto de línea
- **\n\n** Agrega una línea en blanco
- **\t** Agrega un tabulado al comienzo de la línea
- **\\** Inserta un carácter de barra invertida (\)
- **\"** Inserta un carácter de comilla doble

## **C Comments**

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

  * **int** Almacena números enteros (números enteros), sin decimales, como 123 o -123
  * **float** Almacena números de coma flotante, con decimales, como 19.99 o -19.99
  * **char** Almacena caracteres individuales, como 'a' o 'B'. Los valores de caracteres están entre comillas simples.

### Declaración (creación) de variables

- Para crear una variable, especifique el tipo y asígnele un valor:

```c
type variableName = value;
```

- **type** Tipo de variable, cmo int o float.
- **variableName** Nombre de la variable (como x o miNombre).
- **=** El signo igual se utiliza para asignar un valor a la variable.

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

- ó copiar valores a variables vacías:

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

  * Los nombres pueden contener letras, dígitos y guiones bajos.
  * Los nombres deben comenzar con una letra o un guión bajo (_)
  * Los nombres distinguen entre mayúsculas y minúsculas (*myVar* y *myvar* son variables distintas)
  * Los nombres no pueden contener espacios en blanco ni caracteres especiales como !, #, %, etc.
  * Las palabras reservadas (como int) no se pueden utilizar como nombres.

## **Data Types in C**

- Una variable en C debe ser un tipo de datos específico y debes usar un especificador de formato dentro de la función  printf() para poder mostrarlo en la salida:

```c
// Create variables
int myNum = 5;             // Integer (whole number)
float myFloatNum = 5.99;   // Floating point number
char myLetter = 'D';       // Character

// Print variables
printf("%d\n", myNum);
printf("%f\n", myFloatNum);
printf("%c\n", myLetter);
```

### Tipos de datos básicos

- El tipo de datos especifica el tamaño y el tipo de información que almacenará la variable. Los más básicos son:

| **Data Type** | **Size**         | **Description**                                                                                       |
|---------------|------------------|-------------------------------------------------------------------------------------------------------|
| int           | 2 or 4 bytes     | Stores whole numbers, without decimals                                                                |
| float         | 4 bytes          | Stores fractional numbers, containing one or more decimals. Sufficient for storing 6-7 decimal digits |
| double        | 8 bytes          | Stores fractional numbers, containing one or more decimals. Sufficient for storing 15 decimal digits  |
| char          | 1 byte           | Stores a single character/letter/number, or ASCII values                                              |

```c
int myNum = 5; // 2 or 4 bytes & %d or %i
float myFloatNum = 5.99; // 4 bytes & %f
char myLetter = 'D'; // 1 byte & %c
double myDouble = 19.99; // 8 bytes & %lf
```

### Especificadores de formato básicos

- Existen diferentes especificadores de formato para cada tipo de datos. Éstos son algunos de ellos:

| **Format Specifier** | **Data Type**                                                               |
|----------------------|-----------------------------------------------------------------------------|
| %d or %i             | int                                                                         |
| %f                   | float                                                                       |
| %lf                  | double                                                                      |
| %c                   | char                                                                        |
| %s                   | Used for strings (text), which you will learn more about in a later chapter |
| %lu                  | unsigned long (sizeof)                                                      |

### Establecer precisión decimal

- Al imprimir un número de punto flotante el resultado entrega muchos dígitos después del punto decimal:

```c
float myFloatNum = 3.5;
double myDoubleNum = 19.99;

printf("%f\n", myFloatNum); // Outputs 3.500000
printf("%lf", myDoubleNum); // Outputs 19.990000
```

- Para establecer la precisión decimal se puede usar un punto (.) seguido de un número que especifica cuántos dígitos deben mostrarse después del punto decimal:

```c
float myFloatNum = 3.5;

printf("%f\n", myFloatNum); // Default will show 6 digits after the decimal point
printf("%.1f\n", myFloatNum); // Only show 1 digit
printf("%.2f\n", myFloatNum); // Only show 2 digits
printf("%.4f", myFloatNum);   // Only show 4 digits
```

## **Type Conversion in C**

- A veces, es necesario convertir el valor de un tipo de datos a otro. Esto se conoce como conversión de tipos. Por ejemplo, si intenta dividir dos números enteros (5 entre 2), esperaría que el resultado fuera 2.5. Pero como estamos trabajando con números enteros (y no con valores de punto flotante), el siguiente ejemplo simplemente generará 2:

```c
int x = 5;
int y = 2;
int sum = 5 / 2;

printf("%d", sum); // Outputs 2
```

- Para obtener el resultado correcto, necesita saber cómo funciona la conversión de tipos. Hay dos tipos de conversión en C:

  * Conversión implícita (automáticamente)
  * Conversión explícita (manualmente)

### Conversión Implícita

- El compilador realiza automáticamente la conversión implícita cuando asigna un valor de un tipo a otro. Por ejemplo, si asigna un int valor a un tipo float:

```c
// Automatic conversion: int to float
float myFloat = 9;

printf("%f", myFloat); // 9.000000
```

- Como se aprecia, el compilador convierte automáticamente el valor int 9 en un valor flotante de 9.000000. Esto puede ser arriesgado, ya que podría perder el control sobre valores específicos en determinadas situaciones. Especialmente si fuera al revés: el siguiente ejemplo convierte automáticamente el valor flotante 9.99 en un valor int de 9:

```c
// Automatic conversion: float to int
int myInt = 9.99;

printf("%d", myInt); // 9
```

- ¿Qué pasó con .99? ¡Es posible que queramos esos datos en nuestro programa! Así que cuidado. Otro ejemplo, se dividen dos números enteros: 5 entre 2 con resultado 2.5. Y como sabes desde el principio de esta página, si almacenas la suma como un número entero, el resultado solo mostrará el número 2. Por lo tanto, sería mejor almacenar la suma como a float o double.

```c
float sum = 5 / 2;

printf("%f", sum); // 2.000000
```

### Conversión Explícita

- La conversión explícita se realiza manualmente colocando el tipo entre paréntesis delante del valor. Considerando el problema del ejemplo anterior, ahora podemos obtener el resultado correcto:

```c
// Manual conversion: int to float
float sum = (float) 5 / 2;

printf("%f", sum); // 2.500000
```

- También se puede colocar el tipo delante de una variable:

```c
int num1 = 5;
int num2 = 2;
float sum = (float) num1 / num2;

printf("%f", sum); // 2.500000

int num1 = 5;
int num2 = 2;
float sum = (float) num1 / num2;

printf("%.1f", sum); // 2.5
```

## **Constants in C**

- Para que otros (o uno mismo) no puedan cambiar los valores de las variables existentes, puede utilizar la palabra clave const. Esto declarará la variable como "constante", lo que significa que no se puede modificar y es de solo lectura:

```c
const int myNum = 15;  // myNum will always be 15
myNum = 10;  // error: assignment of read-only variable 'myNum'
```

- Siempre se debe declarar la variable como constante cuando tenga valores que es poco probable que cambien:

```c
const int minutesPerHour = 60;
const float PI = 3.14;
```

### Notas sobre constantes

- Cuando se declara una variable constante, se le debe asignar un valor inmediatamente y no después, como en variables sin const:

```c
const int minutesPerHour = 60; // Esto funciona

const int minutesPerHour; // Esto NO funciona
minutesPerHour = 60; // error
```

- Una buena práctica es declararlas en mayúsculas. No es obligatorio, pero es útil para facilitar la lectura del código y es común para los programadores de C:

```c
const int BIRTHYEAR = 1980;
```

## **Operators in C**

- Los operadores se utilizan para realizar operaciones con variables y valores. En el siguiente ejemplo, utilizamos el + operador para sumar dos valores:

```c
int myNum = 100 + 50;
```

- Aunque el operador **+**se usa a menudo para sumar dos valores, también se puede usar para sumar una variable y un valor, o una variable y otra variable:

```c
int sum1 = 100 + 50;        // 150 (100 + 50)
int sum2 = sum1 + 250;      // 400 (150 + 250)
int sum3 = sum2 + sum2;     // 800 (400 + 400)
```

- En C se dividen los operadores en los siguientes grupos:

  * Operadores aritméticos
  * Operadores de Asignación
  * Operadores de comparación
  * Operadores logicos
  * Operadores bit a bit

### Operadores aritméticos

- Los operadores aritméticos se utilizan para realizar operaciones matemáticas comunes.

| **Operator** | **Name**       | **Description**                        | **Example** |
|--------------|----------------|----------------------------------------|-------------|
| +            | Addition       | Adds together two values               | x + y       |
| -            | Subtraction    | Subtracts one value from another       | x - y       |
| *            | Multiplication | Multiplies two values                  | x * y       |
| /            | Division       | Divides one value by another           | x / y       |
| %            | Modulus        | Returns the division remainder         | x % y       |
| ++           | Increment      | Increases the value of a variable by 1 | ++x         |
| --           | Decrement      | Decreases the value of a variable by 1 | --x         |

### Operadores de asignación

- Los operadores de asignación se utilizan para asignar valores a variables. En el siguiente ejemplo, utilizamos el operador de asignación **=** para asignar el valor 10 a una variable llamada x:

```c
int x = 10;
```

- El operador de asignación de suma **+=** agrega un valor a una variable:

```c
int x = 10;
x += 5;
```

- Una lista de todos los operadores de asignación:

| **Operator** | **Example**       | **Same As** |
|--------------|----------------|----------------|
| =            | x = 5          | x = 5          |
| +=           | x += 3	        | x = x + 3      |
| -=           | x -= 3	        | x = x - 3      |
| *=           | x *= 3	        | x = x * 3      |
| /=           | x /= 3	        | x = x / 3      |
| %=           | x %= 3	        | x = x % 3      |
| &=           | x &= 3	        | x = x & 3      |
| |=           | x |= 3	        | x = x | 3      |
| ^=           | x ^= 3	        | x = x ^ 3      |
| >>=          | x >>= 3	      | x = x >> 3     |
| <<=          | x <<= 3	      | x = x << 3     |

### Operadores de comparación

- Los operadores de comparación se utilizan para comparar dos valores o variables. El valor de retorno de una comparación es 1 o 0, lo que significa verdadero o falso. Estos valores se conocen como valores booleanos. En el siguiente ejemplo, utilizamos el operador mayor que > para saber si 5 es mayor que 3:

```c
int x = 5;
int y = 3;
printf("%d", x > y); // returns 1 (true) because 5 is greater than 3
```

- Una lista de todos los operadores de comparación:

| **Operator** | **Name**                 | **Example** |
|--------------|--------------------------|-------------|
| ==           | Equal to	                | x == y      |
| !=           | Not equal	              | x != y      |
| >            | Greater than	            | x > y       |
| <            | Less than	              | x < y       |
| >=           | Greater than or equal to | x >= y      |
| <=           | Less than or equal to	  | x <= y      |

### Operadores lógicos

- También puede probar valores verdaderos o falsos con operadores lógicos. Los operadores lógicos se utilizan para determinar la lógica entre variables o valores:

| **Operator** | **Name**    | **Description**                                         | **Example**        |
|--------------|------ ------|---------------------------------------------------------|--------------------|
| &&           | Logical and | Returns true if both statements are true                | x < 5 &&  x < 10   |
| ||           | Logical or  | Returns true if one of the statements is true           | x < 5 || x < 4     |
| !            | Logical not | Reverse the result, returns false if the result is true | !(x < 5 && x < 10) |

### Tamaño del operador

- El tamaño de la memoria (en bytes) de un tipo de datos o de una variable se puede encontrar con el size of operador:

```c
int myInt;
float myFloat;
double myDouble;
char myChar;

printf("%lu\n", sizeof(myInt));
printf("%lu\n", sizeof(myFloat));
printf("%lu\n", sizeof(myDouble));
printf("%lu\n", sizeof(myChar));
```

## **Booleans in C**

- Muy a menudo en programación se necesita un tipo de datos que solo pueda tener uno de dos valores, como: SÍ ó NO, ENCENDIDO ó APAGADO, VERDADERO ó FALSO.
- Para ello, C cuenta con un tipo de datos **bool**, el cual se conoce como booleanos. Los booleanos representan valores que son true o false.

### Variables booleanas

- En C, el tipo bool no es un tipo de datos integrado, como int o char.
- Se introdujo en C99 y se debe importar el siguiente archivo de encabezado para usarlo:

```c
#include <stdbool.h>
```
- Una variable booleana se declara con la palabra clave bool y solo puede tomar los valores true o false:

```c
bool isProgrammingFun = true;
bool isFishTasty = false;
```

- Antes de intentar imprimir las variables booleanas, debes saber que los valores booleanos se devuelven como números enteros:

  * 1 (o cualquier otro número que no sea 0) representa **true**
  * 0 representa **false**

- Por lo tanto, debes usar el especificador de formato %d o %i para imprimir un valor booleano (ya se trata como int):

```c
// Create boolean variables
bool isProgrammingFun = true;
bool isFishTasty = false;

// Return boolean values
printf("%d", isProgrammingFun);   // Returns 1 (true)
printf("%d", isFishTasty);        // Returns 0 (false)
```

### Comparar valores y variables

- Comparar valores es útil en programación ya que nos ayuda a encontrar respuestas y plantear una mejor toma de decisiones.
- Por ejemplo, puede utilizar un operador de comparación como el operador mayor que (>) para comparar dos valores:

```c
printf("%d", 10 > 9);  // Returns 1 (true) because 10 is greater than 9
```

- También se pueden comparar dos variables:

```c
int x = 10;
int y = 9;
printf("%d", x > y);
```

- En el siguiente ejemplo, se utiliza el operador igual a (==) para comparar diferentes valores:

```c
printf("%d", 10 == 10); // Returns 1 (true), because 10 is equal to 10
printf("%d", 10 == 15); // Returns 0 (false), because 10 is not equal to 15
printf("%d", 5 == 55);  // Returns 0 (false) because 5 is not equal to 55
```

- Por otra parte, no solo se limita a comparar números. También se pueden comparar variables booleanas, o incluso estructuras especiales, como matrices:

```c
bool isHamburgerTasty = true;
bool isPizzaTasty = true;

// Find out if both hamburger and pizza is tasty
printf("%d", isHamburgerTasty == isPizzaTasty);
```

## **If & else in C**

### Condiciones y declaraciones If

- C tiene las siguientes declaraciones condicionales:

  * Se utiliza **if** para especificar un bloque de código que se ejecutará, si se cumple una condición específica (true).
  * Se utiliza **else** para especificar un bloque de código que se ejecutará, si se cumple la misma condición (false).
  * Se utiliza **else if** para especificar una nueva condición para probar, si la primera condición es false.
  * Se utiliza **switch** para especificar muchos bloques alternativos de código que se ejecutarán a raíz de una desición tomada previamente.

### If

- Utilice la declaración **if** para especificar un bloque de código que se ejecutará si una condición es true.

```c
if (condition) {
  // block of code to be executed if the condition is true
}
```

- Tenga en cuenta que if está en letras minúsculas. Las letras mayúsculas (If o IF) generarán un error. Por ejemplo, se prueban dos valores para averiguar si 20 es mayor que 18. Si la condición es true, imprima algo de texto:

```c
if (20 > 18) {
  printf("20 is greater than 18");
}
```

- También se pueden probar variables para probar si x es mayor que y (usando el operador **>**).

```c
int x = 20;
int y = 18;
if (x > y) {
  printf("x is greater than y");
}
```

### Else

- Utilice la declaración **else** para especificar un bloque de código que se ejecutará si la condición inicial tiene como resultado false.

```c
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}
```

- Por ejemplo, el tiempo (20) es mayor que 18, por lo que la condición es false.

```c
int time = 20;
if (time < 18) {
  printf("Good day.");
} else {
  printf("Good evening.");
}
// Outputs "Good evening."
```

### Else if

- Utilice la declaración **else if** para especificar una nueva condición si la primera condición es false.

```c
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```

- Por ejemplo, el tiempo (22) es mayor que 10, por lo que la primera condición es false. La siguiente condición, en la declaración else if, también es false, por lo que pasamos a la condición else, ya que la condición1 y la condición2 son ambas false. Sin embargo, si la hora fuera las 14, el programa imprimiría "Buenos días".

```c
int time = 22;
if (time < 10) {
  printf("Good morning.");
} else if (time < 20) {
  printf("Good day.");
} else {
  printf("Good evening.");
}
// Outputs "Good evening."
```

### Short hand if else

- También existe una abreviatura **if else** que se conoce como operador ternario, porque consta de tres operandos. Se puede utilizar para reemplazar varias líneas de código con una sola línea. A menudo se utiliza para reemplazar declaraciones simples if else:

```c
variable = (condition) ? expressionTrue : expressionFalse;
```

- Esto funciona de la siguiente manera. En lugar de escribir:

```c
int time = 20;
if (time < 18) {
  printf("Good day.");
} else {
  printf("Good evening.");
}
```

- se escribe:

```c
int time = 20;
(time < 18) ? printf("Good day.") : printf("Good evening.");
```

- Aquí la declaración principal **(time < 18)** se asume como sentencia **if**. El caracter **?** toma la función de un **entonces**. Finalmente, el caracter **:** se utiliza como un **else**

## **Switch in C**

### Switch

- En lugar de escribir muchas declaraciones **if..else**, se puede utilizar la declaración **switch**. Esta declaración selecciona uno de los muchos bloques de código que se ejecutarán:

```c
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

- Su funcionamiento se ejecuta de ls siguiente manera:

  * La expresión **switch** se evalúa una vez.
  * El valor de la expresión se compara con los valores de cada **case**.
  * Si hay una coincidencia, se ejecuta el bloque de código asociado.
  * La declaración **break** sale del bloque de cambio y detiene la ejecución del **switch**.
  * La declaración **defaul** es opcional y especifica algún código que se ejecutará si no hay coincidencia de casos dentro del **switch**-

- El siguiente ejemplo utiliza el número del día de la semana para calcular el nombre asignado a este:

```c
int day = 4;

switch (day) {
  case 1:
    printf("Monday");
    break;
  case 2:
    printf("Tuesday");
    break;
  case 3:
    printf("Wednesday");
    break;
  case 4:
    printf("Thursday");
    break;
  case 5:
    printf("Friday");
    break;
  case 6:
    printf("Saturday");
    break;
  case 7:
    printf("Sunday");
    break;
}

// Outputs "Thursday" (day 4)
```

### Break

- Cuando C alcanza un **break** finaliza el proceso actual y sale del bloque que se encuentra en ejecución. Esto detiene por completo la ejecución de más código y pruebas de casos dentro del bloque.
- Cuando se encuentra una coincidencia y el trabajo está hecho, es hora de hacer un descanso. No hay necesidad de realizar más pruebas.
- Una interrupción puede ahorrar mucho tiempo de ejecución porque "ignora" la ejecución del resto del código en el bloque de cambio.

### Default

- AL ejecutar un **default** se especifica algún código que se ejecutará si no hay coincidencia de casos dentro del **switch**:

```c
int day = 4;

switch (day) {
  case 6:
    printf("Today is Saturday");
    break;
  case 7:
    printf("Today is Sunday");
    break;
  default:
    printf("Looking forward to the Weekend");
}

// Outputs "Looking forward to the Weekend"
```

- La palabra clave predeterminada debe usarse como última declaración en el cambio y no necesita interrupción.

## **While loop**

### Bucles

- Los bucles pueden ejecutar un bloque de código siempre que se alcance una condición específica.
- Los bucles son útiles porque ahorran tiempo, reducen errores y hacen que el código sea más legible.

### While

- El bucle **while** recorre un bloque de código siempre que una condición especificada sea true:

```c
while (condition) {
  // code block to be executed
}
```

- En el siguiente ejemplo, el código del bucle se ejecutará una y otra vez, siempre que una variable (i) sea menor que 5:

```c
int i = 0;

while (i < 5) {
  printf("%d\n", i);
  i++;
}
```

- No olvides aumentar la variable utilizada en la condición **i++**, de lo contrario el bucle será infinito y no acabará nunca. Esto puede generar un aumento drástico en el consumo de memoria utilizada para el cálculo.

### Do/While

- El bucle **do/while** es una variante del bucle **while**. Este bucle ejecutará el bloque de código una vez antes de verificar si la condición es verdadera, luego repetirá el bucle mientras la condición sea verdadera.

```c
do {
  // code block to be executed
}
while (condition);
```

- El siguiente ejemplo utiliza un bucle do/while, el cual se ejecuta al menos una vez, incluso si la condición es falsa, ya que el bloque de código se ejecuta antes de que se pruebe la condición:

```c
int i = 0;

do {
  printf("%d\n", i);
  i++;
}
while (i < 5);
```

## **For loop**

### For

- Cuando sepa exactamente cuántas veces desea recorrer un bloque de código, use el bucle **for** en lugar de un bucle while:

```c
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```

- La declaración 1 se ejecuta (una vez) antes de la ejecución del bloque de código.
- La declaración 2 define la condición para ejecutar el bloque de código.
- La declaración 3 se ejecuta (cada vez) después de que se haya ejecutado el bloque de código.

- El siguiente ejemplo imprimirá los números del 0 al 4:

```c
int i;

for (i = 0; i < 5; i++) {
  printf("%d\n", i);
}
```

- Otro ejemplo, el cual solo imprime valores pares entre 0 y 10:

```c
for (i = 0; i <= 10; i = i + 2) {
  printf("%d\n", i);
}
```

### Bucles anidados

- También es posible colocar un bucle dentro de otro bucle. Esto se llama bucle anidado.
- El bucle interno se ejecutará una vez por cada iteración del bucle externo:

```c
int i, j;

// Outer loop
for (i = 1; i <= 2; ++i) {
  printf("Outer: %d\n", i);  // Executes 2 times

  // Inner loop
  for (j = 1; j <= 3; ++j) {
    printf(" Inner: %d\n", j);  // Executes 6 times (2 * 3)
  }
}
```

## **Break & Continue in C**

### Break

- La declaración **break** se puede utilizar para salir de un bucle.
- El siguiente ejemplo salta del bucle for cuando i es igual a 4:

```c
int i;

for (i = 0; i < 10; i++) {
  if (i == 4) {
    break;
  }
  printf("%d\n", i);
}
```

### Continue

- La declaración ***continue** interrumpe una iteración en el bucle si se produce una condición específica, para luego continuar con la siguiente.
- Este ejemplo omite el valor de 4:

```c
int i;

for (i = 0; i < 10; i++) {
  if (i == 4) {
    continue;
  }
  printf("%d\n", i);
}
```

### Break & continue en el bucle While

- También se puede usar break y continue en bucles while:

```c
int i = 0;

while (i < 10) {
  if (i == 4) {
    break;
  }
  printf("%d\n", i);
  i++;
}
```
```c
int i = 0;

while (i < 10) {
  if (i == 4) {
    i++;
    continue;
  }
  printf("%d\n", i);
  i++;
}
```

## **Arrays in C**

### Arrays

- Los arrays o matrices se utilizan para almacenar múltiples valores en una sola variable, en lugar de declarar variables separadas para cada valor.
- Para crear una matriz se define el tipo de dato y se especifica el nombre de la matriz seguido de corchetes [].
- Para insertar valores, use una lista separada por comas dentro de llaves:

```c
int myNumbers[] = {25, 50, 75, 100};
```

### Acceder a los elementos de una matriz

- Para acceder a un elemento de la matriz consulte su número de índice. Los índices de matriz comienzan con 0: [0] es el primer elemento. [1] es el segundo elemento, etc.
- Esta declaración accede al valor del primer elemento [0] en myNumbers:

```c
int myNumbers[] = {25, 50, 75, 100};
printf("%d", myNumbers[0]);

// Outputs 25
```

### Cambiar un elemento de matriz

- Para cambiar el valor de un elemento específico, consulte el número de índice:

```c
myNumbers[0] = 33;
Ejemplo
int myNumbers[] = {25, 50, 75, 100};
myNumbers[0] = 33;

printf("%d", myNumbers[0]);

// Now outputs 33 instead of 25
```

### Recorrer una matriz

- Puede recorrer los elementos de la matriz con el bucle **for**.
- El siguiente ejemplo genera todos los elementos de la matriz myNumbers:

```c
int myNumbers[] = {25, 50, 75, 100};
int i;

for (i = 0; i < 4; i++) {
  printf("%d\n", myNumbers[i]);
}
```

### Establecer tamaño de matriz

- Otra forma común de crear matrices es especificar el tamaño de la matriz y agregar elementos más adelante:

```c
// Declare an array of four integers:
int myNumbers[4];

// Add elements
myNumbers[0] = 25;
myNumbers[1] = 50;
myNumbers[2] = 75;
myNumbers[3] = 100;
```

- Al utilizar este método se debe conocer el tamaño de la matriz para que el programa almacene suficiente memoria.
- No se puede cambiar el tamaño de una matriz después de la creación.

## **Multidimensional Arrays in C**

### Matrices multidimensionales

- Si se desea almacenar datos en forma tabular, como una tabla con filas y columnas, se debe usar una matriz multidimensional.
- Estas básicamente son una matriz de matrices.
- Las matrices pueden tener cualquier número de dimensiones.

### Matrices bidimensionales

- Una matriz 2D es una tabla de filas y columnas.
- Para crear una matriz 2D de números enteros se utiliza la siguiente sintaxis:

```c
int matrix[2][3] = { {1, 4, 2}, {3, 6, 8} };
```

- La primera dimensión representa el número de filas [2], mientras que la segunda dimensión representa el número de columnas [3].
- Los valores se colocan en orden de filas y se pueden visualizar así:

|       | **Column 0** | **Column 1** | **Column 2** |
|-------|--------------|--------------|--------------|
| Row 0 | 1	           | 4            | 2            |
| Row 1 | 3	           | 6            | 8            |

### Acceder a los elementos de una matriz 2D

- Para acceder a un elemento de una matriz bidimensional se debe especificar el número de índice tanto de la fila como de la columna.
- Esta declaración accede al valor del elemento en la primera fila (0) y la tercera columna (2) de la matriz.

```c
int matrix[2][3] = { {1, 4, 2}, {3, 6, 8} };

printf("%d", matrix[0][2]);  // Outputs 2
```

### Cambiar elementos en una matriz 2D

- Para cambiar el valor de un elemento, consulte el número de índice del elemento en cada una de las dimensiones:
- El siguiente ejemplo cambia el valor del elemento en la primera fila (0) y la primera columna (0):

```c
int matrix[2][3] = { {1, 4, 2}, {3, 6, 8} };
matrix[0][0] = 9;

printf("%d", matrix[0][0]);  // Now outputs 9 instead of 1
```

### Recorrer una matriz 2D

- Para recorrer una matriz multidimensional se necesita un bucle para cada una de las dimensiones de la matriz.
- El siguiente ejemplo genera todos los elementos de la matriz:

```c
int matrix[2][3] = { {1, 4, 2}, {3, 6, 8} };

int i, j;
for (i = 0; i < 2; i++) {
  for (j = 0; j < 3; j++) {
    printf("%d\n", matrix[i][j]);
  }
}
```

## **Strings in C**

### Strings

- Los strings se utilizan para almacenar texto/caracteres. Por ejemplo, "Hola mundo" es una cadena de caracteres.
- A diferencia de muchos otros lenguajes de programación, C no tiene un tipo String para crear fácilmente variables de cadena. En su lugar, debes usar el tipo **chart** y crear una matriz de caracteres para crear un string:

```c
char greetings[] = "Hello World!";
```

- Para generar una string, se puede utilizar la función **printf()** junto con el especificador de formato **%s** para indicarle a C que ahora estamos trabajando con strings:

```c
char greetings[] = "Hello World!";
printf("%s", greetings);
```

### Strings de acceso

- Dado que los strings son en realidad matrices en C, se puede acceder a un string consultando su número de índice entre corchetes [ ].

```c
char greetings[] = "Hello World!";
printf("%c", greetings[0]);
```

### Modificar strings

- Para cambiar el valor de un carácter específico en un string, consulte el número de índice y utilice comillas simples:

```c
char greetings[] = "Hello World!";
greetings[0] = 'J';
printf("%s", greetings);
// Outputs Jello World! instead of Hello World!
```

### Bucle a través de un string

- También se puede recorrer los caracteres de un string¿, usando un bucle **for**:

```c
char carName[] = "Volvo";
int i;

for (i = 0; i < 5; ++i) {
  printf("%c\n", carName[i]);
}
```

### Otra forma de crear cadenas

- En los ejemplos anteriores, se ha utilizado un "literal de cadena" para crear una variable de string. Esta es la forma más sencilla de crear un string en C.
- POr otro lado, se debe tener en cuenta que se puede crear un string con un conjunto de caracteres. Este ejemplo producirá el mismo resultado que el ejemplo al principio de esta página:

```c
char greetings[] = {'H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd', '!', '\0'};
printf("%s", greetings);
```

**Nota:** ¿Por qué incluimos el **\0** al final? Esto se conoce como "carácter de terminación nulo" y debe incluirse al crear strings utilizando este método. Le dice a C que este es el final del string.

### Diferencias

- La diferencia entre las dos formas de crear strings es que el primer método es más fácil de escribir y no es necesario incluir el carácter **\0**, ya que C lo hará por usted.
- Se debe tener en cuenta que el tamaño de ambas matrices es el mismo: ambas tienen 13 caracteres (por cierto, el espacio también cuenta como un carácter), incluido el carácter **\0**:

```c
char greetings[] = {'H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd', '!', '\0'};
char greetings2[] = "Hello World!";

printf("%lu\n", sizeof(greetings));   // Outputs 13
printf("%lu\n", sizeof(greetings2));  // Outputs 13
```

## **Special character in C**

### Strings y Caracteres especiales

- Debido a que un string debe escribirse entre comillas, C malinterpretará esta cadena y generará un error:

```c
char txt[] = "We are the so-called "Vikings" from the north.";
```

- La solución para evitar este problema es utilizar el carácter de escape de barra invertida .
- El carácter de escape de barra invertida (**\\**) convierte los caracteres especiales en caracteres de cadena:


| **Escape character** | **Result** | **Description**|
|----------------------|------------|----------------|
| \\'                  | '          | Single quote   |
| \\"                  | "          | Double quote   |
| \\\\                 | \\         | Backslash      |

- La secuencia \\"  inserta una comilla doble en una cadena:

```c
char txt[] = "We are the so-called \"Vikings\" from the north.";
```

- La secuencia \\'  inserta una comilla simple en una cadena:

```c
char txt[] = "It\'s alright.";
```

- La secuencia \\\\  inserta una única barra invertida en una cadena:

```c
char txt[] = "The character \\ is called backslash.";
```

- Otros caracteres de escape populares en C son:

| **Escape character** | **Result** |
|----------------------|------------|
| \\n                  | New line   |
| \\t                  | Tab        |
| \\0                  | Null       |

## **String Functions in C**

### Funciones de cadena

- C también tiene muchas funciones de cadena útiles, que pueden usarse para realizar ciertas operaciones con strings.
- Para usarlos, se debe incluir la librería <string.h> en el encabezado del programa:

```c
#include <string.h>
```

### Longitud de un string

- Por ejemplo, para obtener la longitud de un string, se puede usar la función **strlen()**:

```c
char alphabet[] = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
printf("%d", strlen(alphabet));
```

- En el capítulo **Strings in C**, solíamos sizeofobtener el tamaño de una cadena/matriz.
- Se debe tener en cuenta que **sizeof** y **strlen** se comportan de manera diferente, ya que **sizeof** también incluye el carácter **\0** al contar:

```c
char alphabet[] = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
printf("%d", strlen(alphabet));   // 26
printf("%d", sizeof(alphabet));   // 27
```

- También es importante saber que **sizeof** siempre devolverá el tamaño de la memoria (en bytes), y no la longitud real de la cadena:

```c
char alphabet[50] = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
printf("%d", strlen(alphabet));   // 26
printf("%d", sizeof(alphabet));   // 50
```

### Concatenar strings

- Para concatenar (combinar) dos strings, puede utilizar la función **strcat()**:

```c
char str1[20] = "Hello ";
char str2[] = "World!";

// Concatenate str2 to str1 (result is stored in str1)
strcat(str1, str2);

// Print str1
printf("%s", str1);
```

- Se debe tener en cuenta que el tamaño de **str1** debe ser lo suficientemente grande como para almacenar el resultado de las dos cadenas combinadas (20 en el ejemplo).

### Copiar strings

- Para copiar el valor de un string en otro, se puede usar la función **strcpy()**:

```c
char str1[20] = "Hello World!";
char str2[20];

// Copy str1 to str2
strcpy(str2, str1);

// Print str2
printf("%s", str2);
```

- Se debe tener en cuenta que el tamaño de **str2** debe ser lo suficientemente grande como para almacenar la cadena copiada (20 en el ejemplo).

### Comparar strings

- Para comparar dos strings, puede utilizar la función **strcmp(**)**.
- Esta devolverá 0 si las dos strings son iguales; en caso contrario, un valor que no es 0:

```c
char str1[] = "Hello";
char str2[] = "Hello";
char str3[] = "Hi";

// Compare str1 and str2, and print the result
printf("%d\n", strcmp(str1, str2));  // Returns 0 (the strings are equal)

// Compare str1 and str3, and print the result
printf("%d\n", strcmp(str1, str3));  // Returns -4 (the strings are not equal)
```
