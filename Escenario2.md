# ¡Bienvenido!
* Escenario 2 - Cometer cambios

 Dificultad: principiante
 Tiempo estimado: 10 minutos

Sobre la base del escenario anterior, aquí aprenderá cómo ver los cambios en su directorio de trabajo y confirmarlos en su repositorio. Este entorno tiene un repositorio Git con un archivo confirmado. En el directorio de trabajo existe un cambio en el archivo confirmado y un archivo no confirmado.

En futuros escenarios, cubriremos cómo puede deshacer cambios y compartir compromisos con otras personas.

**Paso 1 - Estado Git**

Como se discutió en el escenario anterior, el estado de git nos permite ver los cambios en el directorio de trabajo y el área de preparación en comparación con el repositorio.

Dado el repositorio actual, el estado de git muestra que se ha realizado un cambio en nuestro directorio de trabajo a un archivo previamente confirmado, commit.js, pero aún no se ha movido al área de preparación.

>git status

## Paso 2 - Git Diff

El comando git diff le permite comparar los cambios en el directorio de trabajo con una versión previamente confirmada. Por defecto, el comando compara el directorio de trabajo y la confirmación HEAD.

Si desea comparar con una versión anterior, proporcione el hash de confirmación como parámetro, por ejemplo, git diff <commit>. La comparación con las confirmaciones generará los cambios para todos los archivos modificados. Si desea comparar los cambios con un solo archivo, proporcione el nombre como un argumento como git diff commit.js.

**Protip**

Por defecto, la salida está en el formato diff combinado. El comando git difftool cargará una herramienta externa de su elección para ver las diferencias.

>git diff

## Paso 3 - Git Añadir

Al igual que en el escenario anterior, para confirmar un cambio, primero se debe configurar utilizando el comando git add.

**Tarea**

Para proceder a la primera etapa tus cambios usando git add.

**Protip**

Si cambia el nombre o elimina archivos, deberá especificar estos archivos en el comando Agregar para que se puedan rastrear. Alternativas puede usar git mv y git rm para que git realice la acción e incluya la actualización del área de preparación.

>git add . 

## Paso 4 - Diferencias por etapas

Una vez que los cambios están en el área de preparación, no se mostrarán en la salida de git diff. Por defecto, git diff solo comparará el directorio de trabajo y no el área de preparación.

Para comparar los cambios en el área de preparación con la confirmación anterior, debe proporcionar el parámetro de configuración git diff --staged. Esto le permite asegurarse de que ha configurado correctamente todos sus cambios.

>git diff
>
>git diff --staged

## Paso 5 - Registro Git

El comando git log le permite ver el historial del repositorio y el registro de confirmación.

**Protip**

El formato de la salida del registro es muy flexible. Por ejemplo, para generar cada confirmación en una sola línea, el comando es git log --pretty = format: "% h% a% ar -% s". Se pueden encontrar más detalles en la página de manual de git log a la que se accede utilizando git log --help

>git log

## Paso 6 - Git Show

Mientras que git log le indica el autor y el mensaje de confirmación, para ver los cambios realizados en la confirmación, debe usar el comando git show

Al igual que con otros comandos, por defecto mostrará los cambios en la confirmación HEAD. Use git show <commit-hash> para ver los cambios más antiguos.

>git show
	
