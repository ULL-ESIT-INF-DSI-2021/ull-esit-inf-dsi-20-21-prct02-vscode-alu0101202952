

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





▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂


## DESARROLLO DEL INFORME CON GITHUB PAGES


Tras finalizar la práctica se nos requiere un informe en con el formato de estilos de Markdown en **GitHub Pages**, para ello me familiaricé e informé tras búsquedas en la página oficial, otros sitios web y visualizaciones de vídeos. Podemos ver la guía de estilos de Markdown en [Markdown guide](https://guides.github.com/features/mastering-markdown/).

Tras saber, por diversas fuentes, cómo elaborar un informe en GitHub Pages llegué a:
Primero para clasificar mejor la parte del informe de la práctica cree una rama nueva llamada **gh_pages** en mi repositorio y un archivo _.md_ denominado **index.md**, también me surgió una duda, que plantearé en el apartado **"CONCLUSIONES"**:
『』[Rama informe gh_pages](https://drive.google.com/file/d/163x2QqzIxu7RmCQzYU5a3cijoz7HLrrS/view)

Con ello tendría el fichero donde elaboraría el informe, pero quiero vincularlo con la herramienta de presentación de GitHub Pages, para ello seguí los siguientes pasos:
1. Ir al apartado _Settings_ esto en el repositorio, y luego en _Options_ llegar hasta casi el final de dicha página, al subapartado _GitHub Pages_.
『』[Settings](https://drive.google.com/file/d/1F1tNIh8Wlz8B28wRuKkbALoN5NbM9NWo/view)
『』[Options](https://drive.google.com/file/d/1Dj_RaJHyn8KT4tpeUUVKQ8fl-obRoeTK/view)

2. **Paso previo** Se debe ejecutar este paso antes, porque si no saltaría un _warning_ debido a la privacidad del repositorio, para ello llegamos al final de la página de _Options_ donde pone _Danger Zone_ y cambiamos la privacidad de **Privada** a **Pública**:
『』[Cambiar visibilidad](https://drive.google.com/file/d/19mlsWJBR7iufx1CspcS89cf30N9qU1Bh/view)

3. Ahora ya con la visibilidad en pública podemos ir al subapartado _GitHub Pages_ antes nombrado y decidir la rama por **gh_pages** donde se encuentra el index.md que contendrá el informe con el que trabajaremos:
『』[GitHub Pages rama](https://drive.google.com/file/d/1Dj_RaJHyn8KT4tpeUUVKQ8fl-obRoeTK/view)

4. Luego en el apartado _Change Theme_ podremos cambiar el tema de fondo con el que se presentará el informe, al aplicar todo, en la parte de arriba se crea un nuevo enlace al informe, dicho enlace se subirá a la tarea dedicada a esta práctica.
『』[Cambiar tema y enlace del informe](https://drive.google.com/file/d/1pZ0Ugz-CtyTPXga6kdyy_MTIGh3hvHaT/view)

Y así finalizamos esta práctica e informe redactado en el archivo **index.md** dentro de la rama **gh_pages**.





▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂

## CONCLUSIONES


Conclusión sobre la práctica e informe, aquí plantearé la dinámica de la práctica y posibles dudas que me hayan surgido y solucionado. La práctica en sí pude hacerla sin dificultades. Sin embargo, a la hora de hacer el informe como nunca antes había usado la herramienta GitHub Pages, tuve que informarme y en varias fuentes me indicaban algo distinto del formato del fichero donde hacer el informe. Esto es debido a que algunos usuarios realizaban los informes o páginas web en formato HTML y muy pocos en formatos .md, pero me di cuenta con la guía de estilos de **Markdown** que muchas herramientas como etiquetas, etc. de HTML eran sustituídas por ejemplo, los tamaños de las cabeceras 

**h1 = #** 
**h2 = ##** etc.

Y aunque muchos trabajasen en HTML y al principio lo intentase con este informe, al final me di cuenta que en .md resulta más legible y conciso, además de ser el formato que aparece en algunas páginas oficiales. Pero de resto, a medida que investigaba conseguía saberme desenvolver algo mejor con la herramienta.


▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂▂

## BIBLIOGRAFÍA Y/O WEBGRAFÍA


- https://pages.github.com/
- https://github.com/cristinafsanz/github-pages
- https://docs.github.com/en/github/working-with-github-pages
- https://developer.mozilla.org/es/docs/Learn/Using_Github_pages
- https://www.youtube.com/watch?v=QaxgF4v4hms
- https://devcode.la/tutoriales/publicar-tu-web-usando-github-pages/
- https://docs.github.com/es/github/writing-on-github/basic-writing-and-formatting-syntax
- https://parzibyte.me/blog/2019/01/17/agregar-imagenes-github-readme-otras-paginas/
- https://guides.github.com/features/mastering-markdown/
- https://docs.github.com/es/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll
