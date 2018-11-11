<!-------------------------------------------------------------------------------------------------------------!>
Git merge
##git merge nos sirve para unir el trabajo de dos ramas para esto nos paramos sobre la rama que queremos unirle el trabajo de otra y ponemos el ocmando git merge nombre
<<<!-------------------------------------------------------------------------------------------------------------!>


<!-------------------------------------------------------------------------------------------------------------!>
Git stash
##git stash nos sirve para guarda cambios temporalmente en una rama por si tenemos que hacer un hotfiz rapido
##git stash list nos muestra una lista con los stash
##git stash drop '{stash}' elimina un stash
<!-------------------------------------------------------------------------------------------------------------!>



<!-------------------------------------------------------------------------------------------------------------!>
LLave ssh esta nos sirve para tener una conexion entre mi pc y github la plataforma, cuando hablamos de mi propio repositorio

##para hacer unsa llave ssh con  git y github hacemos lo siguiente

##ssh-keygen -t rsa -b 4096 -C "correo de la cuenta"

##luego copiamos la llave ssh 

##cat ~/.ssh/id_rsa.pub

##vamos a github en settings, donde estan las key ssh agregaos una nueva, ahi pegamos la que copiamos del bash  y la generamos

<!-------------------------------------------------------------------------------------------------------------!>


<!-------------------------------------------------------------------------------------------------------------!>
##Git remote sirve para crear una conexion entre mi repositorio local y mi repositorio para poder compartirlo con la comunidad, para esto vamos a usar un nuevo comando 

##git remote add nombre

##por convencion lo nombramos origin

##git remote -v lista de las conexiones existentes

##git remote remove 'nombre sin las comillas' elimina una conexion con ese repositorio

##como buenas practias es recomendable:

###el nombre del repositorio creado en github (u otra plataforma) debe ser el mismo que el nombre de la carpet aproyecto

###primero crear el repositorio remoto en github, luego clonarlo al repositorio local en tu maquina 

##si queremos cambiar el nombre de un repositorio remoto 

###git remote set-url origin git@github.com:ppreyer/first_app.git

<!-------------------------------------------------------------------------------------------------------------!>


<!-------------------------------------------------------------------------------------------------------------!>
##Git pull nos sirve para traernos cambios en nuestro repositorio remoto, como cuando trabajamos en equipo y alguien subio una actualizacion al repositorio remoto entonces los descargamos con 

##git pull origin master

si nos da error le agregamos 

##git pull origin master --allow-unrelated-histories

<!-------------------------------------------------------------------------------------------------------------!>


<!-------------------------------------------------------------------------------------------------------------!>
##Git push nos permite subir cambios al repositorio remoto

##git push origin master = envia la rama master

##tambien podemos enviar tags 
###git push origin master --tags

##podemos enviar cualquier rama solo debemos cambiar el nombre
#git push origin RD

<!-------------------------------------------------------------------------------------------------------------!>


<!-------------------------------------------------------------------------------------------------------------!>
Creando un template para issues
##lo hacemos desde github creamos un nuevo archivo 

ej: issue_template.md

y dentro ponemos algo como: 

## ¿Como puedo replicar el problema?
Por favor explicanos como replicar el problema paso a paso y en que sistema operativo ocurre

## ¿En que version occure?
Si este problema ocurre en todas las versiones por favor tambien mencionarlo

luego creamos un issue de ejemplo para ver que sale este texto

<!-------------------------------------------------------------------------------------------------------------!>


<!-------------------------------------------------------------------------------------------------------------!>
Creando un template para pull request 

##creamos un nuevo archivo pull_request_template.md

## Descripcion

¿Que ha cambiado?

- [] Frontend
- [] Backend
- [] Configuracion del server

Como puedo probar los cambios ?
en que url y forma puedo ver el update

<!-------------------------------------------------------------------------------------------------------------!>

<!-------------------------------------------------------------------------------------------------------------!>
.gitignore (Ignorando archivos no deseados)

##si tienes archivos que no pueden ser publicos, como archivos de configuracion con contraseñas, lo ideal es que no lo subas a tu repositorio, estos archivos los puedes poner en el archivo .gitignoe

##creamos un archivo ejemeplo setting.py

##creamos un archivo .git ignore

##dentro de ese ponemos la linea setting.py, llamando a ese archivo


##ponemos lo siguiente adentro, este es un ejemplo para node js que no me muestre lo que no tiene que mostrarme

esto lo acemos desde github entonces como no podemos hacr un commit, creamos una nueva rama ahi sale la opcion. y como tenemos un template para pull request nos envia a eso, y es lo que hacemos en la siguiente seccion 


# Created by https://www.gitignore.io/api/node
# Edit at https://www.gitignore.io/?templates=node

### Node ###
# Logs
logs
*.log
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Runtime data
pids
*.pid
*.seed
*.pid.lock

# Directory for instrumented libs generated by jscoverage/JSCover
lib-cov

# Coverage directory used by tools like istanbul
coverage

# nyc test coverage
.nyc_output

# Grunt intermediate storage (https://gruntjs.com/creating-plugins#storing-task-files)
.grunt

# Bower dependency directory (https://bower.io/)
bower_components

# node-waf configuration
.lock-wscript

# Compiled binary addons (https://nodejs.org/api/addons.html)
build/Release

# Dependency directories
node_modules/
jspm_packages/

# TypeScript v1 declaration files
typings/

# Optional npm cache directory
.npm

# Optional eslint cache
.eslintcache

# Optional REPL history
.node_repl_history

# Output of 'npm pack'
*.tgz

# Yarn Integrity file
.yarn-integrity

# dotenv environment variables file
.env

# parcel-bundler cache (https://parceljs.org/)
.cache

# next.js build output
.next

# nuxt.js build output
.nuxt

# vuepress build output
.vuepress/dist

# Serverless directories
.serverless

# FuseBox cache
.fusebox/

# End of https://www.gitignore.io/api/node

<!-------------------------------------------------------------------------------------------------------------!>


<!-------------------------------------------------------------------------------------------------------------!>
Pull Request (Colabora a proyectos externos)

##ya que hemos bloqueado la rama master por un proceso de sugirad para que no se filtre ningun codigo que se podria ir sin la revision de ninguno de los colaboradores tenemos los pull request
