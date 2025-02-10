---
layout: post
title:  "Estructuras básicas de JAVA"
date: 2025-02-05
categories: [Lenguaje,JAVA]
tags: [estructura]
---

<h1>Cheatsheet de Java</h1>  

### **1️⃣ Listas (ArrayList - Estructura Lineal)**
```java
import java.util.ArrayList; // Importación necesaria

public class EjemploArrayList {
    public static void main(String[] args) {
        ArrayList<String> lista = new ArrayList<>(); // Crear lista
        lista.add("Java");   // Agregar elementos
        lista.add("Python");
        lista.add("C++");

        System.out.println("Lista: " + lista); // Imprimir lista

        lista.remove("Python"); // Eliminar elemento
        System.out.println("Lista después de eliminar: " + lista);
    }
}
```

### **2️⃣ Pilas (Stack - Estructura LIFO)**
```java
import java.util.Stack; // Importación necesaria

public class EjemploStack {
    public static void main(String[] args) {
        Stack<Integer> pila = new Stack<>(); // Crear pila
        pila.push(10); // Agregar elementos
        pila.push(20);
        pila.push(30);

        System.out.println("Pila: " + pila); 
        System.out.println("Elemento removido: " + pila.pop()); // Extraer último elemento
    }
}
```

### **3️⃣ Colas (Queue - FIFO)**
```java
import java.util.LinkedList;
import java.util.Queue;

public class EjemploQueue {
    public static void main(String[] args) {
        Queue<String> cola = new LinkedList<>(); // Crear cola
        cola.add("Elemento1");
        cola.add("Elemento2");
        cola.add("Elemento3");

        System.out.println("Cola: " + cola);
        System.out.println("Elemento removido: " + cola.poll()); // Eliminar el primero en entrar
    }
}
```

### **4️⃣ Conjuntos (HashSet - No permite duplicados)**
```java
import java.util.HashSet;

public class EjemploHashSet {
    public static void main(String[] args) {
        HashSet<Integer> conjunto = new HashSet<>();
        conjunto.add(1);
        conjunto.add(2);
        conjunto.add(2); // No se agregará porque ya existe

        System.out.println("Conjunto: " + conjunto);
    }
}
```

### **5️⃣ Diccionarios (HashMap - Clave-Valor)**
```java
import java.util.HashMap;

public class EjemploHashMap {
    public static void main(String[] args) {
        HashMap<String, Integer> mapa = new HashMap<>();
        mapa.put("Juan", 25);
        mapa.put("María", 30);

        System.out.println("Edad de Juan: " + mapa.get("Juan"));
    }
}
```

### **6️⃣ Árboles (TreeSet - Ordenado)**
```java
import java.util.TreeSet;

public class EjemploTreeSet {
    public static void main(String[] args) {
        TreeSet<Integer> arbol = new TreeSet<>();
        arbol.add(5);
        arbol.add(3);
        arbol.add(8);

        System.out.println("Árbol ordenado: " + arbol);
    }
}
```

---

## **📌 Declaración de Clases, Atributos, Métodos e Instancias en Java**

### **1️⃣ Declaración de una Clase con Constructor, Métodos y Atributos**
```java
class Persona {
    // Atributos
    String nombre;
    int edad;

    // Constructor
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    // Método sin parámetros
    public void mostrarInformacion() {
        System.out.println("Nombre: " + nombre + ", Edad: " + edad);
    }

    // Método con parámetros
    public void actualizarEdad(int nuevaEdad) {
        this.edad = nuevaEdad;
    }
}
```

### **2️⃣ Uso de Objetos (Instancias)**
```java
public class EjemploPersona {
    public static void main(String[] args) {
        Persona persona1 = new Persona("Carlos", 28); // Crear objeto
        persona1.mostrarInformacion(); // Llamar método

        persona1.actualizarEdad(30); // Actualizar edad
        persona1.mostrarInformacion();
    }
}
```

---

## **📌 Entrada y Salida de Datos en Java**

### **1️⃣ Leer Datos desde la Terminal con `Scanner`**
```java
import java.util.Scanner;

public class EntradaDatos {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Leer un string
        System.out.print("Ingrese su nombre: ");
        String nombre = scanner.nextLine();

        // Leer un entero
        System.out.print("Ingrese su edad: ");
        int edad = scanner.nextInt();

        // Mostrar datos ingresados
        System.out.println("Nombre: " + nombre + ", Edad: " + edad);
    }
}
```

---

## **📌 Estructuras de Control**

### **1️⃣ Condicional `if-else`**
```java
public class Condicional {
    public static void main(String[] args) {
        int edad = 20;
        
        if (edad >= 18) {
            System.out.println("Es mayor de edad.");
        } else {
            System.out.println("Es menor de edad.");
        }
    }
}
```

### **2️⃣ Ciclo `while`**
```java
public class EjemploWhile {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 5) {
            System.out.println("Iteración: " + i);
            i++;
        }
    }
}
```

### **3️⃣ Ciclo `for`**
```java
public class EjemploFor {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Número: " + i);
        }
    }
}
```

### **4️⃣ `switch-case`**
```java
import java.util.Scanner;

public class EjemploSwitch {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese un número del 1 al 3: ");
        int opcion = scanner.nextInt();

        switch (opcion) {
            case 1:
                System.out.println("Seleccionaste la opción 1.");
                break;
            case 2:
                System.out.println("Seleccionaste la opción 2.");
                break;
            case 3:
                System.out.println("Seleccionaste la opción 3.");
                break;
            default:
                System.out.println("Opción no válida.");
        }
    }
}
```


