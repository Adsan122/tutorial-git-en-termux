#TUTORIAL DE COMO INSTALAR GIT EN TERMUX

## INSTALACION DE TERMUX

Para la instalacion de termux se puede desde git en [`termux relases`](https://github.com/termux/termux-app/releases)<br>
para instalar la ultima version ya que desde la playstore esta en la version 0.101.

## INSTALACION DE GIT EN TERMUX

Para instalar se colocara el comando `pkg install git` o `apt install git` y comenzara a instalar

**Ya esta instalado git en termux**

## NAVEGAR ENTRE CARPETAS TERMUX

*La ruta predeterminada de termux es `data\data\com.termux\files\home`*.<br>
para usar la tarjeta externa o la memoria del telefono debes usar el comando `Termux-setup-storage` a pedir permisos que use la sd desde la confiracion de la app.
ya concedido el perimso podemos movernos con:<br>
 `cd ..` para ir a la carpeta anterior.
`cd ejemplo` para movernos a la carpeta que queremos.
`ls` para mostrar las carpetas y archivos que hay en la ruta.
`mkdir ejemplo` para crear una carpeta.
`rm` para quitar un archivo `rm archivo.txt`o  quitar carpeta `rm -r carpeta/`.
`cd $home` para ir a la ruta prederterminada de termux.
<br>
Cuando se usa `termux-setup-storage` se crea la carpeta `/storage` en `data/data/com.termux/files/home/`.<br>
*esa carpeta solomente sera un acceso directo.*
LA CARPETA SE ENCUENTRA EN `storage/emulated/0`.
**NO PUEDES VER NI CREAR EN LA CARPETA DE RAIZ YA QUE NO TIENES PERMISOS POR ROOT**

## CREAR CARPETA PARA EL REPOSITORIO

*SI CREAS UN REPOSITORIO EN HOME TU EXPLORADOR DE ARCHIVOS NO LO PODRA VERLOS YA QUE ESTA RUTA ESTA OCULTA*
*SI CREAS EL REPOSITORIO EN `data/data/com.termux/files/home/storage` o en `storage/emulated/0/` tu explorador si podra verlos*<br>
*listo en la ruta de preferencia crearé una carpeta 'githup' para mis repositorios.
*luego creare el repositorio.
*EJEMPLO*
`mkdir github` para crear una carpeta en este caso aqui guardare los repositorios.
`cd github` para ingresar a la carpeta.
`mkdir tutorial-git-en-termux` este el nombre de la carpeta del repositorio.
`cd tutorial-git-en-termux` para ingresar a la carpeta.

### CREAR REPOSITORIO

### iniciar repositorio local
`git init` esto creara una carpeta .git que indicara que es un repositorio local.
*la carpeta .git no se debe manipular si la borramos ya no sera un repositorio*<br>

### iniciar repositorio en la nube 
`git clone https://ejemplo.com` esto descargara el repositorio en la ruta donde estemos
*creara la carpeta del repositorio e incia el git init*

## Creacion de archivo

en este caso inciaremos con un repositorio local el cual esta vacio
crearemos un archivo.

termux trae integrado en editor de codigo llamado `nano` `pkg update nano` para actualizarlo.
en git de escritorio se descarga un editor llamado `vim` para descargarlo `pkg install vim`.
para crear un archivo es :<br>
`nano archivoNano.txt` este para crear un archivo con nano o ingresar si existe.
`vi archivovim.txt` este para crear un archivo con vim o ingresar si existe.

con nano aparece las opciones de ayuda que funcionan con CTRL mas la letra.
con vim para ingresar datos escribimos "i" de ingresar.
para salir del modo ingresar de vim pulsamos "ESC".
para salir del editor vim despues de pulsar "ESC" escribimos `:wq` para guardar y salir.
para salir sin guardar `:q!`

## WORKING AREA O AREA DE TRABAJO

`git add README.md` con un editor se creo el archivo "README.md".
*GIT ADD es para decirle a git que estamos trabajando en un archivo*
`git status` para mirar si el archivo con el que usaste `git add` esta modificado.
cuando hallas terminado de editar usaras `git add` ahora`git status` no te lo resaltara
tenemos un archivo en el que estamos editando esto es lo que se le llama "area de trabajo"

### STAGIN AREA o AREA DE PREPARACION

El commando `git commit -m "comentario"` es para hacer una captura o un registro que se guardara en el historial del codigo en git.<br>
Para usar `git commit` debemos mirar el `git status` ya que puedes haber editado un archivo o borrado.
si quieres guardar esa captura de los archivos que has modificado entonces `git add .` o lo puedes hacer uno por uno.
despues de guardar todos los cambios `git add` entoces procedes hacer el `git commit` con su comentario para especificar que hicistes alli.

## REPOSITORIO EN LA NUBE

Los commit todo se guarda de manera local y no trabajas directamente en la nube.

### SUBIR REPOSITORIO LOCAL

para subir el repositorio local se usa el comando `git push`

para hello te pedira el usuario contraseña y email.

entonces configuras
`git -config user.name ejemplo`. este es para el usuario.
`git -config user.email ejemplo.ejemplo` este es para el email de la cuenta

##### contraseña en git
`git -config user.password ejemplotoken`

para el enlace lo debes hacer con un token.
para ello debes ir al navegador entras a tu cuenga github
-ves a las configuraciones `setting`
'en la parte desarrollador `<>Developer settings` 
-ves a `personal access token`
- pulsa `generate new toquen` le pones el titulo, le pones la duracion, activa la casilla repo y `generate token` copias la contraseña y la pegas
*se usa en termux de este modo ya que la otra auntentificacion no es permitida*
# tutorial-git-en-termux
