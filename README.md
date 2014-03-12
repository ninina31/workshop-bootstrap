workshop-bootstrap-1
====================

Primera sesion del workshop de bootstrap. En esta sesión se tratará:

1. Instalación y preparación de un proyecto para la admisión de Bootstrap 3
2. Técnicas de configuración y personalización de Bootstrap 3 usando less

# Instalación
Cámbiate al branch "setup" del repositorio, ya que este viene con algunas
configuraciones que harán mas ágil el desarrollo del taller.

Para este taller y para el uso general de Bootstrap se recomienda el uso de las
siguientes herramientas:

    * Node.js y npm
    * Bower
    * Grunt

### Node.js
    Es una plataforma para el desarrollo de aplicaciones. En ella se apoyan todas
    las herramientas que estaremos aprendiendo, usando e instalando via npm.
    
### npm
    Es el manejador de paquetes de Node, con él puedes instalar Grunt, Bower, etc.

### Bower
    Es un administrador de librerías y frameworks, ¿Quieres jQuery?, ¿Quieres Bootstrap?
    usa Bower y obtenlos por ahi!

### Grunt
    Es un task runner para Javascript, permite automatizar tareas fastidiosas y 
    repetitivas como por ejemplo compilar un less a css, o compilar un cofeescript
    a javascript.

    Grunt es quizas la herramienta mas poderosa y mas importante de todas. Esta
    sesión del workshop no es suficiente ni siequiera para rasgar la superficie
    del poder de Grunt.

## npm y bower install  
    Debes correr los siguientes comandos para instalar todo lo mencionado
    anteriormente:

    * npm install
    * bower install

    Si todo fue bien, se debieron haber creado un par de directorios, app/bower_components y
    /npm_components ambos son las ubicaciones de las librerías y herramientas que se 
    instalaron. Lo importante aqui es app/bower_components

## Echale un ojo al Gruntfile!
    El gruntfile es muy importante! antente a la explicación! Sin embargo esto sale un poco
    del alcance de esta sesión en específico y no vale la pena invertir mucho tiempo el día
    de hoy, pero otro día lo haremos!

## Compila tu Bootstrap!
    Como ya viste, el Gruntfile viene preconfigurado con tareas que compilan el less de
    bootstrap.

    * less:compile

# Personalización
    Un pilar fundametal de Bootstrap es la personalización y creación de nuevos temas, sin
    embargo surgen preguntas como:

    1. ¿Si quisera personalizar una clase de Bootstrap como haría?
    2. ¿Que pasa cuando quiera actualizar Bootstrap?
    3. ¿Por que no lo configuro y lo descargo desde su website?

Discutiremos cada una de estas en el Workshop, para ello, cámbiate al branch "customize"
del repositorio.

## Si quisieras personalizar Bootstrap
    Para personalizar Bootstrap debemos seguir ciertas reglas muy importantes y que
    por ningún motivo, circunstancia o razón debemos quebrantar:

    * Jamás en tu vida modifiques el código fuente de Bootstrap!!! Eso es todo.

    Pero para no hacer eso, bueno, hay algunos trucos:

    * Crea los siguientes archivos en app/styles/:
        1. my-theme.less
        2. custom-bootstrap.less
        3. custom-variables.less

En el fondo lo que queremos es personalizar Bootstrap creando un tema que al compilarlo
genere un bello css. Para esto nos ayudaremos con los archivos que ya vienen en Bootstrap:

### my-theme.less
Aqui debes importar custom-bootstrap.less

* import "custom-bootstrap.less";

Luego de esto puedes colocar todo el "less que quieras"

### custom-bootstrap.less
Este archivo es identico al original "bootstrap.less", pero los valores de sus
variables los obtiene del archivo "custom-variables.less", por lo tanto, quedaría así:

* import "bootstrap.less"
* import "custom-variables.less"

### custom-variables.less
Este archivo es un copy-paste del original, por lo que no lo colocaremos aqui :P. Sin embargo lo
que se quiere hacer en este archivo es simplemente cambiar el valor de las variables.

Por ejemplo, si el fondo era blanco, aqui lo puedes poner negro, asi poco a poco, dando valores a 
estas variables terminarás creando tu propio tema! Que genial!

