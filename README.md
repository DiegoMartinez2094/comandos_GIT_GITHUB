# GIT

Es un sistema de control de versiones.

Instalacion de GIT:

[https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git ]()

---

## comandos básicos de la terminal de comandos:

`Ctrl+L`  limpia la terminal

`pwd`: Imprimir la ruta del directorio actual

`rmdir`: Eliminar un directorio vacío

`ls ` Muestra los archivos que contenga la carpeta en la que estamos situados

`cd ` direccionarnos solo a carpetas

`cd .. ` direcciona a una carpeta exterior

`cat archivo.txt ` abrir un archivo en la terminal

`New-Item -Path /home/usuario/archivo.txt  ` creará un archivo con el nombre `archivo.txt` en el directorio `/home/usuario`:

`New-Item archivo.txt ` crea un archivo.txt en la pasición actual

`New-Item -Path archivo.txt -Type File -Value "hola"` crea un archivo.txt con un hola dentro

`New-Item  archivo2.txt -Value "hola2" `   forma abreviada

`echo "hola" >> archivo.txt ` y si ya estaba previamente creado el archivo .txt vacio y quiere agg texto

`Set-Content -Path archivo.txt -Value "hola adios"` para editar el contenido de este archivo.txt

`rm`: Eliminar un archivo

`mv`: Mover un archivo o directorio

`cp`: Copiar un archivo o directorio

` mkdir carpeta`  creará una carpeta con el nombre `carpeta` en el directorio actual:

## Comandos de Git

`git clone <url>`  => Clona un repositorio remoto

`git push origin ` => Envía los cambios al repositorio remoto,en la rama que se especifica. Esto solo envía los cambios que han sido confirmados.

---

Establecer el nombre de usuario de Git en `Juan Pérez`, escribirías el siguiente comando:

```
git config user.name "Juan Pérez"
```

**Para establecer la dirección de correo electrónico de Git:**

```
git config user.email "juan.perez@example.com"
```

---

Para inicializar un proyecto con git, se debe abrir la terminal en la carpeta que queremos hacer el control de versiones de archivos seguido utilizamos el comando:

`git init`

El comando git init se utiliza para inicializar un nuevo repositorio de Git. Esto significa crear una estructura de directorios y archivos que Git necesita para rastrear los cambios en los archivos.

Si deseas inicializar un repositorio con un nombre diferente, puedes pasar el nombre del repositorio como argumento al comando git init:

`git init my-repository`

---

`git status`

El comando git status se utiliza para mostrar el estado del directorio de trabajo y del área **de ensayo. Permite ver los cambios que se han preparado, los que no y los archivos en los que Git no va a realizar el seguimiento.**

**El comando git** status muestra una serie de indicadores para cada archivo en el directorio de trabajo:

* **A:** El archivo ha sido modificado, pero no ha sido agregado al área de ensayo.
* **M:** El archivo ha sido modificado y agregado al área de ensayo.
* **?:** El archivo no está siendo rastreado por Git.
* **U:** El archivo ha sido modificado desde la última confirmación, pero no ha sido modificado desde la última vez que se agregó al área de ensayo.
* **D:** El archivo ha sido eliminado del directorio de trabajo, pero aún está siendo rastreado por Git.

El comando git status también muestra una serie de mensajes de estado:

* **Untracked files:** Lista los archivos que no están siendo rastreados por Git.
* **Changes to be committed:** Lista los archivos que han sido modificados y agregados al área de ensayo.
* **Changes not staged for commit:** Lista los archivos que han sido modificados, pero no han sido agregados al área de ensayo.

---

`git add <nombre del archivocon su .tipoDeArchivo>` ejemplo `git add app.js`

El comando git add se utiliza para mover los cambios del directorio de trabajo al área de ensayo. Esto significa que los cambios se prepararán para ser confirmados en el historial de Git.

```
# Agregar todos los archivos modificados
git add .

# Agregar un archivo específico
git add archivo.txt

# Agregar un directorio específico
git add directorio
```

* **`git reset <nombre-archivo>`:** El comando `git reset` para sacar un archivo del `git add .`
* `git diff `para mostrar los cambios del archivo entre dos commits,
  ejemplo : `git diff 2154542187455df458df54d5 a5s4d5sf8sdf5sdf45sdfd `
