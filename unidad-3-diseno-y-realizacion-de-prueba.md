# Unidad 3: Diseño y realización de prueba

### Entornos de desarrollo

![Entornos de desarrollo](https://github.com/daniatenciano/Apuntes_ED/tree/5ef90b395da362a45f5a29f1d8b19747c3595878/assets/entornosdesarrollo.png)  2017-18 - IES Luis Vélez de Guevara - Écija - Spain

### Diseño y realización de pruebas

![cc-by-sa](https://github.com/daniatenciano/Apuntes_ED/tree/5ef90b395da362a45f5a29f1d8b19747c3595878/assets/cc-by-sa.png)

### Índice

#### Introducción

#### Pruebas

#### Integración

#### Calidad

### Introducción

En esta Unidad aprenderemos a:

* Identificar los diferentes tipos de pruebas.
* Definir casos de prueba.
* Efectuar pruebas unitarias de clases y funciones.
* Efectuar pruebas de integración, de sistema y de aceptación.
* Realizar medidas de calidad sobre el software desarrollado.

#### Objetivos de las pruebas

* Una buena prueba debe centrarse en dos objetivos:
  1. probar si el software no hace lo que debe hacer
  2. probar si el software hace lo que no debe hacer.
* Existen distintos **frameworks** para la realización de pruebas.

#### Framework

* En general, un framework \(marco de trabajo\) está compuesto por:
  * un conjunto de las mejores prácticas y suposiciones
  * herramientas comunes
  * bibliotecas 
* Permite unificar el proceso de desarrollo entre desarrolladores.

### Pruebas

#### Forma de las pruebas

* **Pruebas dinámicas:** Requieren la ejecución de la aplicación. Permiten medir el comportamiento de la aplicación desarrollada.
* **Pruebas estáticas:** Se realizan sin ejecutar el código de la aplicación. Se examina el código fuente.

#### Estrategias de prueba

* **Caja negra:** Se estudia el sistema desde fuera. Son pruebas funcionales.
* **Caja blanca:** Se examina el código fuente y su ejecución. Son pruebas estructurales.

#### Estrategias de prueba

![Caja blanca vs Caja negra](https://github.com/daniatenciano/Apuntes_ED/tree/5ef90b395da362a45f5a29f1d8b19747c3595878/img/caja_blanca-caja_negra.png)

#### Estrategias de prueba de caja negra

* Se estudia el sistema desde fuera.
* Se trabaja sobre la interfaz.
* No se tienen en cuenta los detalles internos de funcionamiento.
* Se proporcionan entradas y se estudian las salidas.
* Principales técnicas:
  * Particiones de equivalencia
  * Valores límite

#### Estrategias de prueba de caja blanca

* Se examina el código fuente y su ejecución.
* Se comprueban los flujos de ejecución dentro de cada unidad \(función, clase, módulo, etc.\) 
* También pueden comprobarse los flujos entre unidades durante la integración.
* E incluso entre subsistemas, durante las pruebas de sistema.
* Principales técnicas:
  * Cobertura lógica
  * Prueba de bucles

#### Tipos de pruebas

* **Funcionales:** Evaluan el cumplimiento de los requisitos.
* **No funcionales:** Evaluan aspectos adicionales como rendimiento, seguridad, ...

#### Pruebas funcionales

* Pruebas unitarias \(o de unidad\)
* Pruebas de regresión
* Pruebas de integración 
* Pruebas del sistema
* Pruebas de humo \(smoke test\)
* Pruebas alfa y beta
* Pruebas de aceptación \(validación por parte del cliente\)

#### Pruebas no funcionales

* Pruebas de usabilidad
* Pruebas de rendimiento
* Pruebas de stress
* Pruebas de seguridad
* Pruebas de compatibilidad
* Pruebas de portabilidad
* ...

#### Mecanismos de prueba

* Manual
  * Mediante pruebas realizadas por personal de la empresa o externo.
* Automático
  * Mediante software que ejecuta código de forma automatizada y compara los resultados obtenidos y los resultados esperados.

#### Soporte del depurador

* Puntos de ruptura
* Ejecución paso a paso
* Análisis de variables

#### Automatización de pruebas

* Frameworks de pruebas \(xUnit\)
* Aserciones

[https://en.wikipedia.org/wiki/XUnit](https://en.wikipedia.org/wiki/XUnit)

#### Frameworks para pruebas

* Java: JUnit, TestNG
* C++: CppUnit, Google Test
* PHP: PHPUnit
* Javascript: Mocha

[https://en.wikipedia.org/wiki/List\_of\_unit\_testing\_frameworks](https://en.wikipedia.org/wiki/List_of_unit_testing_frameworks)

#### Caso de prueba

* precondición --&gt; postcondición
* Una entrada conocida  --&gt; Una salida esperada 

[http://www.jtech.ua.es/j2ee/publico/lja-2012-13/sesion04-apuntes.html](http://www.jtech.ua.es/j2ee/publico/lja-2012-13/sesion04-apuntes.html)

#### JUnit4/5 - Anotaciones

* @BeforeClass / @BeforeAll
* @Before / @BeforeEach
* @Test
* @After / @AfterEach
* @AfterClass / @AfterAll
* @Ignore  Se desactiva 

#### JUnit - Aserciones

```java
import org.junit.Test;
import static org.junit.Assert.*;

// ... 
fail()                         // el test termina con fallo
assertTrue(expresión)          // expresión es true ?
assertFalse(expresión)         // expresión es false ?
assertEquals(esperado,real)    // esperado es igual a real ?
assertNotEquals(esperado,real) // esperado es distinto de real ?
assertNull(objeto)             // objeto es null ?
assertNotNull(objeto)          // objeto es distinto de null ?

// objeto_esperado es igual a objeto_real ?
assertSame(objeto_esperado,objeto_real)
// objeto_esperado es distinto de objeto_real ?
assertNotSame(objeto_esperado,objeto_real)
```

[http://junit.org/junit4/javadoc/4.12/org/junit/Assert.html](http://junit.org/junit4/javadoc/4.12/org/junit/Assert.html)

#### TDD

* Desarrollo guiado por pruebas de software, o Test-Driven Development \(TDD\) 
  * Escribir las pruebas primero \(Test First Development\).
  * Refactorización \(Refactoring\).

### Integración

#### Formas de integración

* Integración Big bang
* Integración Descendente
* Integración Ascendente
* Integración Continua \(CI\)

#### Servidores de integración continua

> CI : Integración continua  
> CD : Despliegue continuo

* Jenkins
* Bamboo
* TravisCI
* CircleCI

Note: CI=Continuous Integration / CD=Continuous Delivery.

## Calidad

### Control de calidad

Control de calidad = medición de la calidad de un producto --&gt; Pruebas

### Calidad del proceso/producto \(QA/QC\)

* QA es un conjunto de actividades para garantizar la **calidad en los procesos** mediante los cuales se desarrollan los productos. 
* QC es un conjunto de actividades para garantizar **la calidad de los productos**. Las actividades se centran en identificar defectos en los productos reales producidos.

Note: QA = Quality Assurance / QC = Quality Control

### Factores de calidad

* Corrección
* Fiabilidad
* Eficiencia
* Seguridad
* Facilidad de uso
* Mantenibilidad
* Flexibilidad
* Facilidad de prueba
* Transportabilidad
* Reusabilidad
* Interoperatividad

