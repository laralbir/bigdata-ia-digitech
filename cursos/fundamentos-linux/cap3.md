# Capítulo 3: Linux en el Escritorio: Uso, Virtualización y Seguridad

## 3.1 Introducción

Antes de que te puedas convertir en un administrador eficaz de los sistemas Linux, debes saber utilizar Linux como tu escritorio y tener aptitudes con las habilidades básicas de la **Tecnología de Información y Comunicación (TIC)**. No sólo eso te ayudará al tratar con usuarios, sino que sumergiéndote en Linux te ayudará a mejorar tus habilidades más rápidamente. Además, la vida de un administrador de sistemas es más que un trabajo en el servidor: ¡hay también correo electrónico y documentación para hacer!

> **Para considerar:** ¿Cuál es la mejor posición de empleo de Linux que los Gerentes de Reclutamiento de TI están buscando?
>
> Administradores de Sistemas
>
> — Reporte Laboral de Linux 2013, Linux Foundation & Dice

## 3.2 Modo Gráfico vs. No Gráfico

Linux puede usarse de dos maneras: en **modo gráfico** y **modo no gráfico**. En modo gráfico las aplicaciones corren en ventanas que puedes redimensionar y mover. Tienes menús y herramientas que te ayudan a encontrar lo que buscas. Aquí es donde vas a usar un navegador web, tus herramientas de edición de gráficos y tu correo electrónico. Un ejemplo del escritorio gráfico incluye una barra de menús de aplicaciones populares en la izquierda y un documento de LibreOffice editado con un navegador web en el fondo.

En modo gráfico puedes tener varios shells abiertos, lo cual resulta muy útil cuando se están realizando tareas en múltiples equipos remotos. Incluso puedes iniciar la sesión con tu usuario y contraseña a través de una interfaz gráfica.

Después de iniciar la sesión pasarás al escritorio donde puedes cargar las aplicaciones. El **modo no gráfico** comienza con una sesión basada en texto: simplemente se te pedirá tu nombre de usuario y luego tu contraseña. Si el inicio de sesión tiene éxito pasarás directamente al shell.

En el modo no gráfico no hay ventanas para navegar. A pesar de esto tienes editores de texto, navegadores web y clientes de correo electrónico, pero son sólo de texto. De este modo funcionaba UNIX antes de que los entornos gráficos fueran la norma. La mayoría de los servidores también se ejecutarán en este modo, ya que la gente no entra en ellos directamente, lo que hace que una interfaz gráfica sea un desperdicio de recursos.

Durante el inicio de sesión podrías ver algunos mensajes, llamados el **mensaje del día (MOTD)**, que es una oportunidad para que el administrador de sistemas pase información a los usuarios. El MOTD precede al símbolo del sistema. En un ejemplo típico, el usuario introduce el comando `w`, que muestra quién está conectado. A medida que se introducen y procesan comandos nuevos, la ventana se desplaza hacia arriba y el texto más antiguo se pierde en la parte superior. La **terminal** es responsable de mantener el historial, tal como para permitir al usuario desplazarse hacia arriba y ver los comandos introducidos. En cuanto a Linux, lo que está en la pantalla es todo lo que hay: no hay nada para navegar.

## 3.3 Línea de Comandos

La **línea de comandos** es una entrada de texto simple que te permite ingresar cualquier cosa, desde un comando de una sola palabra hasta scripts complicados. Si inicias la sesión a través de modo de texto te encuentras inmediatamente en la consola. Si inicias la sesión de forma gráfica, entonces necesitarás iniciar un shell gráfico, que es sólo una consola de texto con una ventana a su alrededor para que puedas cambiar su tamaño y posición.

Cada escritorio de Linux es diferente, por lo que tienes que buscar en tu menú una opción llamada `terminal` o `x-term`. Ambas son shells gráficos, diferenciados sobre todo en aspecto más que en funcionalidad. Si tienes una herramienta de búsqueda como Ubuntu Dash, puedes buscar un terminal directamente.

Estas herramientas te permiten buscar rápidamente en tu sistema exactamente lo que quieres ejecutar, en lugar de perderte en los menús.

## 3.4 Virtualización y Cloud Computing