* **`git commit`:** El comando `git commit` crea una instantánea de los cambios en el área de preparación. El mensaje del commit describe los cambios realizados. Para crear un commit con un mensaje, puedes utilizar el siguiente comando:

```
git commit -m "Mensaje del commit"
```

* **`git log`:** El comando `git log` muestra el historial de cambios del repositorio. El historial incluye la fecha y hora del cambio, el autor del cambio, el mensaje del cambio y los archivos afectados.
* **`git checkout`:** El comando `git checkout` cambia a una rama específica. Las ramas son una forma de organizar los cambios en el repositorio.
* **`git merge`:** El comando `git merge` fusiona dos ramas. Las fusiones se utilizan para combinar los cambios de dos ramas en una sola rama.

  `git merge rama_origen -m "Mensaje de commit"`
* **`git push`:** El comando `git push` publica los cambios en un repositorio remoto. Los repositorios remotos son repositorios de Git que se almacenan en un servidor.
* `git checkout -- .` nos redirige la informacion al último commit que hicimos

---

-Para crear una rama en Git, utiliza el comando `git branch`. La sintaxis básica es la siguiente:

```
git branch nombre-de-la-rama
```

---

-Por ejemplo, para crear una rama llamada `nueva-rama` a partir de la confirmación con el hash `1234567890`, escribirías el siguiente comando:

```
git branch nueva-rama 1234567890
```

---

-Eliminar una rama en Git, utiliza el comando `git branch -d`. La sintaxis básica es la siguiente:

```
git branch -d nombre-de-la-rama
```

Este comando eliminará la rama `nombre-de-la-rama` si está fusionada con la rama actual. Si la rama no está fusionada, Git te avisará y tendrás que fusionarla manualmente antes de poder eliminarla.

---

-También puedes utilizar el comando `git branch -D` para eliminar una rama sin importar si está fusionada o no. La sintaxis es la siguiente:

```
git branch -D nombre-de-la-rama
```

---

-Cambiar de rama  `git checkout`. La sintaxis básica es la siguiente:

```
git checkout nombre-de-la-rama
```

---

-para fusionar una rama con la rama principal, debes estar en la rama principal git merge nombre de la rama

`git merge nueva-rama`

---

## Como eliminar un commit:

git log = para enlistar los commits,

git reset --hard 2506cd65ebb0e85387350ae392dbef626e06964c  = elimina los commits que se hicieron DESPUÉS de ese solo localmente(en mi pc)(tambien puede cambiar el hard por soft, mixed)

git push origin -f = envia los cambios al repositorio remoto,

si es a una rama especifica rama  (prueba):  git push origin prueba -f

---

## Viajar entre commits:

para viajar entre commits

`git log` para ver todos los commits con su respectivo **hash ** o número amarillo

![1700147262760](image/README/1700147262760.png)

podemos ver que hay dos commits el más reciente siempre es el de arriba, vamos a viajar al antiguo

`git checkout 723ec2bf1bc23943aad69b859e5f69f235fb0945` viajamos al antiguo

El mensaje indica que ha cambiado a un commit específico con el mensaje "hola en archivo.txt". Ahora está en un estado de HEAD desconectado, lo que significa que no está actualmente en una rama. Puede realizar cambios en sus archivos y confirmarlos, pero estos cambios no estarán asociados con ninguna rama. Puede crear una nueva rama para conservar los commits que realice o puede deshacer el cambio al estado de HEAD desconectado.

`git switch -` para salir del estado de HEAD desconectado y volver al último commit en la rama que estaba

![1700148502142](image/README/1700148502142.png)

## Repositorio Remoto

`git remote add origin https://github.com/DiegoMartinez2094/git_remotee.git`

`git remote rm origin` para eliminar la seleccion del repositorio remoto en el repositorio local

selecciona el repositorio remoto, ojo debe estar en la carpeta del repositorio local.

para editar el repositorio remoto:

`git remote set-url https://github.com/DiegoMartinez2094/git_remotee.git`

`git remote -v` verifia si ya seleccioné el repositorio remoto

---

