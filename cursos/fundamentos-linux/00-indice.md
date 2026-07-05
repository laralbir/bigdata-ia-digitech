# Fundamentos de Linux — Cisco Networking Academy

## Resumen del curso

Este curso ofrece una introducción completa al sistema operativo Linux, pensada tanto para el uso de escritorio como para la administración de sistemas. Parte del origen del kernel y de las distribuciones más populares, pasa por el uso cotidiano de la línea de comandos y el shell Bash, la gestión de archivos, la búsqueda y el filtrado de texto, y los conceptos básicos de scripting. La segunda mitad del curso se adentra en la administración de sistemas propiamente dicha: hardware y dispositivos, administración de paquetes y procesos, redes, y la gestión completa de usuarios, grupos, propiedad y permisos —incluyendo los permisos especiales y el Estándar de Jerarquía del Sistema de Archivos (FHS)—.

En conjunto, el temario cubre los objetivos típicos de las certificaciones **LPI Linux Essentials** y sienta las bases para certificaciones de nivel superior como **LPIC-1** o **CompTIA Linux+**.

## Índice de capítulos

| # | Capítulo | Contenido principal |
|---|----------|----------------------|
| 1 | [Introducción a Linux y los Sistemas Operativos](cap1.md) | Origen del kernel, código abierto, GNU, principales distribuciones (Red Hat, Debian, Ubuntu…) y criterios para elegir un sistema operativo. |
| 2 | [Aplicaciones de Código Abierto y Licenciamiento de Software](cap2.md) | Software de servidor, escritorio, consola y desarrollo; y los esquemas de licenciamiento FOSS (GPL/LGPL, BSD/MIT, Creative Commons) y sus modelos de negocio. |
| 3 | [Linux en el Escritorio: Uso, Virtualización y Seguridad](cap3.md) | Modo gráfico vs. no gráfico, virtualización y Cloud Computing, ofimática con LibreOffice, y seguridad básica del equipo y la privacidad. |
| 4 | [La Interfaz de Línea de Comandos (CLI) y el Shell Bash](cap4.md) | La terminal, el prompt, historial de comandos, variables de entorno (`PATH`), alias, comodines (globbing), comillas e instrucciones de control. |
| 5 | [Obtener Ayuda en Linux: man, info y otras fuentes](cap5.md) | Páginas `man`, el sistema `info`, `--help`, y herramientas de búsqueda de comandos y documentación (`whatis`, `apropos`, `whereis`, `locate`). |
| 6 | [Gestión de Archivos y Directorios](cap6.md) | Estructura de directorios, rutas absolutas/relativas, `pwd`, `cd`, `ls`, y operaciones de copiar, mover, crear y eliminar archivos y directorios. |
| 7 | [Compresión y Empaquetado de Archivos](cap7.md) | Compresión con `gzip`/`bzip2`, empaquetado con `tar`, y archivos ZIP (`zip`/`unzip`). |
| 8 | [Procesamiento y Filtrado de Texto en la Línea de Comandos](cap8.md) | Tuberías (pipes), redirección de E/S, `find`, `less`, `head`/`tail`, `sort`, `wc`, `cut`, `grep`, expresiones regulares básicas y extendidas, y `xargs`. |
| 9 | [Introducción a los Shell Scripts](cap9.md) | Qué es un script, el shebang, edición con `nano`, variables, condicionales (`if`/`case`) y bucles (`for`/`while`). |
| 10 | [Hardware y Dispositivos](cap10.md) | Procesadores, tarjetas madre y buses (PCI, USB), RAM y swap, dispositivos de disco (MBR/GPT), discos ópticos, video y fuentes de poder. |
| 11 | [Administración de Paquetes y Procesos](cap11.md) | Gestión de paquetes Debian (`dpkg`/`apt-get`) y RPM (`rpm`/`yum`), el kernel y `/proc`/`/sys`, monitoreo con `ps`/`top`/`free` y logs del sistema. |
| 12 | [Fundamentos de Redes](cap12.md) | Terminología de redes, direcciones IPv4/IPv6, NAT, configuración de interfaces de red y herramientas de diagnóstico (`ping`, `netstat`, `dig`, `ssh`…). |
| 13 | [Cuentas de Usuario y Grupos](cap13.md) | Los archivos `/etc/passwd`, `/etc/shadow` y `/etc/group`, cuentas de sistema vs. regulares, y `su`, `sudo`, `who`, `w`. |
| 14 | [Gestión de Usuarios y Grupos](cap14.md) | Creación y administración de grupos y usuarios (`groupadd`, `useradd`, `usermod`, `userdel`, `chage`) y buenas prácticas de contraseñas. |
| 15 | [Propiedad y Permisos de Archivos](cap15.md) | Propiedad de usuario/grupo (`chown`, `chgrp`), el sistema de permisos `rwx` con `chmod` (simbólico y octal), y `umask`. |
| 16 | [Permisos Especiales y el Estándar de Jerarquía del Sistema de Archivos](cap16.md) | `setuid`, `setgid`, sticky bit, enlaces físicos y simbólicos, y el FHS (`/bin`, `/etc`, `/var`, `/usr`…). |

## Cómo usar este material

Cada capítulo enlazado arriba es un documento Markdown independiente y autocontenido, enriquecido a partir de las transcripciones originales del curso: conserva toda la información técnica, ejemplos de terminal y explicaciones originales, con mejoras de formato (encabezados, negritas en términos clave, bloques de código, tablas) y un resumen final de puntos clave por capítulo. Todo el contenido está disponible también en un único PDF (`Fundamentos-de-Linux-Curso-Completo.pdf`) que reúne este índice y los 15 capítulos en un solo documento para lectura o impresión.

## Historial de versiones

| Versión | Fecha | Cambios |
|---------|-------|---------|
| 1.1 | 2026-07-05 | Corregida la alineación del calendario ASCII (2014) del capítulo 1. |
| 1.0 | 2026-07-05 | Versión inicial: índice, 16 capítulos, diagramas SVG y compilación en PDF/EPUB. |
