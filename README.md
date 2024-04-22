# Chaos Story

¿Quieres practicar los comandos de GitHub pero te preocupa cometer errores en un repositorio importante? ¡Para eso está este!

Pero incluso dentro del caos de este repositorio, habrá ciertas normas y un objetivo claro: sentirte más a gusto con Git y GitHub después de practicar un poco en un espacio seguro.

En este repositorio solo trabajaremos con texto y Markdown, y el objetivo es completar la historia que se encuentra en el archivo  [`chaos-story.md`](./chaos-story.md).

A continuación, te guiaré un poco en los pasos a seguir para participar (y practicar) en este repositorio.

# 1. Forkear el repositorio:

### Definición de fork
Un fork es una copia de un repositorio en el que puedes experimentar sin afectar al proyecto original. Te permite trabajar en tu propia versión del proyecto sin interferir con el repositorio principal.

### Cómo se hace
Para forkear un repositorio en GitHub, simplemente haz clic en el botón "Fork" en la esquina superior derecha de la página del repositorio.

## 2. Elige tu Issue (parte de la historia):

### Definición de issues en GitHub
Los issues son puntos de discusión que se utilizan para realizar seguimiento de tareas, mejoras, errores u otras colaboraciones en un proyecto de GitHub. Son una forma de colaborar con otras personas en un proyecto.

### Cómo trabajar con issues
Puedes explorar los issues en la pestaña correspondiente en GitHub, elegir uno que te interese y asignártelo si quieres trabajar en él. Luego, sigue las instrucciones para abordar el issue y contribuir al proyecto.

## 3. Clona el fork de tu repositorio en tu local

### Definición de clonar
Clonar un repositorio significa copiarlo a tu propia máquina local para que puedas trabajar en él.

### Cómo se hace (usando VSC)
En Visual Studio Code (VSC), abre la paleta de comandos (en windows **Ctrl + Shift + P**, en macOS **Cmd + Shift + P**), busca "Git: Clone" y proporciona la URL del repositorio que deseas clonar. Luego, selecciona una ubicación en tu sistema de archivos y espera a que se complete el proceso.

## 4. En tu local crea una rama específica para el issue que has elegido

### Definición de ramas
Las ramas en Git son versiones paralelas de un repositorio que permiten trabajar en funcionalidades o correcciones de errores de manera aislada. Son útiles para organizar y realizar un seguimiento de los cambios sin afectar la rama principal del proyecto. Se utilizan mucho, especialmente en equipos grandes, para trabajas sin "pisar" el código de nadie.

La alternativa a trabajar con ramas se llama "trunk base development" (desarrollo basado en el tronco). En esta metodologia no se trabaja con ramas si no que todos los cambios van directos a 'main'. Debido a ello tiene una norma muy importante a seguir: no pushear nunca nada roto a main. Es una metodologia más frecuente en equipos con mucha experiencia y practicas de programación muy cohesionadas, limpias y estrictas.

### Cómo crearlas y publicarlas usando Git Bash
Abriendo la consola de Git Bash, utiliza el comando para crear una nueva rama y cambiar a ella:
```sh
git checkout -b nombre-de-la-rama
```
En este repo en concreto vamos a llamar las ramas por el nombre del issue, en minuscula y cambiando espacios por guiones.

El siguiente paso es publicar la rama a tu repositorio remoto con uno de estos dos commandos, puedes hacer tus cambios en esa rama y publicarla en GitHub con uno de estos dos comandos:

1.
```sh
git push —set-upstream origin nombre-de-la-rama
```

2.
```sh
git push -u origin nombre-de-la-rama
```

## 5. Crea tu parte de la historia, commitea y pushea

### Dónde crearla y cómo para evitar conflictos
Trabaja en el apartado concreto del archivo [`chaos-story.md`](./chaos-story.md) que corresponde al issue que has seleccionado.

### Qué son los conflictos
Los conflictos ocurren cuando dos o más personas modifican el mismo archivo o línea de código al mismo tiempo. Git no puede determinar automáticamente qué cambios conservar, por lo que es necesario resolver los conflictos manualmente.

