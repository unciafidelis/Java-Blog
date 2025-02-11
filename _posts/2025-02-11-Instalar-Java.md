---

layout: post  
title: "Instalación de JAVA en VS Code"  
date: 2025-02-05  
categories: [Lenguaje, JAVA]  
tags: [estructura]  

---

# Comenzando con Java en VS Code

Este tutorial te muestra cómo escribir y ejecutar un programa "Hola Mundo" en Java con Visual Studio Code. También cubre algunas funciones avanzadas, que puedes explorar leyendo otros documentos en esta sección.

Para obtener una visión general de las funciones disponibles para Java en VS Code, consulta [Descripción general del lenguaje Java](https://code.visualstudio.com/docs/languages/java.md).

Si encuentras algún problema al seguir este tutorial, puedes contactarnos enviando un [informe de problema](https://github.com/microsoft/vscode-java-pack/issues).

## Configuración de VS Code para desarrollo en Java

### Coding Pack para Java

Para facilitar la configuración, puedes instalar el **Coding Pack para Java**, que incluye VS Code, el Java Development Kit (JDK) y las extensiones esenciales para Java. Este paquete puede utilizarse para una instalación nueva, o para actualizar o reparar un entorno de desarrollo existente.

<a class="button" onclick="pushCodingPackEvent('java', 'win')" href="https://aka.ms/vscode-java-installer-win">Instalar el Coding Pack para Java - Windows</a>

<a class="button" onclick="pushCodingPackEvent('java', 'mac')" href="https://aka.ms/vscode-java-installer-mac">Instalar el Coding Pack para Java - macOS</a><br>

> **Nota**: El Coding Pack para Java solo está disponible para Windows y macOS. Para otros sistemas operativos, deberás instalar manualmente un JDK, VS Code y las extensiones de Java.

### Instalación de extensiones

Si ya usas VS Code, puedes agregar soporte para Java instalando el [Extension Pack para Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack), que incluye las siguientes extensiones:

* [Soporte para el lenguaje Java™ por Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)
* [Depurador para Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)
* [Ejecutor de pruebas para Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-test)
* [Maven para Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-maven)
* [Administrador de proyectos para Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-dependency)
* [Visual Studio IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode)

<a class="install-extension-btn" href="vscode:extension/vscjava.vscode-java-pack">Instalar el Extension Pack para Java</a>

El [Extension Pack para Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) proporciona una guía de inicio rápido, consejos para la edición de código y depuración, además de una sección de preguntas frecuentes. Usa el comando **Java: Tips for Beginners** en la paleta de comandos (`kb(workbench.action.showCommands)`) para abrir la guía.

![Comenzando con Java](https://code.visualstudio.com/assets/docs/java/java-tutorial/getting-started.png)

También puedes instalar las extensiones por separado. La **Guía de Extensiones** está disponible para ayudarte y puedes acceder a ella con el comando **Java: Extensions Guide**.

Para este tutorial, las únicas extensiones necesarias son:

* [Soporte para el lenguaje Java™ por Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)
* [Depurador para Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)

## Instalación y configuración de un JDK (Java Development Kit)

Para usar Java en Visual Studio Code, necesitas instalar un JDK en tu entorno local. El JDK es un entorno de desarrollo de software utilizado para crear aplicaciones en Java.

### Versiones de Java compatibles

El [Extension Pack para Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) admite versiones de Java 1.8 o superiores.

> **Nota**: Para configurar los JDKs en tus proyectos, consulta [Configurar el entorno de ejecución para proyectos](https://code.visualstudio.com/docs/java/java-project.md#configure-runtime-for-projects). Para habilitar las funciones de vista previa de Java, consulta [Cómo usar VS Code con nuevas versiones de Java](/docs/java/java-faq.md#how-can-i-use-visual-studio-code-with-new-java-versions).

### Instalación de un JDK

Si nunca has instalado un JDK y necesitas hacerlo, te recomendamos elegir entre una de las siguientes opciones:

* [Amazon Corretto](https://aws.amazon.com/corretto)
* [Azul Zulu](https://www.azul.com/downloads/?package=jdk)
* [Eclipse Adoptium's Temurin](https://adoptium.net/)
* [IBM Semeru Runtimes](https://developer.ibm.com/languages/java/semeru-runtimes)
* [Microsoft Build of OpenJDK](https://www.microsoft.com/openjdk)
* [Oracle Java SE](https://www.oracle.com/java/technologies/javase-downloads.html)
* [Red Hat build of OpenJDK](https://developers.redhat.com/products/openjdk/download)
* [SapMachine](https://sapmachine.io)

## Creación de un archivo de código fuente

Crea una carpeta para tu programa en Java y ábrela con VS Code. Luego, en VS Code, crea un nuevo archivo y guárdalo con el nombre `Hello.java`. Cuando abras el archivo, el servidor de lenguaje Java se iniciará automáticamente y verás un ícono de carga en la barra de estado. Una vez finalizada la carga, puedes pasar el cursor sobre el ícono para confirmar que el proceso ha finalizado correctamente.

<video src="https://code.visualstudio.com/assets/docs/java/java-tutorial/JavaHelloWorld.Standalone.mp4" autoplay="" loop="" muted="" playsinline="" controls="" title="Creating a source code file">
</video>

> **Nota**: Si abres un archivo Java en VS Code sin abrir su carpeta, el servidor de lenguaje Java podría no funcionar correctamente.

VS Code también intentará determinar el paquete correcto para el nuevo archivo y completarlo desde una plantilla. Consulta [Crear un nuevo archivo](https://code.visualstudio.com/docs/java/java-editing.md#create-new-file).

También puedes crear un proyecto en Java usando el comando **Java: Create Java Project** desde la paleta de comandos (`kb(workbench.action.showCommands)`). Luego de seleccionar el comando, se te pedirá la ubicación y el nombre del proyecto. También puedes elegir tu herramienta de construcción desde este comando.

<video src="https://code.visualstudio.com/assets/docs/java/java-tutorial/JavaHelloWorld.Project.mp4" autoplay="" loop="" muted="" playsinline="" controls="" title="Create Java Project">
</video>

Visual Studio Code también admite proyectos Java más complejos. Consulta [Gestión de proyectos](https://code.visualstudio.com/docs/java/java-project.md).

## Edición de código fuente

Puedes usar fragmentos de código para estructurar clases y métodos rápidamente. VS Code también ofrece IntelliSense para autocompletar código y diversas opciones de refactorización.

<video src="https://code.visualstudio.com/assets/docs/java/java-tutorial/edit-code.mp4" autoplay loop muted playsinline controls title="Edición de código fuente">
</video>

Para más detalles sobre la edición de código en Java, consulta [Edición en Java](https://code.visualstudio.com/docs/java/java-editing.md).

## Ejecución y depuración del programa

Para ejecutar y depurar código en Java, coloca un punto de interrupción y presiona `kb(workbench.action.debug.start)`, o usa la opción **Ejecutar > Iniciar depuración**. También puedes usar la opción **Ejecutar/Depurar** en el editor. Una vez compilado el código, verás todas tus variables e hilos en la vista **Ejecutar y Depurar**.

<video src="https://code.visualstudio.com/assets/docs/java/java-tutorial/run-debug.mp4" autoplay loop muted playsinline controls title="Ejecución y depuración del programa">
</video>

El depurador también admite funciones avanzadas como [Hot Code Replace](https://code.visualstudio.com/docs/java/java-debugging.md#hot-code-replace) y puntos de interrupción condicionales.

Para más información, consulta [Depuración en Java](https://code.visualstudio.com/docs/java/java-debugging.md).

## Más funciones

El editor ofrece muchas más capacidades para facilitar el desarrollo en Java, incluyendo edición avanzada, depuración, pruebas, gestión de proyectos y soporte para frameworks como Spring Boot.
