
# Chuleta de control de versiones con git

_Indica qué tenemos que saber y saber hacer en la asignatura de Proyectos de Sistemas Electrónicos._

## Control de versiones
El control de versiones consiste básicamente en mantener el control de los cambios que se realizan en el tiempo sobre un conjunto de archivos integrados en un repositorio.


## Conceptos

* **Repositorio local**: Base de datos centralizada donde se guardan las distintas versiones de los ficheros sometidos al control de versiones.
* **Repositorio remoto**: Es un repositorio local que reside en el servidor centralizado.
* **Copia local**: Es la copia que se realiza a algún fichero sometido a control de versiones.
* **log**: Registro Que muestra todos los cambios que se han realizado en un repositorio.
* **Conflicto**: Problema que surge cuando los clientes realizan cambios incompatibles entre si.


## Operaciones:  

* **Clone**: Replica un repositorio entero con todo su historial de cambios y actualiza el directorio local.
* **Add**: Realiza la copia de un fichero modificado, poniéndola en la zona de preparación para ser confirmada.
* **Commit**: Acción que se realiza cuando queremos que los cambios que hemos realizado en el fichero se suban al repositorio.(Tras el commit es necesario el Push)
* **Push**: Es la operación en la que se envian al repositorio centralizado un commit o un conjunto de commits.
* **Pull**: Es la operación en la que se actualiza el repositorio local y el directorio local con commits que provienen del repositio remoto. Es la acción contraria a push.
* **Fork**: Clone que se realiza dentro del mismo servidor. Al repositorio original se le llama UPSTREAM.
* **Pull Request**:
  - Entre Ramas: Petición que se hace al desarrollador de una rama para que sus cambios se unan con la rama principal
  - Entre repositorios: Petición que se hace al desarrollador de que los cambios hechos por el fork sean incorporados al repositorio original.

* **Merge**: La operación donde se une un branch (una rama) a otro branch master (o superior) y se combinan.
* **Branch** : cuando quieres trabajar en paralelo sobre un mismo proyecto y no quieres interferir o llenar commits (cambios) la rama master(principal) te haces tu propia rama para trabajar sobre ella y cuando hayas terminado la unes (haces merge).

## Comandos útiles para git:

**Para el manejo de ficheros en el terminal**

