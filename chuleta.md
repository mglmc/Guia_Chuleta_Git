### Chuleta de control de versiones con git

##### POR HACER

_Indica qué tenemos que saber y saber hacer en la asignatura de Proyectos de Sistemas Electrónicos. _

## Control de versiones
El control de versiones básicamente consiste en mantener el control de los cambios que se realizan sobre la configuración de algun documento o producto.


## Conceptos

* Repositorio local: base de datos centralizada donde se guardan las distintas versiones de los ficheros sometidos al control de versiones.

* Repositorio remoto: es un repositorio local que reside en el servidor centralizado.

* Copia local: es la copia que se realiza a algún fichero sometido a control de versiones.

* log: Registro que muestra todos los cambios que se han realizado en un repositorio.

* Conflicto: problema que surge cuando los clientes realizan cambios incompatibles entre si.


## Operaciones:  

* Clone: replica un repositorio entero con todo su historial de cambios y actualiza el directorio local.

* Add: realiza la copia de un fichero modificado, poniéndola en la zona de preparación para ser confirmada.

* Commit: acción que se realiza cuando queremos que los cambios que hemos realizado en el fichero se suban al repositorio.

* Push: es la operación en la que se envian al repositorio centralizado un commit o un conjunto de commits.

* Pull: es la operación en la que se actualiza el repositorio local y el directorio local con commits que provienen del repositio remoto. Es la acción contraria a push.

* Fork: clone que se realiza dentro del mismo servidor. Al repositorio original se le llama UPSTREAM.

* Pull Request: 
  - Entre Ramas: petición que se hace al desarrollador de una rama para que sus cambios se unan con la rama principal

  - Entre repositorios: petición que se hace al desarrollador de que los cambios hechos por elfork sean incorporados al repositorio original.


## Clientes Gráficos:

* SourceTree

## Servicios de repositorios remotos con control de errores:

* GitHub
* GitLab
* Bitbucket

## Comandos útiles para git:

**En el interprete de comandos de git-bash**

* Mostrar en que directorio estamos: **pwd**
* Crear un directorio: **mkdir nombreDirectorio**
* Cambiar de directorio: **cd RutaDelNuevoDirectorio**
* Mostrar la lista de ficheros de un directorio: **ls**
* Borrar un fichero: **rm nombreArchivo** 
* Cambiar (mover) un fichero de directorio: **move nombreDirectorio**

**En Control de versiones local**

* Crear un repositorio local en nuestra máquina: **git init**
* Preparar ficheros para ser confirmados en el repositorio local: **git add NombreFichero**
* Confirmar cambios en un repositorio local: **git commit -m "Comentario con los cambios realizados"**
* Deshacer las operaciones de preparar y confirmar: **git reset <commit>** 
* Identificar el estado de un fichero o ficheros en un repositorio local: **git status**

**En control de versiones centralizado**

* Configurar git para que trabaje tras un proxy: **git config --global http.proxy 'proxy.satd.uma.es:3120'**
* Replicar un repositorio remoto localmente en nuestra máquina: **git clone URLrepositorio** (pej: git clone http://github.com/arduino/Arduino)
* Replicar un repositorio local en un servidor remoto: **git remote add origin URLservidorRemoto** (pej: git remote add origin https://github.com/uma-dte-docencia/chuleta-git-2017-18-internautas-1)
* Traer los cambios de un repositorio remoto a un repositorio local: **git pull**
* Enviar los cambios de un repositorio a uno remoto: **git push NombreRemoto NombreRama** (pej: git push origin master)
si ya se esta en la rama master basta con hacer git push

**En control de versiones distribuido**

* Crear una rama en un repositorio local: **git branch nombreNuevaRama**
* Cambiar de rama en la copia local: **git checkout nombreRama**
* Enviar la rama al repositorio remoto: **git push origin NombreRama**
* Realizar un pull request entre dos ramas de un repositorio remoto:
* Realizar un pull request entre dos repositorios que resultaron de un Fork:

**Otros comandos de interes**

* **git diff** : para saber las diferencias en un commit (en el/los archivos) ej: git diff HEAD
* **git log** : para ver los cambios(todos los commits) y su HEAD.
* **git reset** : para unstage archivos ej: git reset archivo.txt
* **git branch -d <branch name>** : para eliminar un branch.
* **git merge** : para unir tu rama a otra. ej: git merge rama2
* **git config --global http.proxy 'proxy.wifi.uma.es:3128'** : para redes con proxy
* **git add origin (archivos que vas a modificar)** ->origin es el nombre (alias) que se le da al repositorio al que le vas a hacer stage
* **git fetch [remote-name]** : para recuperar datos remotos de tus repositorios remotos
* **git pull** : para recuperar y unir la rama remota con la rama actual.
* **git push** [nombre-remoto][nombre-rama] : para enviar un repositorio local a uno remoto Ej: git push origin master
* **git rm [files]** : para eliminar algún archivo del repositorio. ej: git rm '*.txt'
* **git remote -v** : muestra los repositorios remotos que tienes con su respectivo enlace
* **git remote** : muestra los alias de los repositorios remotos que tienes
* **git remote add [nombre] [url]** : para añadir repositorios remotos y asignarle un alias
* **git remote show [nombre-repositorio]** : para mostrar más información del repositorio remoto
* **git remote rename** : para renombrar una referencia a un repositorio remoto
* **git remote rm  [alias-repositorio-remoto]**: para eliminar un repositorio remoto


## Comandos útiles para la terminal:

## Tips:

*
*
