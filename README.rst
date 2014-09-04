.. contents::

==============
Linux Commands
==============

---------------
DISK AND MEMORY
---------------

Espacio libre en discos/particiones
===================================
::

	df -h

Espacio libre en memoria
========================
::

	free -h

Unidades Discos
===============
::

	fdisk -l

---------------
FILES
---------------

Backup ficheros
===============

::

	rsync -avPzhe [ORIGEN] [DESTINO]

En el caso de que sea una copia remota: 'ssh -p 1050'

Para excluir un conjunto de directorios --exclude-from '/home/nombre_usuario/fichero' donde este contiene un listado de directorios o ficheros que no se incluirán de forma recurrenbte

::

	rsync -avPzhe 'ssh -p 1050' --progress --exclude-from '/home/nombre_usuario/fichero' /home/nombre_usuario/www

Enlace simbólico
================
::

	ln -s /var/www/OLIF_SYSTEM_V2_0/ /var/www/..../olif

---------------
USERS
---------------

Cambiar contraseña
==================
::

	sudo passwd [USER]

---------------
SAMBA
---------------

Crear / cambiar password usuario
==================
::

	sudo smbpasswd -a pepe
