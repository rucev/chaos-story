# Chaos Story: The Reason

¿Quieres practicar los comandos de GitHub pero te preocupa cometer errores en un repositorio importante? ¡Para eso está este!

Pero incluso dentro del caos de este repositorio, habrá ciertas normas y un objetivo claro: sentirte más a gusto con Git y GitHub después de practicar un poco en un espacio seguro.

En este repositorio solo trabajaremos con texto y Markdown, y el objetivo es completar la historia que se encuentra en el archivo  [`chaos-story.md`](./chaos-story.md).

A continuación, te guiaré un poco en los pasos a seguir para participar (y practicar) en este repositorio.

## 1. Forkear el repositorio: [](#fork)

### Definición de fork
Un fork es una copia de un repositorio en el que puedes experimentar sin afectar al proyecto original. Te permite trabajar en tu propia versión del proyecto sin interferir con el repositorio principal.

### Cómo se hace
Para forkear un repositorio en GitHub, simplemente haz clic en el botón "Fork" en la esquina superior derecha de la página del repositorio y sigue las instrucciones.

![fork](/img/fork.png)

## 2. Elige tu Issue (parte de la historia): [](#issue)

### Definición de issues en GitHub
Los issues son puntos de discusión que se utilizan para realizar seguimiento de tareas, mejoras, errores u otras colaboraciones en un proyecto de GitHub. Son una forma de colaborar con otras personas en un proyecto.

### Cómo trabajar con issues
Puedes explorar los issues en la pestaña correspondiente en GitHub, elegir uno que te interese y comentar para que te lo asignen si quieres trabajar en él. Luego, sigue las instrucciones para abordar el issue y contribuir al proyecto.

![issues](/img/issues.png)

## 3. Clona el fork de tu repositorio en tu local

### Definición de clonar
Clonar un repositorio significa copiarlo a tu propia máquina local para que puedas trabajar en él.



### Cómo se hace (usando VSC)
En Visual Studio Code (VSC), abre la paleta de comandos (en windows **Ctrl + Shift + P**, en macOS **Cmd + Shift + P**), busca "Git: Clone" y proporciona la URL del repositorio que deseas clonar. Luego, selecciona una ubicación en tu sistema de archivos y espera a que se complete el proceso.
![clone](/img/clone.png)
![clone](/img/clone-2.png)
![clone](/img/clone-3.png)

## 4. En tu local crea una rama específica para el issue que has elegido

### Definición de ramas
Las ramas en Git son versiones paralelas de un repositorio que permiten trabajar en funcionalidades o correcciones de errores de manera aislada. Son útiles para organizar y realizar un seguimiento de los cambios sin afectar la rama principal del proyecto. Se utilizan mucho, especialmente en equipos grandes, para trabajas sin "pisar" el código de nadie.

La alternativa a trabajar con ramas se llama "trunk base development" (desarrollo basado en el tronco). En esta metodologia no se trabaja con ramas si no que todos los cambios van directos a 'main'. Debido a ello tiene una norma muy importante a seguir: no pushear nunca nada roto a main. Es una metodologia más frecuente en equipos con mucha experiencia y practicas de programación muy cohesionadas, limpias y estrictas.

### Cómo crearlas y publicarlas usando Git Bash
Abriendo la consola de Git Bash, utiliza el comando para crear una nueva rama y cambiar a ella:
```bash
git checkout -b nombre-de-la-rama
```
En este repo en concreto vamos a llamar las ramas por el nombre del issue, en minuscula y cambiando espacios por guiones.

![rama](/img/rama.png)

El siguiente paso es publicar la rama a tu repositorio remoto con uno de estos dos commandos, puedes hacer tus cambios en esa rama y publicarla en GitHub con uno de estos dos comandos:

1.
```bash
git push —set-upstream origin nombre-de-la-rama
```

2.
```bash
git push -u origin nombre-de-la-rama
```

## 5. Crea tu parte de la historia, commitea y pushea

### Dónde crearla y cómo para evitar conflictos
Trabaja en el apartado concreto del archivo [`chaos-story.md`](./chaos-story.md) que corresponde al issue que has seleccionado.

