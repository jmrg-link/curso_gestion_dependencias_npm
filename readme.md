<div align="center">
  <h1>Curso de Gestion de Dependencias y Paquetes NPM</h1>
  <img src="https://upload.wikimedia.org/wikipedia/commons/3/32/Platzi.jpg" alt="platzi logo" height="300px">
  <h3 style="font-weight:bold;" >Curso Node y Npm (4H)</h3>
  <h5></h5>
</div>

## Requisitos :clipboard:

*   Clousures y Scope
*   Curso de prework en; OSX (Mac), Windows o Linux.

## Comenzando 🚀

## Descripcion :notebook:

**Aprender Npm **
<p>Este curso tiene por objetivo explicar en profundidad como funcionan el gestor de paquetes npm y node en diferentes S.O.. </p>

## Listado de Temas del Curso: 💯
    *   Introduccion al funcionamiento de Node y Npm

#### ¿Qué es NPM (node package manager) ?
*    Es un gestor de paquetes, el más popular que tiene JavaScript, donde encontrarás una gran cantidad de recursos para poder implementar en tus proyectos. También vas a poder crear tus propios paquetes y compartirlos con toda la comunidad.📌

### Seccion 2 : Instalacion de Node los diferentes sistemas operativos.

*   Podemos descargar Nodejs del sitio oficial 

```text
https://nodejs.org/es/download/

Podemos selecionar distintas descargar 
    * Windows 
    * MacOs
    * Linux
```

*   En Windows seleccionaremos al instalador u seguiremos los pasos que dicta el programa instalador.
    *   Si tenemos algun terminal abierto deberemos cerrarlo para hacer que reconozca al abrirse las variables de entorno de la anterior instalacion.

*   En linux:
    *   versión LTS : sudo apt-get install nodejs npm
    *   nvm ls-remote para ver la lista de versiones que hay de node.

*   En MacOs:
    *   Modo NVM : Abriendo la terminal escribimos lo siguiente:
        *   Instalar manejador de versiones:
            *   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
        *   Instalamos con el comando:
            *   nvm install v15
    * Instando el instalador de la web oficial:
      * https://nodejs.org/es/download/
    * Instalar con brew.
      * Ejecutar comando de instalacion en terminal
        * brew install node
```text
brew update
#As a safe measure you should run brew doctor to make sure your system is ready to brew. Run the command below and follow any recommendations from brew doctor.

brew doctor
#Next, add Homebrew’s location to your $PATH in your .bash_profile or .zshrc file.

echo 'export PATH="/usr/local/opt/icu4c/sbin:$PATH"' >> ~/.profile
echo 'export PATH="/usr/local/opt/icu4c/bin:$PATH"' >> ~/.profile
#Next, install Node (npm will be installed with Node):

brew install node
node -v
```

*   Comprobar versiones con los siguientes comandos de Npm y Node:
```text 
npm --version
npm -v
```
```text 
node --version
node -v
```

*   Iniciar proyecto
``` text
npm init              //  Sirve para inicar el proyecto
package name:        //   Establecer nombre del paquete
version: (1.0.0):   //    Version que estamos creando
description:       //     Descripcion del paquete creado
entry point:       \\     archivo que inicia el proyecto
test command:       \\    archivo de test 
keywords:            \\   palabras clave
git repository:       \\  repositorio verions de git

license: tipos de licencias
url:https://es.wikipedia.org/wiki/Licencia_de_software

// Atajos:
inicio rapido: npm init -y // inicia el proyecto por default con yes 
Cambiar author: npm set init.author.email "jrico@jrico.es"
Cambiar nombre: npm set init.author.name "jesus rico"


```

*   Comandos de Npm y sus dependencias:
    *    **npm install** < packet name > --save // Paquete instalado en el proyecto
    *    **npm install** < packet name > --save-dev // Paquete se instala en desarrollo
    *    **npm install** < packet name > -D // Instala en desarollo
    *    **npm install -g < packet name > --save or --save-dev** // paquete instalado de manera global se requiere sudo en macos y linux
    *    **npm list -g --depth 0** // Busca todos los packet name globales en el sistema
    *    **npm install react --dry-run**  // Simula instalacion
    *    **npm install webpack --force** (o -f) // Instala de manera forzada
    *    **npm install@latest** // Instala versiones @latest
    *    **npm install** // Instala segun package.json 
    *    **npm install < packet name >@< version >** // Instala la version del paquete elegido.
    *    **npm list** // Lista paquetes
    *    **npm outdate** // revisar que paquetes tienen versiones nuevas
    *    **npm outdate --dd** // da mas datos de paquetes a actualizar
    *    **npm update** // actaliza los paquetes con actualizaciones
    *    **npm uninstall < packet name >** // Elimina packet name de node_modules
    *    ** npm uninstall < packet name > --no-save** //Elimina ficheros pero no en package.json 