Linux es un sistema operativo **multiusuario**, lo que significa que muchos usuarios diferentes pueden trabajar en el mismo sistema al mismo tiempo y, en su mayor parte, no pueden hacer cosas para dañar a otros usuarios. Sin embargo, esto tiene limitaciones: los usuarios pueden acaparar el espacio en disco o tomar demasiada memoria o recursos de la CPU y causar que el sistema sea lento para todos. Compartir el sistema en modo multiusuario también requiere que cada uno ejecute en modo de usuario sin privilegios, por lo que permitir que cada usuario ejecute su propio servidor web es muy difícil.

La **virtualización** es un proceso donde un equipo físico, llamado **host**, ejecuta múltiples copias de un sistema operativo, cada una llamada **invitado** (guest). El host ejecuta un software llamado **hipervisor** que cambia el control entre los diferentes invitados, tal como el kernel de Linux funciona para los procesos individuales.

La virtualización funciona porque los servidores pasan la mayor parte de su tiempo inactivos y no necesitan recursos físicos tales como un monitor y un teclado. Ahora puedes tomar una potente CPU y difundirla entre varias máquinas virtuales y mantener una distribución más equitativa entre los invitados de lo que es posible en un sistema Linux puro. La principal limitación es por lo general la memoria; con los avances en la tecnología de hipervisor y la CPU es posible poner más máquinas virtuales en un host que nunca.

En un entorno virtualizado un host puede ejecutar docenas de sistemas operativos invitados, y con el apoyo de la CPU, los invitados no saben que se están ejecutando en una máquina virtual. Cada invitado obtiene su propia CPU, RAM y disco virtual, y se comunica con la red. Ni siquiera es necesario ejecutar el mismo sistema operativo en todos los invitados, lo que reduce aún más el número de servidores físicos necesarios.

La virtualización ofrece una manera para que una empresa reduzca su consumo de energía y espacio de centro de datos frente a una flota equivalente de servidores físicos. Los invitados ahora sólo son configuraciones de software, así que es fácil aprovisionar una nueva máquina para una prueba y destruirla cuando haya pasado su utilidad.

Si es posible ejecutar varias instancias de un sistema operativo en una máquina física y conectarse en la red, entonces la ubicación de la máquina no importa. El **Cloud Computing** (Cómputo o Informática en la Nube) toma este enfoque y te permite tener una máquina virtual en un centro de datos remoto que no posees, pagando sólo por los recursos que utilizas. Los proveedores de Cloud Computing pueden aprovechar economías de escala para ofrecer recursos de cómputo a mejores precios de lo que costaría adquirir tu propio hardware, espacio y enfriamiento.

Los servidores virtuales sólo son una faceta de Cloud Computing. También puedes obtener almacenamiento de archivos, bases de datos o incluso software. La clave en la mayoría de estos productos es que pagas por lo que usas —por ejemplo, una cierta cantidad por gigabyte de datos al mes— en lugar de comprar el hardware y el software para hospedarlo tú mismo. Algunas situaciones son más adecuadas para la nube que otras. Las preocupaciones de seguridad y el rendimiento son generalmente los primeros elementos que surgen, seguidos por el costo y la funcionalidad.

Linux juega un papel fundamental en el Cloud Computing. La mayoría de los servidores virtuales se basan en algún tipo de kernel de Linux, y Linux se suele utilizar para alojar las aplicaciones detrás de los servicios de Cloud Computing.

## 3.5 Utilizar Linux para el Trabajo

Las herramientas básicas utilizadas en la mayoría de las oficinas son:

- **Procesador de textos**
- **Hoja de cálculo**
- **Paquete de presentación**
- **Navegador web**

**OpenOffice**, o su variante más activa, **LibreOffice**, se encarga de las tres primeras funciones. El procesador de texto se utiliza para editar documentos, tales como informes y memos. Las hojas de cálculo son útiles para trabajar con números, por ejemplo para resumir datos de ventas y hacer predicciones futuras. El paquete de presentación se utiliza para crear diapositivas con características tales como texto, gráficos y vídeo insertado. Las diapositivas pueden ser impresas o mostradas en una pantalla o un proyector para compartir con una audiencia.

