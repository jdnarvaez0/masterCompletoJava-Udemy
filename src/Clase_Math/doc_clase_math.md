# Clase Math en Java

La clase `Math` en Java es una clase utilitaria que proporciona métodos estáticos para realizar operaciones matemáticas comunes, como cálculos trigonométricos, exponenciales, logarítmicos, redondeo, y más. Está definida en el paquete `java.lang`, por lo que no es necesario importarla explícitamente.

## Métodos Comunes de la Clase Math

### Operaciones Básicas
- `Math.abs(x)`: Devuelve el valor absoluto de `x`.
- `Math.max(x, y)`: Devuelve el mayor de dos valores `x` e `y`.
- `Math.min(x, y)`: Devuelve el menor de dos valores `x` e `y`.

### Redondeo
- `Math.round(x)`: Redondea un número decimal al entero más cercano.
- `Math.ceil(x)`: Redondea un número decimal hacia arriba al entero más cercano.
- `Math.floor(x)`: Redondea un número decimal hacia abajo al entero más cercano.

### Exponenciales y Logaritmos
- `Math.pow(x, y)`: Devuelve `x` elevado a la potencia de `y`.
- `Math.sqrt(x)`: Devuelve la raíz cuadrada de `x`.
- `Math.exp(x)`: Devuelve `e` elevado a la potencia de `x`.
- `Math.log(x)`: Devuelve el logaritmo natural (base `e`) de `x`.
- `Math.log10(x)`: Devuelve el logaritmo en base 10 de `x`.

### Trigonométricas
- `Math.sin(x)`: Devuelve el seno de `x` (en radianes).
- `Math.cos(x)`: Devuelve el coseno de `x` (en radianes).
- `Math.tan(x)`: Devuelve la tangente de `x` (en radianes).
- `Math.toRadians(x)`: Convierte grados a radianes.
- `Math.toDegrees(x)`: Convierte radianes a grados.

### Números Aleatorios
- `Math.random()`: Devuelve un número aleatorio entre 0.0 (inclusive) y 1.0 (exclusivo).

### Constantes
- `Math.PI`: Representa el valor de π (pi).
- `Math.E`: Representa la base del logaritmo natural, `e`.

---

## Ejemplos de Uso

```java
public class MathExamples {
    public static void main(String[] args) {
        // Valor absoluto
        int absoluteValue = Math.abs(-10); // 10

        // Máximo y mínimo
        int max = Math.max(5, 10); // 10
        int min = Math.min(5, 10); // 5

        // Redondeo
        long rounded = Math.round(3.7); // 4
        double ceil = Math.ceil(3.2); // 4.0
        double floor = Math.floor(3.9); // 3.0

        // Exponenciales y raíces
        double power = Math.pow(2, 3); // 8.0
        double sqrt = Math.sqrt(16); // 4.0

        // Logaritmos
        double logNatural = Math.log(Math.E); // 1.0
        double logBase10 = Math.log10(100); // 2.0

        // Trigonometría
        double sinValue = Math.sin(Math.toRadians(30)); // 0.5
        double cosValue = Math.cos(Math.toRadians(60)); // 0.5
        double tanValue = Math.tan(Math.toRadians(45)); // 1.0

        // Números aleatorios
        double randomValue = Math.random(); // Un número entre 0.0 y 1.0

        // Constantes
        double pi = Math.PI; // 3.141592653589793
        double e = Math.E; // 2.718281828459045

        // Imprimir resultados
        System.out.println("Valor absoluto: " + absoluteValue);
        System.out.println("Máximo: " + max);
        System.out.println("Mínimo: " + min);
        System.out.println("Redondeo: " + rounded);
        System.out.println("Ceil: " + ceil);
        System.out.println("Floor: " + floor);
        System.out.println("Potencia: " + power);
        System.out.println("Raíz cuadrada: " + sqrt);
        System.out.println("Logaritmo natural: " + logNatural);
        System.out.println("Logaritmo base 10: " + logBase10);
        System.out.println("Seno de 30°: " + sinValue);
        System.out.println("Coseno de 60°: " + cosValue);
        System.out.println("Tangente de 45°: " + tanValue);
        System.out.println("Número aleatorio: " + randomValue);
        System.out.println("Valor de PI: " + pi);
        System.out.println("Valor de E: " + e);
    }
}
