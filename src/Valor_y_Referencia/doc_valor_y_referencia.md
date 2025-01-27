# Paso por Valor y Referencia en Java

## Conceptos Básicos

### Paso por Valor
- Java siempre pasa los argumentos por valor.
- Para tipos primitivos, se pasa una copia del valor.
- Los cambios en el método no afectan a la variable original.

### Paso por Referencia
- En Java, los objetos se pasan por referencia.
- Se pasa una copia de la referencia al objeto.
- Los cambios en el objeto afectan al original.

## Ejemplos

### 1. Paso por Valor (Tipos Primitivos)

```java
public class PasoPorValor {
    public static void main(String[] args) {
        int numero = 10;
        System.out.println("antes de llamar al método: " + numero);
        
        cambiarValor(numero);
        System.out.println("después de llamar al método: " + numero); // Sigue siendo 10
    }

    public static void cambiarValor(int valor) {
        valor = 20;
    }
}
```

### 2. Paso por Referencia (Arrays)

```java
import java.util.Arrays;

public class PasoPorReferencia {
    public static void main(String[] args) {
        int[] numeros = {1, 2, 3};
        System.out.println("antes de llamar al método: " + Arrays.toString(numeros));
        
        modificarArray(numeros);
        System.out.println("después de llamar al método: " + Arrays.toString(numeros)); // Cambia
    }

    public static void modificarArray(int[] arr) {
        arr[0] = 100;
    }
}
```

### 3. Paso por Referencia (Objetos)

```java
public class PasoPorReferenciaObjeto {
    public static void main(String[] args) {
        Persona persona = new Persona("Juan");
        System.out.println("antes de llamar al método: " + persona.getNombre());
        
        modificarPersona(persona);
        System.out.println("después de llamar al método: " + persona.getNombre()); // Cambia
    }

    public static void modificarPersona(Persona p) {
        p.setNombre("Carlos");
    }
}
```

## Diferencias Clave

| Característica | Paso por Valor | Paso por Referencia |
| -------------- | -------------- | ------------------- |
| Tipo de dato   | Primitivos     | Objetos y Arrays    |
| Modificación   | No afecta original | Afecta al original |
| Memoria        | Copia el valor | Copia la referencia |
| Eficiencia     | Mayor uso de memoria | Más eficiente |

## Consideraciones Importantes

### Inmutabilidad
- String es inmutable aunque sea un objeto.
- Los tipos wrapper (Integer, Double, etc.) también son inmutables.

### Casos Especiales
- String pool.
- Objetos inmutables.
- Referencias nulas.

## Conclusión
- Java siempre usa paso por valor.
- La confusión surge porque con objetos se pasa el valor de la referencia.
- Entender esta diferencia es crucial para el desarrollo en Java.