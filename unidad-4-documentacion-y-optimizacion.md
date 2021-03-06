# Unidad 4: Documentación y optimización

## Introducción

En esta Unidad aprenderemos a:

* Trabajar de forma habitual con un sistema de control de versiones.  
* Identificar los patrones de refactorización más usuales.
* Revisar el código fuente usando un analizador de código.
* Documentar el código fuente.

### Herramientas básicas

### Automatización

Construir \(Build\) = Compilar + Enlazar

### Ejemplos de constructores

* C: **make**
* Java: maven, ant 

## Optimización

### Hediondez del código

* También llamado **code smell** en inglés
* Es síntoma en el código fuente que indica posiblemente un problema más profundo.
* Usualmente no son bug de programación \(errores\): no son técnicamente incorrectos y en realidad no impiden que el programa funcione correctamente. 
* Indica deficiencias en el diseño que puede ralentizar el desarrollo o aumentan el riesgo de errores o fallos en el futuro.
* Es un motivo importante para realizar refactorización.
* [Hediondez del código](https://es.wikipedia.org/wiki/Hediondez_del_código)

### Análisis de código

* Tipos:
  * Análisis estático \(**lint**\)
  * Análisis dinámico \(unit tests\)

### \(Linter\) Analizador estático

* [Introducción a los linters -en inglés-](https://github.com/mcandre/linters)

### Ejemplos de linters

* C: lint
* Java: sonar
* Javascript: JSLint, ESLint 
* Multilenguaje: SonarQube

### Refactorización

* Es el proceso de reestructurar un código fuente, alterando su estructura interna sin cambiar su comportamiento externo. 
* Técnicas:
  * Renombrado de variables
  * Pasar código duplicado a funciones
  * ...

## Documentación

* Javadoc
* Gitbook

## Control de versiones

### Sistemas más conocidos:

* CVS
* Subversion
* Mercurial
* Git

### Git

Origin: Repositorio Principal Master: Rama principal

