# Arrays en Java

Los arrays en Java son estructuras de datos que permiten almacenar múltiples valores del mismo tipo en una sola variable. Son de tamaño fijo, lo que significa que una vez que se define su tamaño, no puede cambiarse. Los arrays pueden ser de tipos primitivos (como `int`, `double`, `char`, etc.) o de objetos (como `String`, `Integer`, etc.).

## Características de los Arrays
- **Tamaño fijo**: El tamaño de un array se define al crearlo y no puede modificarse.
- **Indexado**: Los elementos de un array se acceden mediante un índice, que comienza en 0.
- **Homogéneo**: Todos los elementos de un array deben ser del mismo tipo.
- **Almacenamiento contiguo**: Los elementos se almacenan en posiciones de memoria consecutivas.

## Declaración de Arrays

### Sintaxis Básica
```java
tipo[] nombreArray; // Declaración
nombreArray = new tipo[tamaño]; // Inicialización
```

O también:

```java
tipo[] nombreArray = new tipo[tamaño]; // Declaración e inicialización en una línea
```

### Ejemplo:

```java
int[] numeros = new int[5]; // Array de enteros con 5 elementos
String[] nombres = new String[3]; // Array de cadenas con 3 elementos
```

### Inicialización de Arrays


Puedes inicializar un array con valores específicos al declararlo:

```java
tipo[] nombreArray = {valor1, valor2, valor3, ..., valorN};
```

### Ejemplo:


```java
int[] numeros = {10, 20, 30, 40, 50}; // Array de enteros inicializado
String[] frutas = {"Manzana", "Banana", "Naranja"}; // Array de cadenas inicializado
```

Acceso a Elementos de un Array

Los elementos de un array se acceden mediante su índice. El índice comienza en 0 y va hasta tamaño - 1.

Ejemplo:


```java
int[] numeros = {10, 20, 30, 40, 50};
System.out.println(numeros[0]); // Imprime 10
System.out.println(numeros[2]); // Imprime 30
```

Modificación de Elementos de un Array

Puedes cambiar el valor de un elemento utilizando su índice.

Ejemplo:

```java
int[] numeros = {10, 20, 30, 40, 50};
numeros[1] = 25; // Cambia el segundo elemento a 25
System.out.println(numeros[1]); // Imprime 25
```

### Longitud de un Array
La longitud de un array se obtiene utilizando la propiedad length.

Ejemplo:

```java
int[] numeros = {10, 20, 30, 40, 50};
System.out.println(numeros.length); // Imprime 5
```

### Recorrer un Array

Puedes recorrer un array utilizando un bucle for o un bucle for-each.

#### Ejemplo con for:

```java
int[] numeros = {10, 20, 30, 40, 50};
for (int i = 0; i < numeros.length; i++) {
    System.out.println(numeros[i]);
}
```

Ejemplo con for-each:

```java
int[] numeros = {10, 20, 30, 40, 50};
for (int numero : numeros) {
    System.out.println(numero);
}
```

### Arrays Multidimensionales

Los arrays multidimensionales son arrays de arrays. Por ejemplo, un array bidimensional es una matriz.

Declaración e Inicialización:

```java
tipo[][] nombreArray = new tipo[filas][columnas];
```

Ejemplo:

```java
int[][] matriz = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

### Acceso a Elementos:

```java
System.out.println(matriz[0][0]); // Imprime 1
System.out.println(matriz[1][2]); // Imprime 6
```

### Recorrer un Array Bidimensional:

```java
for (int i = 0; i < matriz.length; i++) {
    for (int j = 0; j < matriz[i].length; j++) {
        System.out.print(matriz[i][j] + " ");
    }
    System.out.println();
}
```

### Ejemplo Completo

```java
public class ArrayExample {
    public static void main(String[] args) {
        // Declaración e inicialización de un array
        int[] numeros = {10, 20, 30, 40, 50};

        // Acceso a elementos
        System.out.println("Primer elemento: " + numeros[0]); // 10
        System.out.println("Tercer elemento: " + numeros[2]); // 30

        // Modificación de un elemento
        numeros[1] = 25;
        System.out.println("Segundo elemento modificado: " + numeros[1]); // 25

        // Longitud del array
        System.out.println("Longitud del array: " + numeros.length); // 5

        // Recorrer el array con for
        System.out.println("Recorrido con for:");
        for (int i = 0; i < numeros.length; i++) {
            System.out.println(numeros[i]);
        }

        // Recorrer el array con for-each
        System.out.println("Recorrido con for-each:");
        for (int numero : numeros) {
            System.out.println(numero);
        }

        // Array bidimensional (matriz)
        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Recorrer la matriz
        System.out.println("Matriz:");
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                System.out.print(matriz[i][j] + " ");
            }
            System.out.println();
        }
    }
}
