# Gestión de Usuarios y Permisos en Linux

## ¿Qué es un usuario?

Un usuario en Linux es una cuenta que permite a una persona o proceso acceder al sistema.  
Cada usuario tiene un identificador único (UID) y permisos específicos sobre archivos y directorios.

Los usuarios permiten controlar quién puede acceder al sistema y qué acciones puede realizar.

---

## ¿Qué es un grupo?

Un grupo es un conjunto de usuarios que comparten permisos sobre ciertos archivos o directorios.

Los grupos facilitan la administración del sistema, ya que se pueden asignar permisos a varios usuarios al mismo tiempo.

Ejemplo:
- dev1 pertenece al grupo developers
- sup1 pertenece al grupo supporting

---

## ¿Cómo funciona chmod?

El comando `chmod` se utiliza para cambiar los permisos de archivos o directorios.

Ejemplo:

chmod 755 development

Esto define qué usuarios pueden leer, escribir o ejecutar un archivo o directorio.

---

## ¿Qué significa 755?

Los permisos en Linux se representan con tres números:

755 significa:

- 7 → propietario (leer, escribir y ejecutar)
- 5 → grupo (leer y ejecutar)
- 5 → otros usuarios (leer y ejecutar)

Equivale a:

rwxr-xr-x

---

## ¿Qué hace chown?

El comando `chown` se usa para cambiar el propietario de un archivo o directorio.

Ejemplo:

chown dev1:developers development

Esto asigna:
- usuario propietario: dev1
- grupo propietario: developers

---

## Creación de usuarios

Para crear usuarios se utiliza el comando:

useradd

Ejemplo:

sudo useradd dev1  
sudo useradd sup1

---

## Creación de grupos

Para crear grupos se utiliza:

groupadd

Ejemplo:

sudo groupadd developers  
sudo groupadd supporting

---

## Cambio de permisos

Los permisos se cambian con el comando chmod.

Ejemplo:

chmod 755 development  
chmod 770 support

Esto define qué usuarios pueden acceder a cada directorio.
