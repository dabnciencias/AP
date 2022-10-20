# AP
Repositorio de mi curso (tentativo) de Animación Programática en la Facultad de Ciencias (UNAM).

![](https://github.com/dabnciencias/AP/blob/main/AP_2023-I.gif)

## ¿Cómo puedo ejecutar los _notebooks_ del curso desde mi computadora?

Para poder ejecutar los _notebooks_ localmente en tu computadora es necesario instalar [Python](https://www.python.org/), [Jupyter](https://jupyter.org/), [Git](https://git-scm.com/doc), [IPython](https://ipython.org/) y  [Manim](https://www.manim.community/):
* **Python** es el lenguaje que usaremos para programar nuestras animaciones,
* **Jupyter** es un entorno cómodo para aprender a programar con el cual podremos abrir los _notebooks_ de Jupyter del repositorio (archivos con formato `.ipynb`),
* **Git** nos servirá para "clonar" (es decir, descargar) el repositorio y actualizarlo cuando sea necesario (en el caso particular de sistemas operativos basados en Arch Linux, también nos ayudará a poder instalar los programas anteriores),
* **IPython** nos permitirá ejecutar código de Python en los _notebooks_ de Jupyter y 
* **Manim** es la librería de Python con la cual generaremos nuestras animaciones.

A continuación, detallamos los pasos que debes seguir en distintos sistemas operativos para poder ejecutar los _notebooks_ del curso localmente en tu computadora. 

**Si utilizas alguna otra distribución de Linux u otro sistema operativo distinto a los mencionados a continuación y necesitas soporte, contacta al profesor o al ayudante.**

### GNU/Linux y MacOS

#### Instalar Python, Jupyter, Git y IPython...

* **...en distribuciones basadas en Debian** ([Mint](https://linuxmint.com/)/[Ubuntu](https://ubuntu.com/)/[Debian](https://www.debian.org/))
1. Abre una terminal virtual y actualiza las bases de datos de paquetes de Debian con el administrador de paquetes [Aptitude](https://wiki.debian.org/Aptitude) ejecutando el comando `sudo apt update && sudo apt -y upgrade`.
1. Instala `python3` y `git` con el comando `sudo apt-get install python3 git`.
1. Para instalar `jupyter` y `ipython`, instala primero `pip` con el comando `apt-get install python3-pip python3-dev -y`; después de que haya terminado, ejecuta el comando `pip install jupyter ipython`.

**Nota**
* No es posible actualizar versiones de Python2 a Python3, pues en realidad son lenguajes de programación distintos; por ende, aunque ya tengas instalado Python2, tendrás que instalar Python3 para poder instalar Jupyter.
* Si tu computadora tiene [ChromeOS](https://www.google.com/chromebook/chrome-os/), puedes [activar las opciones de desarrollador](https://www.androidauthority.com/how-to-enable-developer-mode-on-a-chromebook-906688/) y luego [activar Linux](https://support.google.com/chromebook/answer/9145439?hl=en). De esta manera, una vez que tengas acceso a una terminal virtual de Linux, podrás seguir las instrucciones para distribuciones basadas en Debian para instalar Python, Jupyter y Git.

* **...en distribuciones basadas en Arch** ([Manjaro](https://manjaro.org/)/[Endeavour](https://endeavouros.com/)/[Arch](https://archlinux.org/))
1. Abre una terminal virtual y actualiza las bases de datos de paquetes de Arch con el administrador de paquetes [`pacman`](https://wiki.archlinux.org/title/Pacman) ejecutando el comando `sudo pacman -Syyu` **antes de instalar cualquier cosa**.
1. Instala `python`, `jupyter-notebook` y `git` con el comando `sudo pacman -S python jupyter-notebook git`.
1. Para instalar `ipython`, instala primero `pip` con el comando `sudo pacman -S python3-pip`; después de que haya terminado, ejecuta el comando `pip install ipython`.

* **...en MacOS**
1. Abre una terminal e instala el administrador de paquetes [hombrew](https://brew.sh/) ejecutando el comando `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`.
1. Instala `python`, `jupyter` y `git` con el comando `brew install python jupyter git`.
1. Para instalar `ipython`, ejecuta el comando `pip install ipython` (deberás haber realizado el paso previo anteriormente).

#### Decargar y actualizar actualizar el repositorio del curso (para cualquier distribución GNU/Linux y MacOS)

1. Para descargar todo el repositorio (en su forma actual) a la carpeta "home" de tu computadora, abre una terminal virtual y ejecuta los comandos `cd ~` y después `git clone https://github.com/dabnciencias/AP`. Esto creará una carpeta `AP` con todos los contenidos del repositorio.
1. Para más adelante actualizar el repositorio (a como se encuentra en esta página de GitHub), abre una terminal virtual y ejecuta los comandos `cd ~/AP` y después `git pull`.

#### Ejecutar _notebooks_ localmente (para cualquier distribución GNU/Linux y MacOS)

1. Para ejecutar _notebooks_ de Jupyter (archivos del repositorio con formato .ipynb) localmente, abre una terminal virtual y ejecuta el comando `jupyter-notebook`.

### Windows

#### Instalar Python y Jupyter...

1. Instala Python3 utilizando el instalador desde su página oficial descargando el [siguiente archivo](https://www.python.org/ftp/python/3.10.2/python-3.10.2-amd64.exe).
1. **Al instalar asegurate de marcar la casilla 'Add Python 3 to PATH'.**
1. Da click en la aplicación de Power Shell para abrir una terminal virtual en Windows.
1. Utiliza pip para instalar `jupyter` copiando y pegando el siguiente comando en tu terminal de PowerShell: `python -m pip install jupyter`.
1. Para abrir un notebook de Jupyter utiliza el siguiente comando en la terminal de PowerShell: `jupyter notebook` y espera a que se abra una ventana emergente en tu navegador.
1. Para terminar la sesión de Jupyter, cierra la ventana correspondiente de tu navegador y usa `Ctrl-C` dos veces en la terminal de PowerShell para terminar el proceso.

#### Instalar Git y GitHub Desktop...

1. Crea una cuenta en la [página oficial de GitHub](https://github.com) usando tu correo @ciencias.
1. Descarga GitHub Desktop desde la [página oficial](https://desktop.github.com/).

#### Decargar y actualizar actualizar el repositorio del curso (para cualquier distribución GNU/Linux y MacOS)

1. Inicia GitHub Desktop dando click en el icono que se haya creado en tu escritorio y vincula tu sesión con la cuenta que acabas de crear.
1. Para clonar el repositorio del curso en tu computadora da click en el botón 'Clonar un repositorio de internet', selecciona la pestaña correspondiente a 'URL', copia y pega la siguiente liga: `https://github.com/dabnciencias/AP` y determina la ubicación en la que quieres que se guarde el repositorio en el campo 'Local path' (puedes dejar ese campo con el valor predeterminado). Da click en el botón 'Clone' y espera a que se complete la carga, una vez que haya terminado podrás encontrar los archivos del repositorio en la ubicación que hayas determinado en el 'Local path'. Para una explicación más detallada visita la [siguiente página](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/adding-and-cloning-repositories/cloning-a-repository-from-github-to-github-desktop).

### Instalación de Manim (para cualquier sistema operativo)

Una vez que tengas instalado Python, Jupyter, Git y IPython, y hayas clonado el repositorio del curso en tu computadora, ¡abre el _notebook_ `1.1-Instalación_y_uso_básico_de_Manim.ipynb` de la carpeta `1-Introducción_a_Manim` y sigue las instrucciones para empezar a crear animaciones programáticas!

### Alternativas para cualquier sistema operativo

1. Google Colab  

Si no cuentas con una computadora personal o tu computadora no tiene los recursos suficientes para soportar la instalación, puedes usar Google Colab como alternativa.  
Google Colab es un servicio que ofrece notebooks de Jupyter de manera gratuita con recursos de cómputo totalmente gestionados en la nube sin necesidad de instalar nada en tu computadora local.  
Los _notebooks_ están desarrollados para ejecutar en Python por de forma predeterminada.
Para utilizarlo, ve directamente a la [página oficial de Google Colab](https://colab.research.google.com/), una vez allí verás un recuadro que te pedirá seleccionar un archivo para abrir, selecciona la ventana Google Drive y da click en 'New notebook' para crear un notebook en blanco. Nota: Los archivos que crees de esta manera se almacenarán en una carpeta llamada 'Colab Notebooks' en la página principal de tu carpeta de Google Drive.

También puedes abrir los notebooks del repositorio del curso yendo a la pestaña de 'GitHub', copiando y pegando la siguiente liga `https://github.com/dabnciencias/AC.git` y seleccionando el archivo que quieras abrir.  

1. Anaconda  

Una forma más sencilla (pero menos recomendada por el peso de descarga) para hacer la instalación es utilizando Anaconda Navigator.
Puedes descargar Anaconda directamente desde [su página web](https://www.anaconda.com/products/individual). Si decides utilizar esta opción de descarga y necesitas soporte, contacta directamente al ayudante del curso.
