# ETHICAL-HACKER-WORK-ENVIRONMENT-V2-2022
![escritorio](https://user-images.githubusercontent.com/97669969/154135658-14dbc059-6d51-431a-8be9-abae4d4b1dbd.jpg)
![escritorio principal](https://user-images.githubusercontent.com/97669969/154135668-40fbe59e-060f-4f59-81ef-88f8f543fcde.jpg)
![rofi](https://user-images.githubusercontent.com/97669969/154135680-d692ff29-1033-4e3b-ad8f-b23f578a2bde.jpg)
![win s](https://user-images.githubusercontent.com/97669969/154135687-840f0247-0c8c-46ca-b1bd-f633c98db218.jpg)
![lsdbatranger](https://user-images.githubusercontent.com/97669969/154135696-80cc23de-aca6-4eeb-87fe-0e21300441e1.jpg)
![brave](https://user-images.githubusercontent.com/97669969/154135723-0d596034-a27c-4a36-bf1e-1c80e5b8050c.jpg)

#En primer lugar instalate estas librerias :

  >sudo apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev  libpcre2-dev  libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev

  >sudo apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev libxcb-keysyms1-dev libxcb-xinerama0-dev libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev

  >sudo apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev  libpcre2-dev  libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev

  >sudo apt install bison flex libstartup-notification0-dev check autotools-dev libpango1.0-dev librsvg2-bin librsvg2-dev libcairo2-dev libglib2.0-dev libxkbcommon-dev libxkbcommon-x11-dev libjpeg-dev

 >sudo apt install slim libpam0g-dev libxrandr-dev libfreetype6-dev libimlib2-dev libxft-dev
 

 #Vamos a proceder con la instalacion, todo lo vamos a hacer sobre la carpeta cd ~/Downloads o ~/Descargas :

-sudo apt update
-sudo apt update
-sudo parrot-upgrade   
  -(solo si estas en parrot)

#Instalamos bspwm :

-sudo apt install bspwm   (en dir /HOME)
-cd ~/Downloads
-git clone https://github.com/baskerville/bspwm.git
-cd bspwm
  -make
  -sudo make install
  -Copy/mkdir toda la conf. a sus correspondientes carpetas:

  -mkdir ~/.config/bspwm
  -cp examples/bspwmrc ~/.config/bspwm
  -chmod +x ~/.config/bspwm/bspwmrc
  -cd ..

ABRE : vim o nano ~/.config/bspwm/bspwmrc   (ESTE ES EL CEREBRO,NUESTRO GESTOR,RECUERDA ESTE DIRECTORIO)

Instalamos sxhkd (Gestor de shortcuts hermano de bspwm, por decir): 
 
git clone https://github.com/baskerville/sxhkd.git
cd sxhkd
  make
  sudo make install

Copy/mkdir conf. a sus correspondientes dir/ :

 mkdir ~/.config/sxhkd
  cp ../bspwm/examples/sxhkdrc ~/.config/sxhkd
  cd ..

MUY IMPORTANTE ,NO REINICIAS TU SISTEMA AUN....; ABRE NANO/VIM   vim ~/.config/sxhkd/sxhkdrc Y CONFIGURA LOS SHORTCUTS, A TU PREFERENCIA, EN EL REPO SXHKDRC ESTA LOS MIOS,ECHA UN VISTAZO , POR EX YO ABRO LA TERMINAL ASI GNOME PUEDE SER REEMPLAZADO POR TU TERMINAL PREFERENTE :
# terminal emulator
super + Return
    gnome-terminal

Instalamos polybar ;

En primer lugar para evitar errores de fonts/ descarga e instala las Hack Nerd Fonts, abre firefox/ y desde nerdfonts.com descargas esta fuente.(si no te gusta hack nerd, puedes buscar por Iosevka, ubuntu mono..etc)

  git clone --recursive https://github.com/polybar/polybar
 cd polybar
  mkdir build
  cd build
  cmake ..
  make -j$(nproc)
  sudo make install


----(IMPORTANTE -si tienes el error comun de cmake .. con CMakeLists.txt? o alguna error que desconozcas>> instala estas librerias : ---------------------
sudo apt update

sudo apt install libxcb-xkb-dev libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev i3-wm libjsoncpp-dev libmpdclient-dev libcurl4-openssl-dev libnl-genl-3-dev

sudo apt install build-essential git cmake cmake-data pkg-config python3-sphinx python3-packaging libuv1-dev libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev

Ahora estamos listos para reiniciar en bspwm , fijate en la pantalla de reinicio y elegir bien bspwm , porque por defecto viene tambien i3w (otro gestor de ventanas...) .

No te asustes por la pantalla negra, por arriba veras la polybar (algunas veces se instala por defecto la vieja polybar/release), si configuratse bien los shortcuts,
   con WIN_+ RETURN  tecla de windows seria ENTER , iniciamos nustra terminal gnome,alacritty..etc.

Instalamos el tema de polybar desde este repo :

git clone https://github.com/VaughnValle/blue-sky.git
 
Ejecuta /copy/paste... los siguientes comandos:
 
mkdir ~/.config/polybar
cd ~/Descargas/blue-sky/polybar/
cp * -r ~/.config/polybar
echo '~/.config/polybar/./launch.sh' >> ~/.config/bspwm/bspwmrc 
cd fonts
sudo cp * /usr/share/fonts/truetype/
fc-cache -v

WIN+SHIFT+R Y LA POLYBAR ESTA POR ARRIBA.listo.


Instalamos rofi :

sudo apt install rofi

Asegurate de tener este shortcur en cd~/.config/sxhkd/sxhkdrc  , abre sxhkdrc cobn nano o vim : 
# program launcher
super + d
    rofi -show run
 
Tema nord para rofi :
cd 
mkdir -p ~/.config/rofi/themes
cd Descargas / Downloads ...
cp ~/Descargas/blue-sky/nord.rasi ~/.config/rofi/themes   (blue-sky lo hemos clonado mas arriba si recuerdas, ahi esta el tema nord, viene dentro del repo..)

WIN_+D (si es tu caso..)
escribe : rofi-theme-selector   (abajo del todo esta el tema nord, de igual manera hay cientos de temas tanto en rofi como en github ...)


Instalamos feh :

sudo apt install feh
abres con nano/vim cd ~ /.config/bspwm/bspwmrc y anades esto ;  feh --bg-fill /home/tmcyber/images/fondo.jpg  (reemplaza con tu usuario, e directorios donde tengas la imagen..)


Instalamos picom :

sudo apt update

cd /Descargas / Downloads ..etc
git clone https://github.com/ibhagwan/picom.git
cd picom/
git submodule update --init --recursive
meson --buildtype=release . build
ninja -C build
sudo ninja -C build install

mkdir ~/.config/picom
cp ~/Descargas/blue-sky/picom.conf  ~/.config/picom

::nano o vim abres picom.conf y en mi caso , decomente glx" y comente # “xrender , ”glx tira de grafica entonces es eleccion tuya si queres dejarlo , en mi caso no (todo de glx fuera,comentado)
▪ tambien decomente todo lo relacionado con blurring en las ventanas, si a ti te gusta puedes dejarlo ,,pero gasta recursos.

WIN+AL+R RESETEAMOS LA CONFIGURACION, Y SE DEBERIA APLICAR TRANSPARENCIA, EN ALGUNOS CASOS TARDA UN POCO MAS, ASI QUE PACIENCIA..., o ejecuta un reboot)

 
Instalamos Powerlevel10k ;
 

https://github.com/romkatv/powerlevel10k

O si prefieres, copy/paste y listo!

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc

en tu terminal escribe : zsh y sgiue los pasos.
 
+IMPORTANTE: Para el usuario root debe hacer los mismos pasos.

Aplicamos zsh como nuestra shell por defecto:(es opcional...)

usermod --shell /usr/bin/zsh tmcyber       (seguido de tu usuario)
usermod --shell /usr/bin/zsh root            (para root tambien executas esto)





OPCIONAL + INSTALAMOS BRAVE BROWSER :

+brave es muy seguro 
+rastreadores y bloqueadores incorporados 
+no hace falta agregar extensiones como adblocker o parecidas
+en recursos de sistema tiene muy bajo consumo, menos que firefox.

sudo apt install apt-transport-https curl

sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser

Listo!





OPCIONAL +  MODULOS EN POLYBAR : CREAR MODULOS PARA POLYBAR

(ip, cpu, date, ram, spotify...etc..hay infinidad de modulos que podemos incorporar a nuestro gusto..)

Por ahora anadimos ip_status en mi caso que hago pentest, entoces en todo momento necesito saber mi ip. 

La estructura es la siguente:  (sigue los pasos a pie de letra)

cd /home/.config/
mkdir bin
cd bin
touch ip_status.sh
chmod + ip_status.sh

en ip_status.sh pegas esto :

#!/bin/sh
 
echo "%{F#2495e7} %{F#ffffff}$(/usr/sbin/ifconfig eth0 | grep "inet " | awk '{print $2}')%{u-}"
 
Para el módulo de hackthebox_status.sh:
 
#!/bin/sh
 
IFACE=$(/usr/sbin/ifconfig | grep tun0 | awk '{print $1}' | tr -d ':')
 
if [ "$IFACE" = "tun0" ]; then
    echo "%{F#1bbf3e} %{F#ffffff}$(/usr/sbin/ifconfig tun0 | grep "inet " | awk '{print $2}')%{u-}"
else
    echo "%{F#1bbf3e}%{u-} Disconnected"
fi


Guardas todo bien y sales , ahora :

Te diriges a  cd ~/.config/polybar 
nano/vim current.ini y buscas esto ; [bar/secondary] despues de el pegas esto : 

[bar/terciary]
inherit = bar/main
width = 8%
height = 40
offset-x = 11%
offset-y = 15
background = ${color.bg}
foreground = ${color.white}
bottom = false
padding = 1
;padding-top = 2
module-margin-left = 0
module-margin-right = 0
;modules-left = date sep mpd
modules-center = ip_status
wm-restack = bspwm


Ahora te diriges al final de todo ,,,y pegas esto :

[module/ip_status]
type = custom/script
interval = 2
exec = ~/.config/bin/ip_status.sh

bajas un poco el modulo sysmenu y pegas el modulo nuestro , ip_status primero y sysmenu secundo ..no invades territorio de ningun modulo.

IMPORTANTE : NO HAGAS CAMBIOS SI NO SABES LO QUE HACES, O DESCONOCES el lenguaje, PRIMERO INVESTIGA.te puedes quedar sin barra.




Arreglo de cursor X : en cd ~/.config/bspwm abres nano/vim bspwmrc y pegas esto : xsetroot -cursor_name left_ptr &





INSTALAMOS RANGER :

sudo apt install ranger
ranger ..en tu terminal (veras la diferencia)


INSTALAMNOS LSD :

https://github.com/Peltoche/lsd/releases

INSTALAMOS BAT :

https://github.com/sharkdp/bat/releases


    IRE ACTUALIZANDO EL REPO. SEGUN ACTUALIZE Y ANADE MAS COSAS INTERESANTES, PARA HACER NUESTRA VIDA MAS FACIL~! hackMODE
