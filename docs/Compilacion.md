# COMPILACIÓN
DE UN PAQUETE EN C USANDO MAKEFILE

# Introducción

Elige el programa escrito en C que
prefieras y comprueba en las fuentes que exista un fichero Makefile o
Configure. Deberás compilar desde las fuentes.

Realiza los
pasos necesarios para compilarlo e instálalo en tu equipo en un
directorio que no interfiera con tu sistema de paquetes (/opt,
/usr/local, etc.)

La corrección se hará en clase y deberás
ser capaz de explicar qué son todos los ficheros que se hayan
instalado y realizar una desinstalación limpia.

# Pre-requisitos

En primer lugar instalaremos los paquetes
necesarios para la compilación del kernel. Estos son
build-essential, make y gcc.

```
 sudo apt install build-essential make gcc
```

Con build-essential no tendremos que instalar los demás paquetes ya
que se incluyen durante la instalación, pero para asegurarnos los
instalaremos.

- **build****essential** → Es un paquete
que contiene una serie de paquetes necesarios para la compilacion de
paquetes.
- **make** → Este comando buscará un archivo
llamado "Makefile" en el directorio actual y ejecutará el
objetivo predeterminado especificado en ese archivo.
- **gcc** → Es un conjunto de compiladores
para varios lenguajes de programación, incluyendo C, C++, y Fortran.

# Proceso
a seguir

En mi caso estaré usando el paquete tree. Para
descargarlo haremos un

```
sudo apt source tree
```

Podemos comprobar el contenido del paquete comprobado

Nos moveremos al directorio tree

En este directorio tendremos el contenido del
paquete, aquí encontramos el fichero **Makefile**. En otros casos
es necesario ejecutar el script **configure**. El propósito
principal del script configure es simplificar la configuración del
software para adaptarse al entorno específico del sistema en el que
se va a compilar e instalar el programa. En caso de que lo tuviésemos
ejecutaremos un

```
sudo ./configure
```

Esto ejecutará el script y nos generará el
Makefile, en este caso no es necesario ya que nos encontramos
directamente con el Makefile.

Lo que haremos ahora será ejecutar el comando
**make** para que se lancen las órdenes del makefile

Antes de eso podemos hacer un

```
sudo apt build-dep tree
```

Para descargar las dependencias del paquete,
posteriormente lanzaremos el Makefile.

Este proceso puede tardar mas o menos dependiendo
del paquete con el que estemos trabajando y de nuestro equipo.

Si el proceso de compilación ha sido exitoso, se
nos habrá creado el binario **tree** en el directorio

Podemos comprobar que funciona ejecutándolo.

Ahora podremos instalar el paquete haciendo un

sudo make install

Podemos comprobar que se encuentra instalado

El manual podremos encontrarlo en:

Si quisiéramos eliminarlo haremos un:

```
sudo make uninstall
```