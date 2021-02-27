

# Informe Práctica 2: Instalación y configuración de Visual Studio Code


![Image](https://i.imgur.com/UqPxPnZ.jpg)



╔═══════════════════════════════════════════════════════════════════╗

> - Autora: Andrea Calero Caro
> - Alu: [alu0101202952@ull.edu.es](alu0101202952@ull.edu.es)
> - Práctica: 2 Instalación y configuración de Visual Studio Code
> - Asignatura: Desarrollo de Sistemas Informáticos
> - Universidad de La Laguna

╚═══════════════════════════════════════════════════════════════════╝



▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂


## Índice


  - Objetivos
  - Paso previo: Aceptación de tarea de GitHub Classroom
  - Instalación y funcionalidad de Visual Studio Code
    - Configuración de Visual Studio Code para conectarse a una máquina remota por SSH
    - Sesiones colaborativas con Visual Studio Live Share 
  - Primer proyecto en TypeScript: “Hola Mundo”
  - Desarrollo del informe con GitHub Pages
  - Conclusiones
  - Bibliografía y/o Webgrafía
  
  



▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂


## OBJETIVOS


Los objetivos en esta práctica serán la instalación y configuración de Visual Studio Code, además de nuestro primer proyecto en TypeScript: “Hola Mundo”. Todo ello junto con la presentación de este informe y el desarrollo del mismo en GitHub Pages.




▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂


## PASOS PREVIOS: ACEPTACIÓN DE TAREA DE GITHUB CLASSROOM


Antes de comenzar se nos requiere que aceptemos la tarea asignada en el GitHub Classroom:

![Asignación GitHub Classroom](https://i.imgur.com/JPwjWBt.jpg)

Con ello ya podríamos trabajar en esta práctica.



▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂


## INSTALACIÓN Y CONFIGURACIÓN DE VISUAL STUDIO CODE


Lo primero sería instalar el Visual Studio Code, como yo ya lo tenía simplemente lo ejecuté poniendo en la terminal :

> `$code .`

### CONFIGURACIÓN DE VISUAL STUDIO CODE PARA CONECTARSE A UNA MÁQUINA REMOTA POR SSH

El siguiente paso será como su nombre indica poder conectarse desde el VSC a una máquina remota, en mi caso, la máquina con host: _iaas-dsi31_
Previamente y cómo se sabe tenemos que conectarnos a la VPN de la Universidad de La Laguna:

![VPN](https://i.imgur.com/w4WhqxN.jpg)

A continuación pulsando la tecla > `F1` estando en el VSC se abriría una barra con opciones de conexión remota, y pincharíamos sobre > `Remote-SSH: Connect to Host...`, como se puede ver veríamos distintos Host pero como queremos añadir el host de nuestra máquina virtual, tendríamos que pinchar sobre > `Configure SSH Hosts...` y con ello añadir el host de la máquina remota **iaas-dsi31**:

![Connect to Host](https://i.imgur.com/YGGx7Wy.jpg)

Veríamos el fichero donde debemos añadir el host > `~/.ssh/config`:

![~/.ssh/config](https://i.imgur.com/7SQWUlO.jpg)

Añadiendo así las líneas, líneas 16, 17 y 18 del archivo de la siguiente imagen:

![SSH Config](https://i.imgur.com/wT9STZO.jpg)

Con > `Ctrl + S` guardamos los cambios, pulsamos de nuevo la tecla > `F1`, en la opción > `Remote-SSH: Connect to Host...` encontraríamos así el host de nuestra máquina si la hemos configurado bien:

![Connect to iaas-dis31](https://i.imgur.com/5TFrqYr.jpg)

Al pinchar sobre el host **iaas-dsi31** entraría en remoto con mi MV si no hubiese ningún inconveniente. Como todo fue satisfactorio, lo siguiente fue comprobar que en efecto nos encontramos en nuestra máquina virtual, para ello en el panel superior abrimos una nueva terminal o con la combinación > `Ctrl + Shift + ñ`, y en dicha terminal ponemos `hostname` para corroborar que estamos en la máquina virtual desde VSC:

![Hostname](https://i.imgur.com/sFZgwtS.jpg)

Así observamos que se conectó corectamente.


### SESIONES COLABORATIVA CON VISUAL STUDIO LIVE SHARE


Visual Studio Live Share permite colaborar en las tareas de desarrollo en tiempo real, y para usarlo necesitamos instalar su paquete de extensiones junto con todas las extensiones recomendadas que se puede encontrar al final del siguiente sitio Web:

『 』[Live Share Extension Pack](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-pack)

Instalando así las extensiones recomendadas y las propias del pack de Live Share:

![Extension recomendada 1](https://i.imgur.com/DwZajTg.jpg)

![Extension recomendada 2](https://i.imgur.com/2CTgmiu.jpg)

━━━━━━━━━━━━━━━━━━━━━━━━━━✧❂✧━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Estas extensiones las instalamos tanto en nuestra máquina local como remota, quedando guardadas todas las extensiones:

![Extension pack](https://i.imgur.com/T49IKDV.jpg)

━━━━━━━━━━━━━━━━━━━━━━━━━━✧❂✧━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Cuando ya están todas las extensiones instaladas las podemos probar siguiendo los pasos de la página anterior nombrada. Para finalizar, VSC con Lve Share pide vincularte con nuestra cuenta de GitHub:

![Vincular extensiones](https://i.imgur.com/gXT1980.jpg)

Probando buscar participantes:

![Participantes](https://i.imgur.com/mKFBhhA.jpg)

━━━━━━━━━━━━━━━━━━━━━━━━━━✧❂✧━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━



▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂


## PRIMER PROYECTO EN TYPESCRIPT: "HOLA MUNDO"

En primer lugar instalamos la extensión obligatoria de **ESLint**, esta nos permite realizar comprobaciones de estilo sobre ficheros que incluyan código fuente en JavaScript y TypeScript.

A continuación abrimos una Nueva Terminal, en VSC dentro de la conexión SSH con mi máquina virtual, en la barra superior de tareas o con la combinación > `Ctrl + Shift + ñ`. Y procederemos a instalar el compilador de TypeScript, y veremos la versión en la que se encuentra con el comando > `tsc --version` tal que:

![Instalar compilador de TypeScript](https://i.imgur.com/j1JDNYP.jpg)

Y en la terminal comprobamos la ruta en la que estamos situados con > `pwd` y creamos el directorio hello-world, en el que trabajaremos para crear nuestro primer programa de **"Hola Mundo"**

Como ya sabemos tendremos primero que clonar el repositorio asignado en la tarea de GitHub Classroom con > `git clone [enlace]` y trabajaremos desde el repo, por tanto, comenzaremos con > `git init` para trabajar en la rama.

Y ya podríamos hacerlo:

![mkdir hello-world](https://i.imgur.com/jZOyq1d.jpg)

Veríamos a su vez cómo se creó dicho directorio y los permisos, tal que:

![Permisos](https://i.imgur.com/cYgy3Ou.jpg)

Para trabajar de forma eficiente creamos un espacio de trabajo en la opción > `Add Folder to Workspace...`, puse un nombre por defecto asociado al directorio de **hello-world** y lo guardé con > `Save Workspace As...`. A continuación, creo un fichero dentro del directorio con el nombre de  **tsconfig.json** esto lo hago desde la terminal con el comando `touch`, y le añadimos las líneas:

> `{
>  "compilerOptions": {
>    "target": "ES2018",
>    "outDir": "./dist",
>    "rootDir": "./src",
>    "module": "CommonJS"
>  }
>}`

Con ello configuraríamos cómo se compilaría el código de TypeScript, quedando:

![Crear tsconfig.json](https://i.imgur.com/ncNThAE.jpg)

━━━━━━━━━━━━━━━━━━━━━━━━━━✧❂✧━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━


Procederemos creando otro fichero **index.ts** que será necesario para la implementación del código de "Hola Mundo" a compilar, para que quede organizado y como se especificó en el código anterior del fichero **tsconfig.json**("rootDir": "./src"), quedando:

![Src directorio,index.ts](https://i.imgur.com/3sznxD3.jpg)

Creándose así satisfactoriamente el fichero.

Ahora rellenamos el fichero **index.ts** con el código que imprimirá por pantalla el "Hola Mundo", tal que:

![Código Hola Mundo](https://i.imgur.com/FfHtaAZ.jpg)

Y lo compilamos con el comando > `tsc`, esto compilará el código en un .js que se denotará como **index.js** y que se alojará en el directorio **./dist**, tal y como se especificó en el fichero **tsconfig.json** ("outDir": "./dist"), el directorio dist se crearía sin nosotros haberlo creado manualmente:

![Creacion index.js y directorio ./dist](https://i.imgur.com/5zDEPvR.jpg)

Ahora comprobaremos si entre ambos ficheros existe diferencia y para ello hacemos, con el comando > `diff` :

![Diff comando](https://i.imgur.com/IlkFYJE.jpg)

Analizando la imagen en mi caso detecta diferencia entre en la línea > `let myString: string = "Hola Mundo";` y la línea > `let myString = "Hola Mundo";`. Además, por error mío detecta un error más porque en el fichero **.ts** hay un espacio más al final del código, esto nos da a ver que el comando detecta todo tipo de diferencias, como si es de tener una línea más en blanco:

![diff](https://i.imgur.com/fOSQzk3.jpg)

Una vez que ya tenemos el código compilado sería hora de ejecutarlo con el comando > `node`, quedando de la manera:

![Node](https://i.imgur.com/EZBjxxW.jpg)

━━━━━━━━━━━━━━━━━━━━━━━━━━✧❂✧━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Comprobando así que se ejecuta perfectamente.

Damos por concluída la práctica hacemos un **commit** con el comando: > `git add .` y luego con > `git commit -m` y así guardamos los cambios del proceso. Por último subimos los cambios con > `git push -u origin master` y así tenerlos en el repositorio GitHub.


▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂


## DESARROLLO DEL INFORME CON GITHUB PAGES


Tras finalizar la práctica se nos requiere un informe en con el formato de estilos de Markdown en **GitHub Pages**, para ello usamos la guía de estilos de Markdown en [Markdown guide](https://guides.github.com/features/mastering-markdown/).

Y así finalizamos esta práctica e informe redactado en el archivo **index.md** dentro de la rama **gh_pages**.





▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂

## CONCLUSIONES


Conclusión sobre la práctica e informe, aquí plantearé la dinámica de la práctica y posibles dudas que me hayan surgido y solucionado. La práctica en sí la hice sin dificultad al igual que el informe pues ya en la práctica 1, me familiaricé con la herramienta de GitHub Pages.

▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂

## BIBLIOGRAFÍA Y/O WEBGRAFÍA


- https://ull-esit-inf-dsi-2021.github.io/prct02-vscode/