Nota cómo la hoja de cálculo, **LibreOffice Calc**, no se limita a filas y columnas de números: los números pueden ser la fuente de un gráfico, y puedes escribir fórmulas para calcular valores basados en la información, por ejemplo reunir las tasas de interés y cantidades para ayudar a comparar diferentes opciones de préstamo.

Utilizando el **Writer** de LibreOffice, un documento puede contener texto, gráficos, tablas de datos y mucho más. Puedes vincular documentos y hojas de cálculo, por ejemplo, para resumir los datos en forma escrita y saber que cualquier cambio en la hoja de cálculo se reflejará en el documento.

LibreOffice también puede trabajar con otros formatos de archivo, como Microsoft Office o **Adobe Portable Document Format (PDF)**. Además, mediante el uso de extensiones, se puede integrar LibreOffice con software Wiki para ofrecer una poderosa solución de intranet.

Linux es un ciudadano de primera clase para los navegadores Firefox y Google Chrome. Como tal, puedes esperar tener el software más reciente disponible para tu plataforma y el acceso oportuno a correcciones de errores y nuevas características. Algunos complementos, como Adobe Flash, no siempre funcionan correctamente ya que dependen de otra compañía con prioridades diferentes.

## 3.6 Proteger tu Equipo Linux

A Linux no le importa si estás en el teclado de un equipo o conectado a través de Internet, por lo que querrás tomar algunas precauciones básicas para asegurarte de que tus datos están a salvo.

Lo más fácil es utilizar una buena y única **contraseña** donde quiera que vayas, sobre todo en tu máquina local. Una buena contraseña tiene al menos 10 caracteres y contiene una mezcla de números y letras (tanto mayúsculas como minúsculas) y símbolos especiales. Utiliza un paquete como **KeePassX** para generar contraseñas, ya que luego sólo necesitas tener una contraseña de inicio de sesión a tu equipo y una contraseña para abrir el archivo de KeePassX.

Después de eso, crea periódicamente un punto de comprobación de actualizaciones. En la configuración de actualización de software de Ubuntu (disponible en el menú de Configuración), se puede ver que el sistema está configurado para buscar actualizaciones de forma diaria. Si hay actualizaciones relacionadas con la seguridad, entonces se te pedirá que las instales inmediatamente. De lo contrario, recibirás las actualizaciones en lotes cada semana. Cuando hay actualizaciones disponibles aparece un cuadro de diálogo; todo lo que tienes que hacer es hacer clic en Instalar ahora y tu equipo se actualizará.

Por último, tienes que proteger tu equipo de aceptar conexiones entrantes. Un **firewall** es un dispositivo que filtra el tráfico de red, y Linux tiene uno integrado. Si usas Ubuntu, `gufw` es una interfaz gráfica para "Uncomplicated Firewall" (`ufw`) de Ubuntu.

Simplemente cambiando el estado a "on" se bloquea todo el tráfico que llega a tu equipo, a menos que lo hayas iniciado tú mismo. De manera selectiva puedes permitir que entren algunas cosas haciendo clic en el signo más.

Bajo el capó estás usando **iptables**, que es el sistema de firewall integrado. En lugar de introducir comandos `iptables` complicados, usas una GUI. Mientras que esta GUI te permite construir una política efectiva para un escritorio, apenas araña la superficie de lo que se puede hacer con `iptables`.

## 3.7 Protegerte a tí Mismo

Cuando navegas por Internet, dejas una **huella digital**. Mucha de esta información viene ignorada, pero alguna es reunida para recopilar estadísticas de publicidad y otra puede ser utilizada para propósitos maliciosos.

Como regla general, no deberías confiar en los sitios con los que interactúas. Usa contraseñas diferentes en cada sitio de Internet para que, si tal sitio web fuera hackeado, la contraseña no pudiera utilizarse para obtener acceso a otros sitios. Usar KeePassX (mencionado anteriormente) es la forma más fácil de hacerlo. De la misma forma, limita la información que proporcionas a los sitios, sólo lo imprescindible. Mientras que dar el nombre de tu madre y fecha de nacimiento podría ayudarte a desbloquear tus credenciales de la red social en caso de que pierdas tu contraseña, la misma información puede utilizarse para suplantar la identidad de tu banco.

