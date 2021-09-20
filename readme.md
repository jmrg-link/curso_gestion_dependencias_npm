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
*    Es un gestor de paquetes, el más popular que tiene JavaScript, donde encontrarás una gran cantidad de recursos para poder implementar en tus proyectos. También vas a poder crear tus propios paquetes y compartirlos con toda la comunidad..📌

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

*   