### Qué son los conflictos
Los conflictos ocurren cuando dos o más personas modifican el mismo archivo o línea de código al mismo tiempo. Git no puede determinar automáticamente qué cambios conservar, por lo que es necesario resolver los conflictos manualmente.

### Cómo hacer commit y push
1. **git add** para agregar los archivos modificados al área de preparación.
```bash
git add nombre-archivo-modificado
```
2. **git commit** para confirmar los cambios en tu repositorio local.
```bash
git commit -m 'acción que has hecho en infinitivo e inglés #NumeroIssueSeleccionado'
```
Un ejemplo de mensaje apropiado para el commit sería: `'add new description #6'`

3. **git push** para enviar los cambios a tu repositorio remoto en GitHub.
```bash
git push
```

¡**Recuerda** que todos los cambios no commiteados se pueden perder si cambias de rama!

**Consejo Pro:** Si te interesa cambiar de rama pero aún no estás preparado para hacer commit, puedes utilizar `git stash` para guardar temporalmente tus cambios y luego cambiar de rama con tranquilidad.
```bash
git stash
```
Una vez que vuelvas a la rama original, puedes recuperar lo último que hayas "stasheado" utilizando: 
```bash
git stash pop
```
Sin embargo, si realizas varios `git stash`, tendrás que especificar cuál quieres recuperar. Puedes ver todos los "stashes" con:
```bash
git stash list
```
Y recuperar uno específico con:
```bash
git stash pop stash@{NUMERO}
```
Además, los cambios "stasheados" no aparecen en ninguna parte al ejecutar `git status`, por lo que es una manera segura de guardar cambios temporales pero es fácil dejarse llevar. Es recomendable no acumular muchos "stashes" ya que puede volverse confuso.

## 6. Haz una pull-request con los cambios de tu repo al repositorio principal

### Qué es una pull request
Una pull request es una solicitud que haces a los colaboradores del repositorio principal para que revisen y consideren tus cambios. Es una forma de proponer tus contribuciones al proyecto y solicitar que se fusionen con la rama principal.

### Cómo se hace
En la página del repositorio en GitHub, haz clic en el botón "New pull request", selecciona la rama que contiene tus cambios y la rama a la que deseas fusionarlos, y proporciona una descripción detallada de los cambios que has realizado. Puede que sea necesario pulsar ene el link de *compare across forks*

![pull-request](/img/pull-request-1.png)
![pull-request](/img/pull-request-2.png)

A veces los proyectos tienen normas muy concretas sobre qué contenido deben tener las pull-request. En este caso vamos a trabajar solo con un par de normas muy básicas:
- Nombre de la pull request totalmente en minúscula y que sea el nombre de la rama que quieres fusionar.
- Vincula la pull request al issue con el que has estado trabajando.

El resto del contenido de la pull-request es totalmente libre.

![pull-request](/img/pull-request-3.png)

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
```bash
git switch main
```
```bash
git checkout -b nombre-del-nuevo-issue
```

2.
```bash
git checkout main
```
```bash
git checkout -b nombre-del-nuevo-issue
```


### 7.3. ¡Propón nuevos issues para que la historia siga creciendo!
Si tienes ideas para expandir la historia o mejorar el proyecto, propón nuevos issues en el repositorio. 

Para ello, ten en cuenta que deberás indicar el título que deberá tener ese apartado en el archivo [`chaos-story.md`](./chaos-story.md) y en qué ubicación (avisa entre qué otros dos segmentos se encontraría). Además, añade una checklist similar a las ya existentes en otros issues para dar una idea de cómo debería desarrollarse.

## ¡IMPORTANTE!

No es obligatorio seguir los comandos planteados en este repositorio. Si deseas probar algún comando nuevo de Git que no conozcas, puedes elegir un issue y realizar tus experimentos ahí. Sin embargo, asegúrate de dejar un comentario indicando que estás experimentando en el propio issue, y si lo deseas, comparte los resultados para que otros puedan aprender de tus pruebas.

## Ejemplo práctico: cambiar el mensaje de un commit anterior.

