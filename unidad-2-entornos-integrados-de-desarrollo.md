# Unidad 2: Entornos integrados de desarrollo

## Introducción

En esta Unidad aprenderemos a:

* Instalar entornos de desarrollo, propietarios y libres.
* Personalizar y automatizar el entorno de desarrollo.
* Generar ejecutables a partir de código fuente.
* Identificar las características comunes y específicas de diversos entornos de desarrollo.

### Conceptos

* Codigo fuente. EL texto  legible en un lenguaje de programacion.
* Codigo intermedio u objeto. Es un codigo binario pero no se puede ejecutar
* Codigo binario. Es un codigo ejecutable \(codigo final\).
* Bibliotecas \(librerías\). Son archivos, que se pueden distribuir con codigo fuentes y codigo objetos.
* Compilar. Es el proceso de coger el codigo fuente y traducirlo a codigo objeto
* Enlazar \(Link\).Es coger varios archivos obejetos y juntarlos todos y crear un archivo ejecutable.
* Interpretar.Lee el codigo fuente y lo traduce a codigo binario y se ejecuta en el momento. No se interpreta binario.

## Herramientas básicas

### Lo básico

* Editor de texto: permite escribir código fuente
* Compilador: genera código objeto a partir del código fuente
* Enlazador: agrupa varios archivos objeto en uno binario
* Interprete: lee código fuente y genera código binario para su ejecución

### Bibliotecas \(o librerías\) \(I\)

> Conjunto de archivos objeto que extienden la funcionalidad del lenguaje

* **Biblioteca estándar** del lenguaje. Suele venir con el lenguaje
* **Bibliotecas adicionales** 

### Bibliotecas \(o librerías\) \(II\)

* **Biblioteca estándar del lenguaje C**
  * Entrada y salida por terminal
  * Manejo de archivos
  * Funciones matemáticas
* **Biblioteca estándar del lenguaje Java**
  * Entrada y salida por terminal
  * Manejo de archivos
  * Funciones matemáticas
  * Interfaz gráfica 
  * Red
  * Bases de datos
  * Gráficos \(sólo 2D\)

### Bibliotecas \(o librerías\) \(III\)

* Cada biblioteca está compuesta por varios archivos objeto
* Tipos
  * bibliotecas dinámicas \(.DLL o .so\) \(.jar en Java\)
    * muy usadas
  * bibliotecas estática \(.LIB o .a\)
    * menos usadas actualmente

### Bibliotecas \(o librerías\) \(IV\)

* Una biblioteca se compone de 2 partes:
  * Especificación \(ofrece una API\) Es la declaración de los metodos, el código en este caso no nos interesa.                                       

    Son las clases y los métodos que podemos utlizar.

  * Implementación: Para modificarlo

**API** = Interfaz de Programación de Aplicaciones

### Entorno necesario en java

* JRE: necesario para ejecutar programas
  * JVM \(inteprete java\)
  * Biblioteca estándar
* JDK: necesario para desarrollar programas
  * Herramientas: javac, jar, javadoc, ... Para compilar, empaquetar.

### Construir \(Build\) \(I\)

> Construir \(Build\) = Compilar + Enlazar. Genera un ejecutable

* Dos opciones:
  * Herramientas de construcción
  * Servidor de construcción

### Construir \(Build\) \(II\)

Equipo local

#### **Herramientas de construcción**

* make, ninja \(C, C++\)
* ant, maven, gradle \(Java\)
* grunt, gulp \(Javascript\)
* rake \(ruby\)

### Construir \(Build\) \(III\)

#### **Archivos de construcción \(buildfiles\)**

Cada sistema necesita un archivo de construcción.

* make: **Makefile**
* ninja: **build.ninja**
* ant: **build.xml**
* maven: **pom.xml**
* gradle: **build.gradle**
* grunt: **Gruntfile.js**
* gulp: **gulpfile.js**
* rake: **Rakefile**

### Construir \(Build\) \(IV\)

* Generadores de archivos de construcción
  * CMake: CMakeLists.txt Podemos generar archivos como los anteriores.
  * Meson: meson.build  

### Construir \(Build\) \(V\)

Integración continua \(CI\)

* Servidores de construcción
  * Jenkins 
  * TravisCI
  * CircleCI
  * Bamboo
  * TeamCity

## Entornos integrados de desarrollo \(IDE\)

### Ejemplos

* Destinados principalmente a C++:
  * DevC++
  * Microsoft Visual Studio
  * QtCreator
* Destinados principalmente a Java:
  * Netbeans
  * Eclipse
  * IntelJ IDEA
  * Oracle JDeveloper

