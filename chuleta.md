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

* **git** init : crea un repositorio nuevo.
* **git clone** /path/to/repository : clona un repositorio que está en Github a tu directorio local. ej: git clone https://github.com/arduino/Arduino
* **git commit**
* **git status** : para saber el estado de los archivos
* **git diff** : para saber las diferencias en un commit (en el/los archivos) ej: git diff HEAD
* **git log** : para ver los cambios(todos los commits) y su HEAD.
* **git reset** : para unstage archivos ej: git reset archivo.txt
* **git branch** : para hacer una rama copia de la master (o superior) y poder trabajar en ella en paralelo. ej: git branch guia_
* **git branch -d <branch name>** : para eliminar un branch.
* **git checkout** : para cambiar de rama. REVISAR
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
