# Curso Profesional de Git y GitHub

## Crear un repositorio
Le indicaremos a Git que queremos crear un nuevo repositorio para utilizar su sistema de control de versiones. Solo debemos posicionarnos en la carpeta raíz de nuestro proyecto y ejecutar el comando ``git init``.

### Configura tu usuario y email
``git config --global user.email "tu@email.com"
git config --global user.name "Tu Nombre"``

### Realizar commit
``git add``: nos ayuda a mover archivos del Untracked o Unstaged al estado Staged.

``git commit``: nos ayuda a mover archivos de Unstaged a Tracked. Esta es una ocasión especial, los archivos han sido guardados o actualizados en el repositorio. Git nos pedirá que dejemos un mensaje para recordar los cambios que hicimos y podemos usar el argumento -m para escribirlo (``git commit -m "mensaje"``).

### Checkout
El comando git checkout + ID del commit nos permite viajar en el tiempo. Podemos volver a cualquier versión anterior de un archivo específico o incluso del proyecto entero. Esta también es la forma de crear ramas y movernos entre ellas.

``git branch rama, git checkout -b rama``
``git checkout rama-o-id-commit``

### GitHub repositorio remoto
Estos servidores remotos pueden estar alojados en GitHub, GitLab, BitBucket, entre otros. Lo que van a hacer es guardar el mismo repositorio que tienes en tu computadora y darnos una URL con la que todos podremos acceder a los archivos del proyecto para descargarlos, hacer cambios y volverlos a enviar al servidor remoto para que otras personas vean los cambios, comparen sus versiones y creen nuevas propuestas para el proyecto.

**Comandos:**
- **git clone url_del_servidor_remoto:** Nos permite descargar los archivos de la última versión de la rama principal y todo el historial de cambios en la carpeta .git.

- **git push**: Luego de hacer git add y git commit debemos ejecutar este comando para mandar los cambios al servidor remoto.

- **git fetch:** Lo usamos para traer actualizaciones del servidor remoto y guardarlas en nuestro repositorio local (en caso de que hayan, por supuesto).

- **git merge:** También usamos el comando git merge con servidores remotos. Lo necesitamos para combinar los últimos cambios del servidor remoto y nuestro directorio de trabajo.

- **git pull:** Básicamente, git fetch y git merge al mismo tiempo.

### Branch
Las ramas son la forma de hacer cambios en nuestro proyecto sin afectar el flujo de trabajo de la rama principal. Esto porque queremos trabajar una parte muy específica de la aplicación o simplemente experimentar.

git branch rama, ``git checkout -b rama`` o movernos en el tiempo a cualquier otro commit de cualquier otra rama con los comandos (``git reset id-commit``, `git checkout rama-o-id-commit`).

### Merge
El comando ``git merge`` nos permite crear un nuevo commit con la combinación de dos ramas (la rama donde nos encontramos cuando ejecutamos el comando y la rama que indiquemos después del comando).

``git checkout master``
``git merge cabecera``

* Crear un nuevo commit en la rama cabecera combinando los cambios de cualquier otra rama:
``git checkout cabecera``
``git merge cualquier-otra-rama``

### Tags
Los tags o etiquetas nos permiten asignar versiones a los commits con cambios más importantes o significativos de nuestro proyecto.

Comandos para trabajar con etiquetas:
- **Crear un nuevo tag y asignarlo a un commit:** ``git tag -a nombre-del-tag id-del-commit``.

- **Borrar un tag en el repositorio local:** ``git tag -d nombre-del-tag``.

- **Listar los tags de nuestro repositorio local:** ``git tag o git show-ref --tags``.

- **Publicar un tag en el repositorio remoto:** ``git push origin --tags``.
- **Borrar un tag del repositorio remoto:** ``git tag -d nombre-del-tag`` y ``git push origin :refs/tags/nombre-del-tag``.

### Pull Request
Es una funcionalidad de github (en gitlab llamada merge request y en bitbucket push request), en la que un colaborador pide que revisen sus cambios antes de hacer merge a una rama, normalmente master.

Al hacer un pull request se genera una conversación que pueden seguir los demás usuarios del repositorio, así como autorizar y rechazar los cambios

### Fork
Es una característica única de GitHub en la que se crea una copia exacta del estado actual de un repositorio directamente en GitHub, éste repositorio podrá servir como otro origen y se podrá clonar (como cualquier otro repositorio), en pocas palabras, lo podremos utilizar como un git cualquiera

### Amend
A veces hacemos un commit, pero resulta que no queríamos mandarlo porque faltaba algo más. Utilizamos ``git commit --amend``, amend en inglés es remendar y lo que hará es que los cambios que hicimos nos los agregará al commit anterior.

### Git reset
Con git reset HashDelHEAD nos devolveremos al estado en que el proyecto funcionaba.

- **``git reset --soft HashDelHEAD``** te mantiene lo que tengas en staging ahí.

- **``git reset --hard HashDelHEAD``** resetea absolutamente todo incluyendo lo que tengas en staging.

# Actividad del curso
## hyperblog
Un blog increible para el curso de Git y Github