`git pull origin main`   para realizar un pull de un repositorio local a uno remoto (traer los archivos remotos)

para hacerlo de manera forzada:

`git pull origin main-- allow-unrelated-histories` indica que debe mezclar las historias tanto remotas como locales.

---

`git push --set-upstream origin MASTER` para subir los cambios al repositorio remoto:

En el caso del comando `git push --set-upstream origin MASTER`, se está indicando a Git que asocie la rama local `MASTER` con la rama remota `origin`. Esto significa que cuando se ejecute el comando `git push`, los cambios realizados en la rama local `MASTER` se enviarán a la rama remota `origin`.

---

En términos más técnicos, `git fetch` crea una nueva rama local llamada `FETCH_HEAD` que apunta a la última confirmación del repositorio remoto. Esta rama se puede utilizar para ver los cambios remotos sin fusionarlos con la rama actual.

`git pull` es una combinación de `git fetch` y `git merge`. Primero, ejecuta `git fetch` para descargar los cambios del repositorio remoto. Luego, ejecuta `git merge` para fusionar los cambios con la rama actual.

En general, `git fetch` es una buena opción si desea ver los cambios remotos sin fusionarlos con la rama actual. `git pull` es una buena opción si desea fusionar los cambios remotos con la rama actual.

**Ejemplos**

Para ver los cambios remotos sin fusionarlos con la rama actual, podemos ejecutar el siguiente comando:

```
git fetch origin main
```

Este comando descargará los cambios de la rama `main` del repositorio remoto llamado `origin`. Los cambios se almacenarán en la rama local `FETCH_HEAD`.

Para fusionar los cambios remotos con la rama actual, podemos ejecutar el siguiente comando:

```
git pull origin main
```

Este comando descargará los cambios de la rama `main` del repositorio remoto llamado `origin`. Luego, fusionará los cambios con la rama actual.

---

## GIT GREP

El comando `git grep` se utiliza para buscar texto en los archivos de un repositorio Git. Puede utilizarse para encontrar líneas de código, archivos o cualquier otro patrón específico en un proyecto.

El comando `git grep` tiene el siguiente formato:

```
git grep <texto>
```

Donde `<texto>` es el texto que se desea buscar.

*Por ejemplo*, el siguiente comando buscará la palabra `"adios"` en todos los archivos del repositorio:

```
git grep "adios"
```

`PS C:\Users\Diego martinez\OneDrive\Escritorio\NuevaCarpeta> git grep adios`
`archivo.txt:adiosito
 archivo2.txt:adios
 archivo2.txt:adios `

me indica que la palabra adios se encuentra en los dos archivos y dos veces en el archivo2.txt

---



## GIT LOG

El comando `git log` sirve para mostrar el historial de commits de un repositorio Git. El argumento `–oneline` comprime la salida del comando `git log` en una sola línea por commit.

La salida del comando `git log --oneline` tiene el siguiente formato:

```
<hash-commit> <mensaje-comit>
```

Por ejemplo, la siguiente salida del comando `git log --oneline` muestra los últimos cinco commits de un repositorio:

```
4477a20 [2023-11-19 10:00:00] Actualización del README
702282c [2023-11-18 12:00:00] Corrección de un error
c770834 [2023-11-17 14:00:00] Añadido un nuevo archivo
1234567 [2023-11-16 16:00:00] Creación del proyecto
```

El hash-commit es un identificador único para cada commit. El mensaje-comit es una breve descripción de los cambios realizados en el commit.

---

## GIT REFLOG

El comando `git reflog` sirve para mostrar el historial de cambios de los punteros de referencia (`refs`) en un repositorio Git. Los punteros de referencia son los objetos que indican la ubicación de los commits en el historial.

El comando `git reflog` puede utilizarse para ver los cambios realizados en los punteros de referencia, como los cambios realizados al cambiar de rama, al fusionar ramas o al mover commits. También puede utilizarse para recuperar commits que se hayan perdido o eliminado accidentalmente.

El comando `git reflog` tiene dos modos principales:

* **`–all`:** Este modo muestra todos los cambios realizados en los punteros de referencia, incluidos los cambios realizados en ramas remotas.
* **`–branches`:** Este modo muestra solo los cambios realizados en los punteros de referencia de las ramas locales.

