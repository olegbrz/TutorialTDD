Desarrollo guiado por pruebas
==============================

El desarrollo guiado por pruebas o **TDD** es una metodología de desarrollo de software que consiste en escribir primero pruebas (tests unitarios) del código y después el código fuente, de forma que éste tenga que satisfacer las pruebas.

Con esta metodología se consigue un código más robusto, seguro y una mayor velocidad de desarrollo.

jUnit y Maven
--------------

jUnit es un framework open-source de automatización de pruebas unitarias para Java. jUnit permite ejecutar los métodos de las clases Java de manera controlada, evaluando en cada una el output obtenido en base al output esperado.

Para añadir jUnit al proyecto Maven, tan solo hace falta actualizar el archivo ``pom.xml`` generado por Maven.

Las dependencias de maven se pueden encontrar en `https://mvnrepository.com/ <https://mvnrepository.com/>`_. Al seleccionar una dependencia, la propia página suministra el código a añadir para Maven, y otras herramientas como Gadle, SBT, Ivy, etc...

En este caso, se va a añadir la dependencia ``org.junit.jupiter`` en la versión ``5.6.2``.

.. code-block:: xml

  <dependencies>
    <dependency>
      <groupId>org.junit.jupiter</groupId>
      <artifactId>junit-jupiter-engine</artifactId>
      <version>5.6.2</version>
      <scope>test</scope>
    </dependency>
  </dependencies>

.. note:: Se tiene que actualizar la etiqueta ``dependencies`` del ``pom.xml``, de modo que cada dependencia vaya dentro de esas llaves. No se trata de añadir este código al archivo sin más.
