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

Nota: El cuerpo de int main()también podría escribirse como:
    int main(){printf("Hello World!");return 0;}

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

- Los comentarios de varias líneas comienzan con /* y terminan con */. El compilador ignorará cualquier texto entre /*y :*/

```c
/* The code below will print the words Hello World!
to the screen, and it is amazing */
printf("Hello World!");
```

## Variables in C































