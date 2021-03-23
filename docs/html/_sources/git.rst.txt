Sistemas de control de versiones: Git
======================================

Los **VSC** (version control system), son herramientas que permiten realizar control de cambios y versiones de cada proyecto de forma automática y eficiente. Un VCS realiza copias incrementales de cada archivo del proyecto de forma interna, y el usuario solo tiene que preocuparse de añadir los archivos y describir los cambios.

En este tutorial se va a utilizar la herramienta más popular, llamada **Git**. Git sirve para evitar casos como estos:

.. image:: /assets/memes.webp
	:width: 300
	:align: center

Instalación de Git
-------------------

El instalador de Git se puede descargar desde `https://git-scm.com/ <https://git-scm.com/>`_.

.. warning:: Es muy importante que Git esté incluido en el PATH del sistema.

Para comprobar si git está en el PATH, se puede ejecutar en la línea de comandos la siguiente línea:

.. code-block:: bash

	git --version

Si la salida es la versión de Git, entonces Git está instalado y añadido a PATH, de lo contrario, deberá comprobar la instalación.

Inicialización de un repositorio local
---------------------------------------

Para inicializar un repositorio local con Git, en la linea de comandos, dentro del directorio que se quiera usar para el proyecto, deberá ejecutar:

.. code-block:: bash

	git init

La salida será algo similar a ``Initialized empty Git repository in <directorio del proyecto>``

Añadir, modificar y confirmar cambios
--------------------------------------

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

Para volver atrás en los cambios, se necesita el **hash** del commit al que se quiere volver. Para visualizar el log de los commits y sus respectivos hashes y comentarios:

.. code-block:: bash

	git log

Teniendo el hash, para volver a ese commit:

.. code-block:: bash

	git reset --hard <hash del commit>

Ramas
-----

La utilidad de las ramas es la de hacer una bifurcación del código del proyecto, creando dos caminos paralelos en los cuales se desarrolla el código de forma independiente. Las ramas se utilizan principalmente para introducir nuevas funcionalidades en el proyecto, y de esta forma, mantener la rama principal "limpia". 

.. image:: ./assets/branches.png


Cuando se termina el desarrollo de la funcionalidad deseada y se quiere incluir esos cambios en la rama principal, las ramas se **fusionan**.

Para crear una rama: 

.. code-block:: bash

	git branch <nombre rama>

Para cambiar a una rama:

.. code-block:: bash

	git checkout <nombre rama>

.. tip:: Como atajo, los dos últimos comandos se pueden acortar con:

	.. code-block:: bash

		git checkout -b <nombre rama>

	Este comando crea una rama y se cambia.

Para borrar una rama no deseada:

.. code-block:: bash

	git branch -d <nombre rama>

Para fusionar dos ramas, estando en la rama **master** o **main**:

.. code-block:: bash

	git merge <nombre rama>

.. warning:: Si el mismo archivo se ha modificado en dos ramas, al fusionarlas, pueden crearse conflictos, los cuales necesitan solución manual.

	.. image:: /assets/memes2.jpg
		:width: 200
		:align: center


Repositorios remotos
---------------------

Como se puede observar, los repositorios de Git son muy útiles a la hora de desarrollar un proyecto software serio. El problema de lo que se ha explicado hasta ahora es que toda la información se guarda de manera local, de este modo, si se pierde el acceso al dispositivo en el que se está desarrollando, se pierde todo el proyecto. Otro problema surge si se tiene que trabajar en equipo sobre un mismo repositorio. Para solventar estos problemas, Git soporta repositorios remotos. El proyecto se guarda en un servidor de una plataforma. Allí el proyecto está mucho más seguro que solo en local y ya pueden acceder a él todas las personas que tengan una conexión a Internet. 

Una de estas plataformas es `GitHub <https://github.com/>`_, aunque hay muchas más como `GitLab <https://about.gitlab.com/>`_ o `Bitbucket <https://bitbucket.org/>`_.

Para subir un proyecto git a un repositorio remoto, primero se debe crear el repositorio en la plataforma, el cual estará asociado a un link .git. Para añadir el repositorio remoto al proyecto:

.. code-block:: bash

	git remote add origin <link .git del repositorio>

Al tener el repositorio remoto enlazado, lo siguiente es hacer realizar un **push**. El primer push debe especificar la rama del repositorio remoto a la que se va a subir, el comando es el siguiente:

.. code-block:: bash

	git push --set-upstream origin <nombre rama>

Los siguientes push se pueden realizar sin los argumentos.

Git clone, pull y fetch
------------------------

Ahora, ¿qué pasa si hace falta descargar un repositorio remoto existente para trabajar en él? Para esto, se necesita el antes mencionado link .git del repositorio. Para descargarlo en un directorio, se utiliza:

.. code-block:: bash

	git clone <link .git>

De esta forma el proyecto se descargará con todo el historial de cambios, como si se hubiese creado en la máquina.

Si varias personas trabajan con el mismo repositorio remoto, hará falta sincronizar los cambios que hacen los demás antes. Para sincronizar:

.. code-block:: bash

	git pull

Este listado de comandos es el set básico para poder trabajar con Git, el siguiente paso es... ¡crear el proyecto!
