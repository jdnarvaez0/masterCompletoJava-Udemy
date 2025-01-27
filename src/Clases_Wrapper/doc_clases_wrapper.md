# Clases Wrapper en Java

## ¿Qué son las Clases Wrapper?

Las clases Wrapper (envoltorio) en Java son clases que permiten convertir tipos de datos primitivos en objetos y viceversa. Estas clases encapsulan un valor de un tipo primitivo en un objeto, permitiendo que los tipos primitivos sean utilizados como objetos.

## Tipos de Clases Wrapper

| Tipo Primitivo | Clase Wrapper |
|----------------|---------------|
| boolean        | Boolean       |
| char           | Character     |
| byte           | Byte          |
| short          | Short         |
| int            | Integer       |
| long           | Long          |
| float          | Float         |
| double         | Double        |

## Características Principales

1. **Autoboxing**: Conversión automática de tipos primitivos a objetos wrapper.
2. **Unboxing**: Conversión automática de objetos wrapper a tipos primitivos.
3. **Conversión entre tipos**: Métodos para convertir entre diferentes tipos de datos.
4. **Funcionalidades adicionales**: Métodos útiles para manipulación de valores.

## Ejemplos de Uso

### Creación de Objetos Wrapper

```java
// Diferentes formas de crear objetos wrapper
Integer numero1 = new Integer(50);          // Deprecated
Integer numero2 = Integer.valueOf(50);      // Forma recomendada
Integer numero3 = 50;                       // Autoboxing
```

### Conversión de String a Tipos Primitivos

```java
int i = Integer.parseInt("10");
double d = Double.parseDouble("10.5");
boolean b = Boolean.parseBoolean("true");
```

### Conversión de Tipos Primitivos a String

```java
String s1 = Integer.toString(10);
String s2 = Double.toString(10.5);
String s3 = Boolean.toString(true);
```

### Comparaciones

```java
Integer num1 = 10;
Integer num2 = 20;

System.out.println(num1.equals(num2));        // false
System.out.println(num1.compareTo(num2));     // -1
```

### Valores Máximos y Mínimos

```java
System.out.println(Integer.MAX_VALUE);        // 2147483647
System.out.println(Integer.MIN_VALUE);        // -2147483648
```

## Utilidad de las Clases Wrapper

- **Colecciones**: Las colecciones en Java solo pueden almacenar objetos, no tipos primitivos.
- **Valores null**: Los wrappers pueden contener null, los primitivos no.
- **Métodos útiles**: Proporcionan métodos para conversiones y operaciones.
- **Genericidad**: Necesarios para usar tipos genéricos en Java.

## Buenas Prácticas

- Usar autoboxing/unboxing cuando sea posible.
- Evitar crear nuevos objetos wrapper innecesariamente.
- Considerar el impacto en el rendimiento al usar wrappers.
- Manejar posibles `NullPointerException`.

## Consideraciones de Rendimiento

- Los wrappers ocupan más memoria que los tipos primitivos.
- Las operaciones con wrappers son más lentas que con primitivos.
- El autoboxing/unboxing tiene un costo en rendimiento.

## Conclusión

Las clases Wrapper son una parte fundamental de Java que proporcionan una forma de tratar tipos primitivos como objetos. Son especialmente útiles cuando se trabaja con colecciones, APIs y frameworks que requieren objetos en lugar de tipos primitivos.