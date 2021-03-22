Git
===

Los **VSC** (version control system), son herramientas que permiten realizar control de cambios y versiones de cada proyecto de forma automática y eficiente. Un VCS realiza copias incrementales de cada archivo del proyecto de forma interna, y el usuario solo tiene que preocuparse de añadir los archivos y describir los cambios.

En este tutorial se va a utilizar la herramienta más popular, llamada **Git**.

Instalación de Git
------------------

El instalador de Git se puede descargar desde `https://git-scm.com/ <https://git-scm.com/>`_.

Es muy importante que Git esté incluido en el PATH del sistema, para comprobarlo, se puede ejecutar en la línea de comandos la siguiente línea:

.. code-block:: bash

	git --version

Si la salida es la versión de Git, entonces Git está instalado y añadido a PATH, si no, deberá comprobar la instalación.

Inicialización de un repositorio local
--------------------------------------

Para inicializar un repositorio local con Git, en la linea de comandos, dentro del directorio que se quiera usar para el proyecto, deberá ejecutar:

.. code-block:: bash

	git init

La salida será algo similar a ``Initialized empty Git repository in <directorio del proyecto>``

Añadir, modificar y confirmar cambios
-------------------------------------

Para ver el estado del repositorio y los archivos en seguimiento, ejecute:

.. code-block:: bash

	git status

En la salida se mostrarán los cambios nuevos que se pueden agregar y los archivos que aún no se han agregado antes.

Para agregar un archivo/cambio:

.. code-block:: bash

	git add <nombre del archivo>

Si el archivo fue añadido por error, se puede borrar con:

.. code-block:: bash

	git rm <nombre del archivo>

Para confirmar y comentar el cambio:

.. code-block:: bash

	git commit -m "<comentario>"

Con estos comandos se realiza la mayor parte del workflow con Git. Cada commit lleva asociado un hash, un valor hexadecimal el cual sirve como identificador único para ese cambio. 

Viajes en el tiempo
-------------------

Ramas
-----

Repositorios remotos
--------------------

Git clone, pull y fetch
-----------------------
