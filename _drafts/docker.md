---
title: How to Docker (on Windows)
date: 2019-10-06 00:00:00 -06:00
---

Durante años he trabajado con Windows. Siempre me ha gustado y nunca he entendido por qué tantos desarrolladores aman Linux.

Hasta que comencé a usar Linux.

Por eso cuando comencé a involucrarme en el tema de Docker, lo hice con Linux. Excepto que en mi equipo tengo instalado Windows.

Como había leído que el dual boot puede llegar ser problemático, mi única opción era el Windows Subsystem for Linux (WSL).

Así que instalé Docker. En Linux. Con Windows.

Y luego escribí un post al respecto.

## Qué es Docker

La verdad es que ya bastantes personas se han dedicado a explicar qué es Docker. Tan sólo googlea _tutorial docker_ y verás el montón de resultados que te aparece.

No es sorpresa, claro, pues esta herramienta ha existido desde el 2013. Suficiente tiempo para que todos se pusieran a usarla y explicarla.

Entonces, en breve:

> Docker es una plataforma que te permite ejecutar aplicaciones dentro de contenedores.

Al decir plataforma, me refiero a que en realidad son varias herramientas que, en conjunto, se encargan de hacer lo explicado arriba: contenedor-izar aplicaciones (en inglés es un poco más amigable la palabra: *containerize* __containerize__).

Es decir que los programas se encapsulan junto con sus dependencias, con número de versiones y toda la cosa, para luego ser ejecutadas dentro de estas "cápsulas" (los contenedores) sobre un sistema operativo.

Si esto te hace pensar en una máquina virtual, es porque de hecho se parecen entre sí. La principal diferencia, sin embargo, es que Docker no necesita montar un sistema operativo virtualizado sobre aquél del equipo en el que se está ejecutando.

Por el contrario, el sistema operativo en el que se aloja Docker es compartido por todos sus contenedores. Así se eliminan muchos problemas de consumo de recursos, una de las principales ventajas de Docker.

![La misma imagen que todos usan](https://docs.docker.com/images/Container%402x.png)

![La misma imagen que todos usan](https://docs.docker.com/images/VM%402x.png)

Bueno, con eso basta por ahora para poder continuar. Si deseas conocer más detalles, te recomiendo visitar [uno de mis tutoriales preferidos](https://djangostars.com/blog/what-is-docker-and-how-to-use-it-with-python/) sobre el tema.

## Cómo instalar Docker

Existen dos opciones: Linux y Windows.

Si lo tuyo es Linux, felicidades. El asunto es tan sencillo como seguir las indicaciones oficiales ([aquí las de Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)), y con eso basta. Tienes un Docker recién salido del horno, listo para usar.

Pero por supuesto que el procedimiento se complica un poco, sólo un poco, ligeramente, cuando se trata de Windows. Y gracias a eso tuve un tema para escribir este post.

En Windows se puede correr Docker de dos maneras. Con [Docker Desktop](https://hub.docker.com/editions/community/docker-ce-desktop-windows) o con [Docker Toolbox](https://docs.docker.com/toolbox/overview/).

Se dice en la documentación oficial que el segundo método es para sistemas "más antiguos" que no cumplen los requisitos del nuevo Docker Desktop.

Pues resulta que el principal requisito de éste es tener Windows 10 Enterprise, ya que en la versión Home no se encuentra habilitado el uso de Hyper-V (una cosa súper moderna, así bien pro que Windows 10 ---Enterprise--- incluye para mejorar la virtualización).

Por lo tanto, nos toca continuar con Docker Toolbox. Una vez que hayas completado la instalación, puedes usar Docker directamente a través de Windows.

O si te gusta la adrenalina y prefieres continuar con el WSL, como fue mi caso, puedes también instalarlo desde una shell de tu distro preferida. Sólo inicia una sesión de WSL y sigue las instrucciones de instalación de Linux para tu distro.

En resumen:

```bash
# Instalación en Windows

# Instalación en Ubuntu WSL
```

Falla OpenSSH.

Y sólo en caso de que aún no tengas WSL habilitado, chécate [esta página](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

## Cómo echarlo a andar

La instalación es tan sólo el primer paso. Aún falta mover algunas perillas y picar algunos botones antes de poder correr Docker en el WSL.

Los pasos son como sigue:

```bash
# 1. Create docker machine: shared folders with VM (/code, /data)
# 2. Mount volumes on WSL (/code, /data)
# 3. Eval env always https://docs.docker.com/machine/reference/env/
# 4. Export docker cert as wsl path (add to ~/.bashrc)
# 5. docker run hello-world
# 6. Change mount /mnt/c to /c
```

![Diagrama de mounts Windows > VM > Docker]()


## Cómo convertí a Docker en computadora

[Get started](https://docs.docker.com/get-started/)

Jekyll

Python

Jupyter


## Los sabios

- []()
- []()
- []()
- []()
- []()
