# ¡Bienvenido!

- Escenario 1 - Comprometer archivos
  Dificultad: principiante
  Tiempo estimado: 10 minutos

En este escenario, aprenderá cómo inicializar un nuevo repositorio Git y enviar archivos al control de versiones.

El control de versiones le permite grabar cambios en un archivo o conjunto de archivos a lo largo del tiempo, lo que le permite volver a una versión específica si es necesario. Git es un sistema de control de versiones distribuido. Esto significa que, en lugar de tener una instantánea de los últimos archivos, tiene un espejo completo del repositorio en su máquina local. El repositorio realiza un seguimiento de los cambios, cuándo se produjeron y quién los realizó. Tener el repositorio completo en su máquina local reduce los retrasos debidos al tráfico de la red y le permite continuar trabajando cuando está desconectado.

Este entorno de Scrapbook ha sido preconfigurado con git instalado. Para obtener más información sobre la instalación de Git, consulte la documentación oficial.


## Paso 1 - Git Init

Para almacenar un directorio bajo el control de versiones necesita crear un repositorio. Con Git inicializa un repositorio en el directorio de nivel superior para un proyecto.

**Tarea**  

Como este es un nuevo proyecto, se necesita crear un nuevo repositorio. Utilice el comando git init para crear un repositorio.

**ProTip**

Después de inicializar un repositorio, se crea un nuevo subdirectorio oculto llamado .git. Este subdirectorio contiene los metadatos que Git utiliza para almacenar su información. Si está interesado en los detalles, use la línea de comandos para explorar los contenidos.

>git init

## Paso 2 - Estado Git

Cuando un directorio forma parte de un repositorio, se denomina Directorio de trabajo. Un directorio de trabajo contiene la última versión descargada del repositorio junto con cualquier cambio que aún no se haya confirmado. Mientras trabaja en un proyecto, todos los cambios se realizan en este directorio de trabajo

Puede ver qué archivos han cambiado entre su directorio de trabajo y lo que se ha confirmado previamente en el repositorio con el comando git status.

La salida de este comando se denomina "estado del árbol de trabajo".
 
 **Protip**

Todos los archivos están "sin seguimiento" por Git hasta que se indique lo contrario. Los detalles de cómo se trata en el siguiente paso.

>git status

## Paso 3 - Git Añadir

Para guardar o confirmar archivos en su repositorio Git, primero debe agregarlos al área de preparación. Git tiene tres áreas, un directorio de trabajo, un área de preparación y el propio repositorio. Los usuarios mueven, de otro modo se denomina promoción, los cambios del directorio de trabajo a un área de preparación antes de enviarlos al repositorio.

Uno de los enfoques clave con Git es que los compromisos son enfocados, pequeños y frecuentes. El área de preparación ayuda a mantener este flujo de trabajo permitiéndole solo promover ciertos archivos a la vez en lugar de todos los cambios en su directorio de trabajo.

**Tarea**

Use el comando git add <file | directory> para agregar hello-world.js al área de preparación.

Si realiza un cambio adicional después de agregar un archivo al área de preparación, el cambio no se reflejará hasta que vuelva a agregar el archivo.

**Protip**

Como se describe en el Paso 2, el comando git status le permite ver el estado del directorio de trabajo y del área de preparación en cualquier momento.

>git add *
>
>git status

## Paso 4 - Git Commit

Una vez que se ha agregado un archivo al área de preparación, debe comprometerse en el repositorio. El comando git commit -m "commit message" mueve los archivos desde el almacenamiento intermedio al repositorio y registra la hora / fecha, el autor y un mensaje de confirmación que se puede usar para agregar un contexto y un razonamiento adicionales a los cambios, como un número de informe de error.

Solo se confirmarán los cambios agregados al área de preparación, no se incluirán los archivos en el directorio de trabajo que no hayan sido almacenados.

**Tarea**

Use git commit -m "<commit message>" para confirmar el archivo preconfigurado.

**Protip**

A cada confirmación se le asigna un hash SHA-1 que le permite consultar la confirmación en otros comandos.

>git commit -m "Primer Commit"

## Paso 5 - Git Ignorar

A veces hay archivos o directorios particulares que nunca desea confirmar, como la configuración de desarrollo local. Para ignorar estos archivos, cree un archivo .gitignore en la raíz del repositorio.

El archivo .gitignore le permite definir comodines para los archivos que desea ignorar, por ejemplo * .tmp ignorará todos los archivos con la extensión .tmp.

Cualquier archivo que coincida con un comodín definido no se mostrará en una salida de estado de git y se ignorará cuando se intente con el comando git add.

**Tarea**

Agregue y confirme un archivo .gitignore en el repositorio para ignorar todos los archivos * .tmp.

**Protip**

El .gitignore debe estar comprometido con el repositorio para garantizar que las reglas se apliquen en diferentes máquinas.

>**nano .gitignore**
>
>*detro del archivo de texto*
>
>***.tmp**