* **pwd**: Mostrar en que directorio estamos.
* **mkdir** _[nombreDirectorio]_: Crear un directorio.
* **cd** _[RutaDelNuevoDirectorio]_: Cambiar de directorio.
* **ls**: Mostrar la lista de ficheros de un directorio.
* **rm** _[nombreArchivo]_: Borrar un fichero.
* **move** _[nombreDirectorio]_: Cambiar (mover) un fichero de directorio.
* **ls -all** : lista todos los archivos incluidos los que empiezan con punto.
* **cd ..**  : para volver atrás en el directorio.
* **touch** : crea un archivo vacío.
* **mkdir -p** : crea ramas de directorios que no existen.
* **man** _[comando]_ : para consultar en el manual dicho comando.
* **cat** : concatena archivos y/o los muestra como salida.
* **/*.extension** : para referirnos a todos las extensiones de un directorio.

**En control de versiones local**

* **git init**: Crear un repositorio local en nuestra máquina.
* **git add** _[NombreFichero]_: Preparar ficheros para ser confirmados en el repositorio local.
* **git commit -m** _"Comentario con los cambios realizados"_: Confirmar cambios en un repositorio local.
* **git reset commit**: Deshacer las operaciones de preparar y confirmar.
* **git status**: Identificar el estado de un fichero o ficheros en un repositorio local.

**En control de versiones remoto**

* **origin**: Es el nombre que se le da al servidor origen (no es un comando).
* **git config** _--global http.proxy 'proxy.satd.uma.es:3120'_: Configurar git para que trabaje con un proxy.
* **git clone** _[URLrepositorio]_: Replicar un repositorio remoto localmente en nuestra máquina (pej: git clone http://github.com/arduino/Arduino Arduino_Code).
* **git remote add origin** _[URLservidorRemoto]_: Añade un repositorio remoto para poder trabajar con el (pej: git remote add origin https://github.com/uma-dte-docencia/chuleta-git-2017-18-internautas-1).
* **git pull**: Traer los cambios de un repositorio remoto a un repositorio local.
* **git push** _[NombreRemoto NombreRama]_: Enviar los cambios de un repositorio a uno remoto (pej: git push origin master) si ya se esta en la rama master basta con hacer git push.
* **git fetch** _[NombreRemoto]_: A diferencia de *git pull* solo actualiza los datos del remoto sin hacer efecto en los archivos en los que estes trabajando.  
* **git remote -v** : Muestra los repositorios remotos que tienes con su respectivo enlace.
* **git remote** : Muestra los alias de los repositorios remotos que tienes.
* **git remote add** *[Alias RepRemoto]* : Para añadir repositorios remotos y asignarle un alias.
* **git remote show** *[RepRemoto]* : Para mostrar más información del repositorio remoto.
* **git remote rename** : Para renombrar una referencia a un repositorio remoto.
* **git remote rm** *[RepRemoto]*: Para eliminar un repositorio remoto.

**En control de versiones distribuido**

* **git branch** _[NombreNuevaRama]_: Crear una rama en un repositorio local.
  * **git branch -f master HEAD~3**: Crea una rama nueva y fuerza a que el master sea donde está el HEAD pero 3 commit atras.
* **git checkout** _[NombreRama]_: Cambiar de rama en la copia local.
  * **git checkout -b** _[NombreNuevaRama]_: Cambia de rama y crea una nueva.
  * **git checkout** _[Cambio]_: El cambio puede ser a un commit específico.
* **git push origin** _[NombreRama]_: Enviar la rama al repositorio remoto.

* Para realizar un pull request entre dos ramas de un repositorio remoto y entre dos repositorios que resultaron de un Fork el proceso hay que hacerlo a través de la interfaz de la pagina de git (en este caso Github) o por un cliente de escritorio (por ejemplo SourceTree) donde se le explicará al los encargados del repositorio original o la rama master (o superior) de los cambios realizados y la justificación para que sea añadido en dicha rama a traves de un **merge**.

**Otros comandos de interes**

* **git diff** : Para saber las modificaciones o cambios en un commit (en el/los archivos) ej: git diff HEAD.
* **git add ./*** : Para añadir todos los archivos del directorio.
* **git log** : Para ver los cambios (todos los commits) y su HEAD.
* **git reset** : Para unstage archivos ej: git reset archivo.txt
* **git branch -d** _[BranchName]_ : Para eliminar un branch (la instruccion branch también permite crear y listar ramas mediante otros atributos).
* **git merge** : Para unir tu rama a otra. ej: git merge rama2
* **git add** Origin _[ArchivosAModificar]_ :origin es el nombre (alias) que se le da al repositorio al que le vas a hacer stage.
* **git stash** : Cuando trabajas en un archivo (y lo modificas) en un repositorio y quieres cambiar de rama se hace un preguardado que tienes que anular con este comando.
* **git rm** _[Archivos]_ : Para eliminar algún archivo del repositorio. ej: git rm *'*.txt'
* **rm -rf .git** : para eliminar un git init
* **git status** para saber donde estas y donde git te puede dar alguna pista sobre que puedes hacer.


## Operaciones específicas:

##### Añadir las modificaciones al repositorio
1. *cd* _nombreDirectorio_
2. *git add* _nombreArchivoModificado_
3. *git commit -m "comenario sobre las modificaciones"*
4. *git push*

##### Clonar un repositorio y crear uno nuevo identico (mirroring)[Fuente](https://help.github.com/articles/duplicating-a-repository/):

1. Clonar el repositorio:
*git clone --bare https://github.com/exampleuser/old-repository.git*
2. Nos movemos a la ubicación donde se ubica el repositorio clonado con el comando *cd*
3. Push con el atributo mirror:
*git push --mirror https://github.com/exampleuser/new-repository.git*
4. Movemos el directorio uno arriba *cd ..*
5. Eliminamos el repositorio temporal creado en el paso 1:
*rm -rf old-repository.git*

## Tips:

* Se recomienda ante dudas lo primero es hacer **git status**.
* Si quieres volver a quitar el proxy de github tienes que abrir con permiso (sudo) un editor de texto el config de github Ej: sudo **open ~/.gitconfig** y comenta (con #) las lineas donde esté configurado el proxy **#proxy = proxy.wifi.uma.es:3128** y **#[http]**.
* Cuando hagas un **git branch** recordar hacer el **checkout** [nombre de la nueva rama] para empezar a trabajar en dicha rama.
* Para empezar se recomienda hacer este turial de git:  https://try.github.io/
* Para saber como escribir el **Readme.md** -> [Página muy útil](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* Usando el **caracter** (**^**). Nos referimos al padre (parent) del commit. p.e: Poniendo _master^_ es equivalente a decir el primer pariente del master.

## Clientes Gráficos:

* **SourceTree**: Disponible para Windows y MAC.
* **GitKraken**: Disponible para Windows, Linux y MAC.
* **GitHub Desktop**: Disponible para Windows y MAC.

## Servicios de repositorios remotos con control de errores:

* **GitHub**
* **GitLab**
* **Bitbucket**

## Referencias:

* https://gist.github.com/jelcaf/1404619
* http://rogerdudler.github.io/git-guide/index.es.html
* https://git-scm.com/book/es/v1/Fundamentos-de-Git-Trabajando-con-repositorios-remotos
* https://aprendiendoausarlinux.wordpress.com/2011/11/18/el-comando-cat-en-unix/
* https://gist.github.com/evantoli/f8c23a37eb3558ab8765
