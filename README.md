# Introduccion a git
Que es un control de versiones?
Es un sistema que registra cada cambio que se realiza en codigo fuente de un proyect.
Este permite tener todos los cambios producidos en sus ficheros, asi mismo saber 
quien y cuando lo hicieron. 

### CLASE 1
 ## GIT COMMIT
 Sirve para registrar los cambios que se han producido en el repositorio
   git commit -m "aniadimos una neva busqueda"
```bash
git commit -m "NombreNuevo"
```  
  ## GIT INIT
  Crea un repositorio local es deci proyecto nuevo
 ```bash  
git init
```  
## GIT ADD
Sirve para incluir archivos nuevos en un directorio contreto
# CLASE 2
## GIT BRANCH
Permite crea,listar ,eliminar y renobar las ramas
bash
git brach mi-primera-rama

## GIT MERGE
Sirve para incorporar los cambios de una rama a la rama en la que nos encontramos
## GIT CHECKOUT
Cambia entre ramas y restura en el directorio de trabajo
## RESOLVER CONFLICTOS
Es una situacion en la que no es capaz de determinar que cambio es el tiene prevalecer una vez ocurra la fusion
bash
git diff
++<<<<<<<HEAD

## GIT CONFIG
Permite eitar lo que se utiliza en git

# CLASE 3
Que son las ramas y para que sive
## GIT REMOTE ORIGIN<URL>
Agregamos el url del repositorio remoto del code HTTPS O SSH se necesita que sea publico
## GIT PUSH ORIGIN<rama>
Nos permite sincronizar los cambios  de los repositorios  local con el remoto
 ## GIT REMOTE PRUNE ORIGIN 
 Nos permite elimnar ramas que ya no existen en el remoto  y que podemos eliminar en el local
 ## GIT BRANCH -a ,  GIT SWITCH
 Nos permite visualizar las remotas como local referenciadas
# CLASE 4
Pull Request : Es una peticion de cambios que se envia el repositorio original
# CLASE 5
 ## GIT FLOW
 RAMAS PRINCIPALES
 MAIN: Su proposito es contener el codigo que encuentre en produccion 
 DEVELOP: Tienen caracteristicas que todavia tienen que ser probadas y validas
 # CLASE 6
## BUENAS PRACTICAS
- Usar los verbos imperativos  
add : Añade un nuevo archivo
bash
git commit -m "añadimos un nuevo archivo."  # esta mal por el punto final
git commit -m "para arreglar un problema..." # esta mal por los puntos suspensivos 
git commit -m "cambiamos por defecto el sistema del color" # esta bien ya que no hay errores de sintaxis 

- Usar como maximo 50 caracteres para todos los mensajes de commit
- Usar los prefijos para los commits

feat : para una nueva caracteristica del usuario
fix : bug que afecta al usuario 
 perf : cambios que mejora los rendimientos     
 build : para cambios del sistema  
ci : para los cambios de integracion    
refactor : refactorizacion de codigo      
test : refactoriza un codigo ya  existente
# CLASE 7
### COMO DESHACER MIS CAMBIOS?
Hay dos formas de deshacer el ultimo commit.
bash
git reset --soft HEAD-1

Con este comando que se hace en vez de eliminarlos,mantiene los cambios  que se hicieron en el commit 
# CLASE 8
## Que es un Hook?
Nos permite ejecutar una accion o script cada vez que ocurre un evento en git.
- pre-commit : permite comprobar o es un bue sitio para ejecutar linter   
- prepare-commit-msg : modifica o añade mensajes
- pre-push :  ejecuta una bateria de test
- posst-checkout y post-merge : permite limpiar el directorio de trabajo despues de hacer checkout que ya no se usan tras realizar un merge.
## QUE ES UN ALIAS?
Nos permite crear nuestros propios comandos que se usan habitualmente
bash
git config --global alias.[nombre-del-alias]
