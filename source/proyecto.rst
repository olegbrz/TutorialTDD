Creación del proyecto Maven
============================

¿Qué es un proyecto Maven y para qué sirve?
-------------------------------------------------

**Maven** es una herramienta open-source para la gestión y construcción de proyectos Java basado en un formato XML. Se creó con el objetivo de simplificar procesos  de build (para compilar y generar ejecutables a partir de código fuente).

Para ello, en Maven se definen tres ciclos de build del software con una serie de etapas diferenciadas. Por defecto tiene las siguientes etapas:

    - **Validación**: Validar que el proyecto es correcto.
    - **Compilación**.
    - **Test**: Probar el código utilizando pruebas unitarias.
    - **Empaquetar** el código compilado y transformarlo en algún formato, por ejemplo .jar.
    - **Pruebas de integración**: Procesar y desplegar el código en algún entorno.
    - **Verificar** que el código es válido y cumple con los criterios de calidad.
    - **Instalar** el código en el repositorio locar para poder usarlos como dependencias de otros proyecots.
    - **Desplegar** el código a un entorno.


¿Cómo crear un proyecto Maven en IntelliJ IDEA?
-------------------------------------------------

Al haber elegido IntelliJ IDEA, habría que seguir unos pasos para crear correctamente el proyecto.

#. Abrir el entorno y crear un nuevo proyecto.
#. Seleccionar *Create form archetype* y, luego, *org.apache.maven.archetypes:maven-archetype-quickstar*, como se indica en la imagen siguiente.
    .. image:: ./assets/CrearProyecto1.png
        :width: 500
        :align: center

#. Se le asigna el nombre al proyecto, en este caso será *FactorialTDD*.
    .. image:: ./assets/CrearProyecto2.png
        :width: 500
        :align: center

#. Se seleccionaría *Next* y, en la siguiente ventana, *Finish*.
    .. image:: ./assets/CrearProyecto3.png
        :width: 500
        :align: center

#. Una vez creado el proyecto, se obtendrá la estructura definida junto con el archivo *pom.xml*, en el que se encuentran las dependencias necesarias para **Maven**. 
    .. image:: ./assets/CrearProyecto4.png
        :width: 500
        :align: center

Estructura final de la carpeta src del proyecto
-------------------------------------------------

* main
  * java
    * org.FactorialTDD
        * Factorial
* test
  * java
    * org.FactorialTDD
        * FactorialTest
