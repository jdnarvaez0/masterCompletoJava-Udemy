# Matrices en Java

## Definición
Una matriz (array bidimensional) es una estructura de datos que permite almacenar múltiples elementos organizados en filas y columnas, formando una tabla.

## Sintaxis

### Declaración
```java
// Forma 1
tipo[][] nombreMatriz = new tipo[filas][columnas];

// Forma 2
tipo[][] nombreMatriz = {
    {valor1, valor2, valor3},
    {valor4, valor5, valor6}
};
```

### Ejemplos Comunes
Crear una matriz
```java
int[][] numeros = new int[3][3]; // Matriz 3x3 de enteros
String[][] nombres = new String[2][2]; // Matriz 2x2 de strings
```

Inicializar con valores
```java
int[][] calificaciones = {
    {90, 85, 88},
    {78, 92, 95},
    {88, 84, 90}
};
```

### Operaciones Básicas

Acceder a elementos
```java
matriz[fila][columna] = valor; // Asignar valor
valor = matriz[fila][columna]; // Obtener valor
```

Recorrer una matriz
```java
for(int i = 0; i < matriz.length; i++) {
    for(int j = 0; j < matriz[i].length; j++) {
        System.out.print(matriz[i][j] + " ");
    }
    System.out.println();
}
```

### Buenas Prácticas
- **Inicialización**: Siempre inicializa los elementos de la matriz.
- **Validación**: Verifica los índices antes de acceder a elementos.
- **Dimensiones**: Utiliza variables para las dimensiones si son dinámicas.
- **Documentación**: Comenta el propósito de la matriz y su estructura.

### Características Importantes
- Las matrices son objetos en Java.
- El índice comienza en 0.
- Pueden contener tipos primitivos o referencias a objetos.
- Son de tamaño fijo una vez creadas.
- Cada fila puede tener diferente longitud (matrices irregulares).

### Métodos Útiles
- `matriz.length`: Obtiene el número de filas.
- `matriz[i].length`: Obtiene el número de columnas en la fila `i`.