---
Fichero **.gitignore** - Añadir ficheros o archivos a ignorar en subidas a git
```git
node_modules
```
---

*   Versionado semantico en el fichero package.lock.
*   Dicho versionado  se indica de la siguiente manera : major , minor , patch.
*   La tilde ~ coincide con la versión de parche más reciente (el tercer número) para la versión menor especificada (el segundo número).
~ 1.2.3 coincidirá con todas las versiones 1.2.x, pero se mantendrá en espera en 1.3.0.

*   El caret ^ es más relajado. Coincide con la versión secundaria más reciente (el segundo número) para la versión principal especificada (el primer número).

    *   Cuando tiene : < : Versión menor a la indicada.
    *   Cuando tiene : <= : Versión menor o igual a la indicada.
    *   Cuando tiene : > : Versión mayor a la indicada.
    *   Cuando tiene : >= : Versión mayor o igual a la indicada.

    * Explicacion de **Package.json** vs **Package-lock.json**

* Estos dos archivos son el corazón del manejo de dependencias de un proyecto en Node.

- **Package.json** contiene mas información sobre el proyecto en si, y establece las dependencias principales del proyecto.

- **Package-lock.json** guarda mas información sobre las dependencias. Por ejemplo: si estamos utilizando Express.js, esta estará referenciada en el package.json como dependencia, pero Express a su vez contiene 30 dependencias mas y 18 dependencias de desarrollo. Además de almacenar otra información importante como la version de las mismas. Esta información estará contenida en el package-lock.json.

---

#### Package.json

*   Scripts:
    *   Son comandos que podemos establecer para poder ejecutar desde la consola. Estos nos van a dar una serie de salidas según sea el caso.

    *   Podemos crear la cantidad de scripts que necesitemos. Estos scripts van a poder correr de forma nativa dentro de nuestra terminal.

```json
// Example scripts running program
"dev": "webpack-dev-server --mode development",
"build": "webpack --mode production",
"start": "serve ./dist -s -l 8080",
"format": "prettier --write '{*.js,src/**/*.js{js,jsx}}'",
"lint": "eslint src/ --fix"
```

---

#### Soluciones de Errores
##### Manejo y mejores practicas para errores.

*   Comando verbose sirve para que el sistema nos muestre informacion de como se ejecuta la aplicacion con node.

``` json

npm run build --dd

```

*   Comando para limpiar cache

``` json
npm cache clean --force
// Para verificar que verdaderamente se borro podemos usar
npm cache verify

// Si persiste un error  al borrar cache lo correcto seria eliminar carpeta node_modules y reinstalarla con el cache borrado para tener la ultima del repositorio de npm


```

 * El paquete rimraf se puede instalar con npm y permite borrar la carpeta node_modules desde cualquier sistema.
```json
//instalar globalmente
sudo npm install rimraf -g 

// ejecutar rimraf para borrar node_modules
rimraf node_modules
```
---

#### Auditar paquetes en node

Podemos revisar las vulnerabilidades de nuestro proyecto con:
*   **npm audit:**
    *   En caso de tener vulverabilidades, se recomienda usar el comando:
*   **npm audit fix:**
    *   Y en caso de que esto no lo solucione, podemos ir actualizandolos de uno en uno.
*   **npm update < package name > --depth 2**
    *   Para actualizar el paquete y dependencias de un modulo instalado

```json
// Genera un archivo json de npm audit
npm audit --json
```
---

### Loguearse en NPM
#### Registrar cuenta en la web de npm.

```bash
npm adduser 

Username: <nickname>
password: <your-password>
email:    <email@email.com>
```

#### Probar paquete de  forma local
*   Antes de subir probar paquete de manera local
```bash
sudo npm link
#Se ejecuta la función
random-msg
```

#### Publicar paquete en npm
*   En la ruta del fichero a publicar ingresar comando.
```bash
npm publish 
```
---

#### Informacion previa a la subida del package en npm
* Para mejorar nuestros paquete y que cuente con los requerimientos mínimos para serlo haremos lo siguiente:
crearemos un buen README.md en donde vamos a explicar lo que hará nuestro paquete osea toda nuestra documentación, además esto debe estar en ingles.

*   Ademas debemos Conectarlo a un repositorio de github
npm init ahora veremos que ya esta ligado a un repositorio, de igual forma podemos ver esta información en el package.json.

    * **npm version <major |minor |patch>** nos permite actualizar la versión de nuestro proyecto o paquete ejem npm version patch y el resultado seria v1.0.1, muchas veces nos dira que debemos actualizar a la versión mas reciente de npm y lo hacemos con sudo install -g npm , si nos vamos al package veremos que la versión a cambiado, y para publicarlos volvemos a ejecutar el comando npm publish
    *   **npm unpublish -f** para despublicar un paquete recuerda que debes estar ubicado en la carpeta raíz del proyecto