### Cómo hacer commit y push
1. **git add** para agregar los archivos modificados al área de preparación.
```sh
git add nombre-archivo-modificado
```
2. **git commit** para confirmar los cambios en tu repositorio local.
```sh
git commit -m 'acción que has hecho en infinitivo e inglés #NumeroIssueSeleccionado'
```
Un ejemplo de mensaje apropiado para el commit sería: `'add new description #6'`

3. **git push** para enviar los cambios a tu repositorio remoto en GitHub.
```sh
git push
```

¡**Recuerda** que todos los cambios no commiteados se pueden perder si cambias de rama!

**Consejo Pro:** Si te interesa cambiar de rama pero aún no estás preparado para hacer commit, puedes utilizar `git stash` para guardar temporalmente tus cambios y luego cambiar de rama con tranquilidad.
```sh
git stash
```
Una vez que vuelvas a la rama original, puedes recuperar lo último que hayas "stasheado" utilizando: 
```sh
git stash pop
```
Sin embargo, si realizas varios `git stash`, tendrás que especificar cuál quieres recuperar. Puedes ver todos los "stashes" con:
```sh
git stash list
```
Y recuperar uno específico con:
```sh
git stash pop stash@{NUMERO}
```
Además, los cambios "stasheados" no aparecen en ninguna parte al ejecutar `git status`, por lo que es una manera segura de guardar cambios temporales pero es fácil dejarse llevar. Es recomendable no acumular muchos "stashes" ya que puede volverse confuso.

## 6. Haz una pull-request con los cambios de tu repo al repositorio principal

### Qué es una pull request
Una pull request es una solicitud que haces a los colaboradores del repositorio principal para que revisen y consideren tus cambios. Es una forma de proponer tus contribuciones al proyecto y solicitar que se fusionen con la rama principal.

### Cómo se hace
En la página de tu repositorio en GitHub, haz clic en el botón "New pull request", selecciona la rama que contiene tus cambios y la rama a la que deseas fusionarlos, y proporciona una descripción detallada de los cambios que has realizado.

A veces los proyectos tienen normas muy concretas sobre qué contenido deben tener las pull-request. En este caso vamos a trabajar solo con un par de normas muy básicas:
- Nombre de la pull request totalmente en minúscula y que sea el nombre de la rama que quieres fusionar.
- Vincula la pull request al issue con el que has estado trabajando.

El resto del contenido de la pull-request es totalmente libre.

## 7. Y otras cosas que puedes hacer

### 7.1. Revisa las pull request o los issues en los que está trabajando otra gente

#### Cómo
Visita la sección de pull requests o issues en GitHub y revisa las contribuciones de otros colaboradores. Puedes comentar, hacer preguntas o sugerir mejoras.

#### Por qué
Revisar el trabajo de otros te permite aprender de diferentes enfoques, ofrecer feedback constructivo y colaborar en la mejora del proyecto en general.

### 7.2. Elige un nuevo issue y sigue practicando
Explora los issues abiertos en el repositorio y elige uno que te interese para trabajar en él. ¡Continúa practicando tus habilidades con Git y GitHub mientras contribuyes a este caos de historia!

Si haces eso asegurate de, desde tu local, volver a main y crear una rama nueva con el nombre del siguiente issue elegido de una de las siguientes maneras:

1. 
```sh
git switch main
```
```sh
git checkout -b nombre-del-nuevo-issue
```

2.
```sh
git checkout main
```
```sh
git checkout -b nombre-del-nuevo-issue
```


### 7.3. ¡Propón nuevos issues para que la historia siga creciendo!
Si tienes ideas para expandir la historia o mejorar el proyecto, propón nuevos issues en el repositorio. 

Para ello, ten en cuenta que deberás indicar el título que deberá tener ese apartado en el archivo [`chaos-story.md`](./chaos-story.md) y en qué ubicación (avisa entre qué otros dos segmentos se encontraría). Además, añade una checklist similar a las ya existentes en otros issues para dar una idea de cómo debería desarrollarse.

## ¡IMPORTANTE!

No es obligatorio seguir los comandos planteados en este repositorio. Si deseas probar algún comando nuevo de Git que no conozcas, puedes elegir un issue y realizar tus experimentos ahí. Sin embargo, asegúrate de dejar un comentario indicando que estás experimentando en el propio issue, y si lo deseas, comparte los resultados para que otros puedan aprender de tus pruebas.