Las **cookies** son el mecanismo principal que los sitios web utilizan para darte seguimiento. A veces este seguimiento es bueno, por ejemplo para dar seguimiento de lo que está en tu cesta de compras o para mantenerte conectado cuando regreses al sitio.

Cuando navegas por la web, un servidor web puede devolver una cookie, que es un pequeño trozo de texto junto con la página web. Tu navegador la almacena y la envía con cada solicitud al mismo sitio. No envías cookies de `ejemplo.com` a sitios en `ejemplo.org`.

Sin embargo, muchos sitios tienen incrustados scripts que provienen de terceros, como un mensaje emergente de anuncio o un píxel de analítica. Si `ejemplo.com` y `ejemplo.org` tienen un píxel de analítica —por ejemplo, de un anunciante— entonces esa misma cookie se enviará al navegar por ambos sitios. El anunciante se entera entonces de que has visitado `ejemplo.com` y `ejemplo.org`.

Con un alcance suficientemente amplio, como los "Likes" y botones parecidos, un sitio web puede obtener un entendimiento de cuáles sitios web visitas y averiguar tus intereses y datos demográficos.

Existen diversas estrategias para tratar este asunto:

- **Ignorarlo**: no tomar ninguna medida especial frente al seguimiento.
- **Limitar los píxeles de seguimiento que aceptas**: ya sea por bloqueo completo o vaciándolos periódicamente.

En la configuración de cookies de Firefox, el usuario puede optar por que Firefox no dé permiso al sitio para el seguimiento. Esta es una etiqueta voluntaria enviada en la petición que algunos sitios distinguirán. También se puede indicar al navegador que no recuerde nunca las cookies de terceros y que elimine las cookies regulares (por ejemplo, del sitio navegado) después de haber cerrado Firefox.

Afinar la configuración de privacidad puede hacerte más anónimo en Internet, pero también puede causar problemas con algunos sitios que dependen de cookies de terceros. Si esto sucede, probablemente tengas que permitir explícitamente que se guarden algunas cookies.

También existe la posibilidad de olvidar el historial de búsqueda o no llevarlo. Con el historial de búsqueda eliminado no habrá ningún registro en el equipo local de los sitios que hayas visitado.

Si te preocupa mucho ser anónimo en Internet, puedes descargar y utilizar el **Navegador Tor**. **Tor** es el nombre corto para "The Onion Router", una red de servidores públicamente ejecutados que rebotan tu tráfico para ocultar el origen. El navegador que viene con el paquete es una versión básica que no ejecuta ni siquiera las secuencias de comandos, por lo que algunos sitios probablemente no funcionarán correctamente. Sin embargo, es la mejor manera de ocultar tu identidad si es lo que deseas hacer.

### Resumen del capítulo

- Linux puede utilizarse en **modo gráfico** (ventanas, menús, GUI) o en **modo no gráfico** (sesión basada en texto), siendo este último el habitual en los servidores por eficiencia de recursos.
- La **línea de comandos** y la terminal (física o gráfica, como `x-term`) son la puerta de entrada al shell, tanto en sesiones de texto puro como dentro de un entorno gráfico.
- La **virtualización** permite que un host ejecute múltiples sistemas operativos invitados mediante un hipervisor, optimizando el uso de hardware; esta misma idea es la base del **Cloud Computing**, donde se paga sólo por los recursos usados en centros de datos remotos, y Linux tiene un rol central en ambas tecnologías.
- Para el trabajo de oficina, Linux ofrece alternativas maduras como **LibreOffice** (procesador de texto, hoja de cálculo, presentaciones) y navegadores como Firefox y Chrome con soporte de primer nivel.
- Proteger el equipo implica usar contraseñas fuertes y únicas (idealmente con un gestor como **KeePassX**), mantener el sistema actualizado y activar un **firewall** (como `gufw`/`iptables` en Ubuntu).
- Protegerse uno mismo en línea implica gestionar cookies y el seguimiento publicitario, limitar la información personal compartida, y opcionalmente usar herramientas como el **Navegador Tor** para mayor anonimato.
