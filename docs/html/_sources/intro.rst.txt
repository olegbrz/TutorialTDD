Introducción
============
Este proyecto tiene como finalidad la explicación a modo de tutorial de cómo se desarrollaría un proyecto Maven con pruebas unitarias y utilizando herramientas como GIT y jUnit, con la metodología TDD. 

En este caso, se va a realizar un proyecto completo para obtener el factorial de un número entero, siguiendo los pasos necesarios para cumplir con una estrategia TDD, la cual se basa en escribir primero las pruebas que pasaría el proyecto en cuestión para comprobar que se ha efectuado de manera correcta y, más adelante, escribir el código fuente que pasaría las pruebas satisfactoriamente.


En la imagen adjunta, se puede observar de manera rápida la dinámica **Test-Driven Development (TDD)**:

.. image:: ./assets/tdd.png
	:width: 300
	:align: center
	

Se imprementarán un conjunto de Pruebas Unitarias en **Java** para el proyecto Factorial. También se hará uso de **Maven** para poder importar **jUnit** y así utilizarlo en las pruebas.

Para crear el proyecto será necesario tener instalado en el sistema:
	* Java 13 (o cualquier versión de Java superior a 8)
	* Maven (versión 3.6.3. o posterior)
	* IntelliJ IDEA como IDE, pero puede utilizarse cualquier otro.