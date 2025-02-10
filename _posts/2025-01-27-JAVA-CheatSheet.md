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