---



# Git reset

El comando `git reset` sirve para restablecer el estado de un repositorio Git. Puede utilizarse para deshacer cambios, volver a un estado anterior o preparar un repositorio para una fusión.

El comando `git reset` tiene tres modos principales:

* **`–soft`:** Este modo solo restablece el índice de cambios, pero no los archivos del directorio de trabajo. Esto significa que los cambios se pueden volver a aplicar fácilmente con `git checkout`.
* **`–mixed`:** Este modo restablece el índice de cambios y los archivos del directorio de trabajo. Sin embargo, los cambios que se hayan realizado en el directorio de trabajo después del último commit se conservan.
* **`–hard`:** Este modo restablece el índice de cambios, los archivos del directorio de trabajo y la historia de commits. Esto significa que todos los cambios realizados después del commit especificado se pierden.

EJEMPLO:

primero ejecutamos el comando `git reflog`:

![1700446095816](image/README/1700446095816.png)

tenemos hash y heads, copiamos el head de donde queremos volver:

`git reset --HARD 3a62088` con este comando volvemos al head 3

---

## git shortlog

El comando `git shortlog` se utiliza para mostrar un resumen del historial de commits de un repositorio Git. El resumen incluye la cantidad de commits realizados por cada autor, junto con el título de cada commit.

El comando `git shortlog` tiene el siguiente formato:

```
git shortlog [<opciones>]
```

Las opciones más comunes del comando `git shortlog` son:

* **`-n`:** Muestra solo los autores con más commits.
* **`-s`:** Muestra la cantidad de commits en orden descendente.
* **`--since`:** Muestra los commits realizados desde una fecha determinada.
* **`--until`:** Muestra los commits realizados hasta una fecha determinada.

El comando `git shortlog -sn --all`  mostrando solo el autor y la cantidad de commits realizados por cada autor

El comando `git shortlog ` se utiliza para mostrar un resumen del historial de commits de un repositorio Git con su respetivo autor.

**`git shortlog -sn --all --no-merge`**  muestra cuantos commit han hecho cada miembros quitando los eliminados sin los merges

---

## GIT BLAME

El comando `git blame` se utiliza para mostrar quién modificó cada línea de un archivo en un repositorio Git. La salida del comando `git blame` incluye el hash del commit que modificó la línea, el nombre del autor del commit y la fecha y hora del commit.

El comando `git blame` tiene el siguiente formato:

```
git blame [<archivo>]
```

Donde `<archivo>` es el archivo que se desea analizar.

Por ejemplo, el siguiente comando mostrará quién modificó cada línea del archivo `README.md` en el repositorio actual:

```
git blame README.md
```

La salida del comando `git blame` tendrá el siguiente formato:

```
<hash-commit> <autor> <fecha> <hora> <línea>
```

Por ejemplo, la siguiente salida del comando `git blame` muestra que la línea 1 del archivo `README.md` fue modificada por el autor "juan" en el commit `4477a20`, el 19 de noviembre de 2023 a las 10:00:00:

```
4477a20 juan 2023-11-19 10:00:00 1
```

---

## GIT HELP

El comando `git help` se utiliza para obtener ayuda sobre los comandos de Git. El comando `git help` tiene el siguiente formato:

```
git help [<comando>]
```

Donde `<comando>` es el comando sobre el que se desea obtener ayuda.

Por ejemplo, el siguiente comando mostrará la ayuda para el comando `git commit`:

```
git help commit
```

La salida del comando `git help` incluirá información sobre el uso del comando, así como ejemplos de cómo utilizarlo.

El comando `git help` también tiene una serie de opciones que permiten personalizar la salida. Por ejemplo, la opción `-a` muestra la ayuda para todos los comandos, y la opción `-g` muestra la ayuda para todos los guías.

Aquí hay algunos ejemplos de cómo se puede utilizar el comando `git help`:

* **Para obtener ayuda sobre un comando específico:**

```
git help commit
```

* **Para obtener ayuda sobre todos los comandos:**

```
git help -a
```

* **Para obtener ayuda sobre todos los guías:**

```
git help -g
```

El comando `git help` es una herramienta útil para aprender a utilizar los comandos de Git.
