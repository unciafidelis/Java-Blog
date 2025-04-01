

Claro, aquí tienes la información proporcionada en formato Markdown:

```markdown
# Ejemplos de Estructuras de Datos en Java

En Java, las estructuras de datos como **arreglos**, **listas**, **tuplas**, **conjuntos** y **diccionarios** tienen sus propias características y métodos asociados. A continuación, te proporciono ejemplos de cada una de estas estructuras y algunas de las funciones más comunes que puedes usar para operar con ellas.

---

## 1. Arreglos (Arrays)

En Java, los arreglos son estructuras de datos fijas y se crean con un tamaño determinado. No puedes agregar o eliminar elementos de un arreglo una vez que se ha creado, pero sí puedes modificar los elementos existentes.

**Ejemplo:**

```java
public class Main {
    public static void main(String[] args) {
        // Crear un arreglo de enteros
        int[] arreglo = new int[5];  // Arreglo de tamaño 5

        // Asignar valores a los elementos
        arreglo[0] = 10;
        arreglo[1] = 20;
        arreglo[2] = 30;
        arreglo[3] = 40;
        arreglo[4] = 50;

        // Modificar un valor
        arreglo[2] = 35;

        // Imprimir el arreglo
        for (int i = 0; i < arreglo.length; i++) {
            System.out.println("Elemento " + i + ": " + arreglo[i]);
        }
    }
}
```

**Funciones comunes:**
- Acceso a elementos: `arreglo[i]`
- Modificación de elementos: `arreglo[i] = nuevoValor`
- Obtener el tamaño: `arreglo.length`

---

## 2. Listas (ArrayList)

`ArrayList` es una estructura de datos que permite agregar, eliminar y modificar elementos de manera dinámica.

**Ejemplo:**

```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        // Crear una lista de enteros
        ArrayList<Integer> lista = new ArrayList<>();

        // Agregar elementos
        lista.add(10);
        lista.add(20);
        lista.add(30);

        // Modificar un elemento (índice 1)
        lista.set(1, 25);

        // Eliminar un elemento (índice 0)
        lista.remove(0);

        // Imprimir la lista
        for (int i : lista) {
            System.out.println(i);
        }
    }
}
```

**Funciones comunes:**
- Agregar un elemento: `lista.add(elemento)`
- Modificar un elemento: `lista.set(indice, nuevoValor)`
- Eliminar un elemento: `lista.remove(indice)` o `lista.remove(elemento)`
- Obtener el tamaño: `lista.size()`
- Acceder a un elemento: `lista.get(indice)`

---

## 3. Tuplas (No existe una clase Tuple en Java, pero se puede simular con clases o con `AbstractMap.SimpleEntry`)

Java no tiene un tipo de dato llamado "tupla" como en otros lenguajes. Sin embargo, se puede simular con una clase personalizada o con `AbstractMap.SimpleEntry` para almacenar pares clave-valor.

**Ejemplo (usando `AbstractMap.SimpleEntry`):**

```java
import java.util.AbstractMap;

public class Main {
    public static void main(String[] args) {
        // Crear una tupla (pareja de valores)
        AbstractMap.SimpleEntry<String, Integer> tupla = new AbstractMap.SimpleEntry<>("Uno", 1);

        // Acceder a los valores
        System.out.println("Clave: " + tupla.getKey() + ", Valor: " + tupla.getValue());
    }
}
```

**Funciones comunes:**
- Acceder a la clave: `tupla.getKey()`
- Acceder al valor: `tupla.getValue()`

---

## 4. Conjuntos (HashSet)

`HashSet` es una estructura de datos que no permite elementos duplicados. Proporciona operaciones para agregar, eliminar y comprobar la existencia de elementos.

**Ejemplo:**

```java
import java.util.HashSet;

public class Main {
    public static void main(String[] args) {
        // Crear un conjunto de enteros
        HashSet<Integer> conjunto = new HashSet<>();

        // Agregar elementos
        conjunto.add(10);
        conjunto.add(20);
        conjunto.add(30);

        // Intentar agregar un elemento duplicado
        conjunto.add(20);  // No se agregará porque ya existe

        // Eliminar un elemento
        conjunto.remove(10);

        // Comprobar si un elemento existe
        if (conjunto.contains(20)) {
            System.out.println("El elemento 20 está en el conjunto.");
        }

        // Imprimir el conjunto
        for (int i : conjunto) {
            System.out.println(i);
        }
    }
}
```

**Funciones comunes:**
- Agregar un elemento: `conjunto.add(elemento)`
- Eliminar un elemento: `conjunto.remove(elemento)`
- Verificar existencia de un elemento: `conjunto.contains(elemento)`
- Obtener el tamaño: `conjunto.size()`

---

## 5. Diccionarios (HashMap)

`HashMap` es una estructura de datos que almacena pares clave-valor. Permite agregar, eliminar y acceder a valores a través de sus claves.

**Ejemplo:**

```java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        // Crear un diccionario con claves de tipo String y valores de tipo Integer
        HashMap<String, Integer> diccionario = new HashMap<>();

        // Agregar pares clave-valor
        diccionario.put("Uno", 1);
        diccionario.put("Dos", 2);
        diccionario.put("Tres", 3);

        // Modificar un valor (clave "Dos")
        diccionario.put("Dos", 22);

        // Eliminar un par clave-valor
        diccionario.remove("Tres");

        // Acceder a un valor por su clave
        System.out.println("Valor de la clave 'Uno': " + diccionario.get("Uno"));

        // Comprobar si una clave existe
        if (diccionario.containsKey("Dos")) {
            System.out.println("La clave 'Dos' está en el diccionario.");
        }

        // Imprimir el diccionario
        for (String clave : diccionario.keySet()) {
            System.out.println("Clave: " + clave + ", Valor: " + diccionario.get(clave));
        }
    }
}
```

**Funciones comunes:**
- Agregar un par clave-valor: `diccionario.put(clave, valor)`
- Modificar un valor: `diccionario.put(clave, nuevoValor)`
- Eliminar un par clave-valor: `diccionario.remove(clave)`
- Obtener un valor por clave: `diccionario.get(clave)`
- Verificar si una clave existe: `diccionario.containsKey(clave)`
- Obtener el tamaño: `diccionario.size()`

---

## Resumen

- **Arreglos**: Tienen tamaño fijo. Se accede y modifica mediante índices.
- **Listas** (`ArrayList`): Dinámicas, permiten agregar, eliminar y modificar elementos.
- **Tuplas**: No hay una implementación directa, pero puedes usar clases como `AbstractMap.SimpleEntry`.
- **Conjuntos** (`HashSet`): No permiten duplicados. Se puede agregar, eliminar y verificar existencia de elementos.
- **Diccionarios** (`HashMap`): Almacenan pares clave-valor y permiten agregar, eliminar y acceder a los valores mediante sus claves.
```

Este formato es ideal para ser usado en plataformas como GitHub o cualquier editor que soporte Markdown. Puedes copiar y pegar este texto en tu archivo Markdown para tener los ejemplos y explicaciones bien estructurados.
