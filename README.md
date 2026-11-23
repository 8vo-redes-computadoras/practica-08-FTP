# FTP (File Transfer Protocol)

## ¿Qué es FTP?

FTP (*File Transfer Protocol* o Protocolo de Transferencia de Archivos) es
un protocolo de red que permite enviar y recibir archivos entre un
equipo y un servidor a través de una red.

En lugar de copiar archivos manualmente en un dispositivo de
almacenamiento, un cliente FTP se conecta a un servidor y transfiere los
archivos directamente por la red.

## ¿Para qué sirve?

FTP facilita el intercambio de archivos entre equipos, especialmente
cuando son grandes o cuando varias personas necesitan acceder a los mismos
datos. Se utiliza para publicar páginas web, respaldar información y
compartir documentos en entornos domésticos, escolares y empresariales.

Entre sus principales funciones se encuentran:

-   Subir archivos desde un equipo hacia un servidor.
-   Descargar archivos desde un servidor a un equipo.
-   Navegar por las carpetas del servidor.
-   Crear, renombrar y eliminar archivos y carpetas, según los permisos
    del usuario.

## Elementos que intervienen en FTP

-   **Servidor FTP:** equipo o servicio que almacena los archivos y
    responde a las solicitudes de los clientes.
-   **Cliente FTP:** programa desde donde se conecta al servidor, como
    FileZilla o el explorador de archivos de algunos sistemas.
-   **Credenciales:** usuario y contraseña que permiten el acceso al
    servidor. En algunos casos se permite el acceso anónimo.
-   **Permisos:** reglas que definen qué carpetas y archivos puede ver,
    subir, modificar o eliminar cada usuario.

## ¿Cómo funciona FTP?

La comunicación FTP se realiza en dos partes:

1.  **Conexión de control:** el cliente se conecta al servidor, se
    autentica y envía las órdenes, como listar carpetas o pedir un
    archivo.
2.  **Conexión de datos:** por este canal viajan los archivos y los
    listados de carpetas. Se abre cada vez que hace falta transferir
    información.

De esta forma, las órdenes y los archivos se envían por separado, lo que
permite controlar la transferencia sin interrumpir la conexión principal.

## Modos de conexión

FTP puede trabajar en dos modos para abrir el canal de datos:

-   **Modo activo:** es el servidor quien inicia la conexión de datos
    hacia el cliente.
-   **Modo pasivo:** es el cliente quien inicia la conexión de datos
    hacia el servidor. Es el más utilizado actualmente, porque funciona
    mejor detrás de firewalls y routers.

## Puertos utilizados

FTP utiliza el protocolo de transporte TCP:

| Puerto | Uso |
| :--- | :--- |
| **21** | Conexión de control: autenticación y envío de órdenes. |
| **20** | Conexión de datos en modo activo. |
| **Rango alto variable** | Conexión de datos en modo pasivo, definido por el servidor. |

## Ventajas de FTP

-   **Sencillez:** es un protocolo fácil de usar y compatible con muchos
    programas.
-   **Eficiencia:** transfiere archivos grandes de forma rápida y estable.
-   **Control de acceso:** permite asignar permisos a cada usuario.
-   **Automatización:** puede utilizarse en scripts para copias de
    seguridad y tareas programadas.

## Consideraciones de seguridad

FTP tradicional envía el usuario, la contraseña y los archivos sin cifrar.
Cualquier persona que observe la red podría obtener esa información. Para
reducir estos riesgos se utilizan alternativas como:

-   **FTPS:** FTP con cifrado mediante TLS/SSL.
-   **SFTP:** transferencia de archivos mediante SSH, que cifra toda la
    comunicación. Es la opción más recomendada actualmente.
-   **Contraseñas seguras y permisos limitados:** cada usuario debe tener
    solo los accesos que necesita.

## Relación entre FTP y otros servicios de red

FTP y otros servicios cumplen funciones diferentes:

-   **FTP** transfiere archivos entre un cliente y un servidor.
-   **SMTP** envía correos electrónicos, que pueden incluir archivos
    adjuntos.
-   **DNS** permite localizar el servidor FTP mediante un nombre de
    dominio, como `ftp.ejemplo.com`.

FTP no sustituye a los servicios de almacenamiento en la nube ni a los
sistemas de copias de seguridad, aunque puede formar parte de ellos.

## Conclusión

FTP es un protocolo fundamental para transferir archivos entre equipos a
través de la red. Su modelo de control y datos permite gestionar
transferencias de forma ordenada y es un recurso habitual para publicar
sitios web y compartir información. Para su uso actual conviene elegir
versiones cifradas, como FTPS o SFTP, que protegen la información
transmitida.