Somos seres humanos y es normal equivocarnos, y a veces tardamos un poco en darnos cuenta de que nos hemos equivocado. Digamos que estamos revisando nuestro log de commits (usando el comando 'git log') y nos damos cuenta de que hemos hecho un typo (o falta ortográfica), irónicamente en la palabra 'typo'... ¿Cómo podemos corregirlo?

![rebase](/img/rebase.png)

Antes de nada tenemos que acordarnos de pulsar `q` para salirnos del log. Si hubiera sido justo el commit anterior podríamos solucionarlo fácilmente con un amend, pero [a parte de esa hay otras formas](https://git-scm.com/book/es/v2/Herramientas-de-Git-Reescribiendo-la-Historia) en casos más complejos. Para este ejemplo vamos a usar el comando `git rebase`

### ¿Qué es git rebase?

[Git rebase](https://git-scm.com/docs/git-rebase) es un comando que te permite mover o combinar una serie de commits a una nueva base de commits. Dicho de una forma más simple, es una forma de reescribir la historia de commits de un repositorio.

### Usar git rebase para cambiar nuestro "tipo" por "typo"

El primer paso es localizaren el log el "hash" del commit **anterior** al que queremos modificar y hacer el comando git rebase con dicho hash. En este caso sería:

```bash
git rebase -i  a0684874c7c7e303b730cca596e09c0438dcc1b7
```

Esto nos va a abrir el editor de texto de bash, en este caso es Vim, con algo parecido a lo siguiente:

![rebase](/img/rebase-2.png)

En el texto en azul podemos ver los distintos comandos y tareas que podemos llevar a cabo en cada commit. En este caso queremos hacer "reword", que permite cambiar el mensaje del commit.

Para ello necesitamos pulsar la tecla `i` que nos permite editar el archivo. Nos movemos con las flechas de dirección hasta el "pick" previo al commit que queremos modificar y lo reemplazamos por una simple "r":

![rebase](/img/rebase-3.png)

Ahora tenemos que salir del modo edición pulsando la tecla `esc` y proceder a guardar los cambios realizados escribiendo el comando `:wq`. En caso de querer, por alguna razón, salir sin guardar el comando sería `:q!`. En ambos casos es importante no olvidarse los dos puntos. Posteriormente, le damos a `enter` y, si hemos guardado los cambios, se nos abrirá otra vez Vim. Pero esta vez nos ofrece modificar el mensaje elegido:

![rebase](/img/rebase-4.png)

El proceso es el mismo: pulsar `i`, navegar con las flechas hasta el texto que queremos modificar y cambiarlo, y luego `esc`, `:wq` y `enter`.

Si ahora hacemos git status veremos que nuestra rama local difiere de la del repositorio remoto:

![rebase](/img/rebase-5.png)



1. [Forkear el repositorio](#fork)
2. [Elige tu Issue (parte de la historia):](#issue)

Nos da la opción de hacer `git pull` para mergear nuestro rama con la remota, pero eso no nos interesa. Para saber porque solo necesitamos comprobar una vez más nuestro `git log`:

![rebase](/img/rebase-6.png)

Como podéis ver es exactamente igual al anterior solo que habiendo corregido el "typo" en el mensaje del segundo commit. Eso significa que en nuestro local hemos reescrito la historia de los commits del proyecto.

Pero si la mergeamos con el repositorio remoto, nos traeremos la historia que estamos intentando "eliminar" y la uniremos a la que hemos modificado. Teniendo la versión con faltas ortográficas primero y luego las corregidas.

Evidentemente, eso no nos interesa. Lo que queremos es reemplazar los commits del repositorio remoto con los que tenemos en nuestro local. Para ello vamos a usar un comando un tanto arriesgado:

```
git push --force origin nombre-de-la-rama
```

Con esto reemplazaremos la rama remota con nuestra rama local. Los comandos que incluyen `--force` o `-f` fuerzan un cambio eliminando versiones anteriores. En este caso nos hace falta porque es lo que nos habíamos propuesto (no dejar rastro de nuestros typos) pero es mejor asegurarse mucho antes de usar algún comando que incluya el 'force', dado que esos cambios serán, muy seguramente, irreversibles.
