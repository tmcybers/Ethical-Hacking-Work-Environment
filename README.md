 # TMCyber 
   #ETHICAL HACKER | CEH | PYTHON IA|ML | |Bug Bounty|Researcher|

# Gnome Terminal + Powerlevel10K + Feh + Polybar 
![escritorio](https://user-images.githubusercontent.com/97669969/154135658-14dbc059-6d51-431a-8be9-abae4d4b1dbd.jpg)

# Powerlevel10K + Feh + Polybar 
![escritorio principal](https://user-images.githubusercontent.com/97669969/154135668-40fbe59e-060f-4f59-81ef-88f8f543fcde.jpg)

# Rofi Nord Theme
![rofi](https://user-images.githubusercontent.com/97669969/154135680-d692ff29-1033-4e3b-ad8f-b23f578a2bde.jpg)

# Brave + Flotant Terminal 
![win s](https://user-images.githubusercontent.com/97669969/154135687-840f0247-0c8c-46ca-b1bd-f633c98db218.jpg)

# Lsd , Bat , Ranger
![lsdbatranger](https://user-images.githubusercontent.com/97669969/154135696-80cc23de-aca6-4eeb-87fe-0e21300441e1.jpg)

# Brave
![brave](https://user-images.githubusercontent.com/97669969/154135723-0d596034-a27c-4a36-bf1e-1c80e5b8050c.jpg)

              

## MUY IMPORTANTE : 

* Configura y haz la instalacion en una maquina virtual, o clona la maquina.
* Solo en el caso de no tener experiencia con gestores de ventanas y sus previas configuraciones.

## PRESTA ATENCION, A LOS PASOS A SEGUIR, NO HAGAS NADA CON USUARIO ROOT, USA TU USUARIO HABITUAL / O CREAA UNO NUEVO COMO TU CREEAS CONVENIENTE.
* SOLO EN EL CASO DE QUE HAGA FALTA Y SE ESPECIFICA TAL CASO SE USA SUDO.
* LOS COMNANDOS ESTAN PREPARADOS PARA COPY/PASTE I LISTO, HAY CASOS EN DONDE TENDRAS QUE ESPECIFICAR TU USUARIOS POR SUSPUESTO, O CAMBIAR ALGUNOS DIRECTORIOS.
* LA MAYORIA DE LAS INSTALACIONES/CLONES SE HACEN EN /DESCARGAS / DOWNLOADS PERO SE DA EL CASO QUE TENDRAS QUE HACERLO EN /HOME.ATENTO A LOS PASOS.

** Instalacion hecha sobre : Parrot OS 4.11.3 2022.



### En primer lugar instalate estas librerias :

-  sudo apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev  libpcre2-dev  libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev

-  sudo apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev libxcb-keysyms1-dev libxcb-xinerama0-dev libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev

- sudo apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev  libpcre2-dev  libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev

-   sudo apt install bison flex libstartup-notification0-dev check autotools-dev libpango1.0-dev librsvg2-bin librsvg2-dev libcairo2-dev libglib2.0-dev libxkbcommon-dev libxkbcommon-x11-dev libjpeg-dev

- sudo apt install slim libpam0g-dev libxrandr-dev libfreetype6-dev libimlib2-dev libxft-dev



##  Vamos a proceder con la instalacion, todo lo vamos a hacer sobre la carpeta cd ~/Downloads o ~/Descargas 

* sudo apt update
* sudo parrot-upgrade   (solo si estas en parrot)

# Instalamos bspwm :
```bash
# sudo apt install bspwm   
# cd ~/Downloads
$ git clone https://github.com/baskerville/bspwm.git
# cd bspwm
$ make
$ sudo make install
```
# Copiamos toda la .config a sus correspondientes carpetas:

```bash
# mkdir ~/.config/bspwm
# cp examples/bspwmrc ~/.config/bspwm
# chmod +x ~/.config/bspwm/bspwmrc
# cd ..
```

# ESTE ES EL CEREBRO, NUESTRO GESTOR, RECUERDA ESTE DIRECTORIO.

* ~/.config/bspwm/bspwmrc
  
# Instalamos sxhkd:

```bash
# cd Downloads
$ git clone https://github.com/baskerville/sxhkd.git
# cd sxhkd
  # make
  # sudo make install
```

# Copiamos toda la .config a sus correspondientes dir

```bash
$ mkdir ~/.config/sxhkd
# cp ~/Downloads/bspwm/examples/sxhkdrc ~/.config/sxhkd
# cd ..
```

# abre con nano/vim    

```bash
 $ nano ~/.config/sxhkd/sxhkdrc 
```

# Configura tus shortcuts y recuerdalos, escribelos en algun sitio, por ex uno importante es abrir tu terminal gnome, alacritty, etc.

```bash
# terminal emulator
super + Return
    gnome-terminal
```

# Instalamos polybar
```bash
$ git clone --recursive https://github.com/polybar/polybar
# cd polybar
# mkdir build
# cd build
# cmake ..
# make -j$(nproc)
# sudo make install
```

# IMPORTANTE -si tienes el error comun de cmake .. con CMakeLists.txt? o alguna error que desconozcas>> instala estas librerias:

* sudo apt install libxcb-xkb-dev libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev i3-wm libjsoncpp-dev libmpdclient-dev libcurl4-openssl-dev libnl-genl-3-dev

* sudo apt install build-essential git cmake cmake-data pkg-config python3-sphinx python3-packaging libuv1-dev libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev

* sudo apt update

# Ahora estamos listos para reiniciar en bspwm , fijate en la pantalla de reinicio y elegir bien bspwm , porque por defecto viene tambien i3 (otro gestor de ventanas)
* No te asustes por la pantalla negra, por arriba veras la polybar (algunas veces se instala por defecto la vieja polybar/release), si configuraste bien los shortcuts,
   con WIN+RETURN tecla de windows seria ENTER , iniciamos nuestra terminal gnome, alacritty.etc.


# Instalamos el tema de polybar 

```bash
# cd Downloads
$ git clone https://github.com/VaughnValle/blue-sky.git
```

   # Ejecuta /copy/paste de los siguientes comandos, uno por uno:

```bash
# mkdir ~/.config/polybar
# cd ~/Downloads/blue-sky/polybar/
# cp * -r ~/.config/polybar
# echo '~/.config/polybar/./launch.sh' >> ~/.config/bspwm/bspwmrc 
# cd fonts
# sudo cp * /usr/share/fonts/truetype/
# fc-cache -v
```
   # WIN+SHIFT+R actualizamos el gestor, y veras la polybar por arriba.


# Instalamos rofi 

```bash
# sudo apt install rofi
```

# Asegurate de tener este shortcut en cd~/.config/sxhkd/sxhkdrc  , abre sxhkdrc con nano o vim : 

```bash
# program launcher
super + d
    rofi -show run
```

# Tema Nord para Rofi

```bash
# cd 
# mkdir -p ~/.config/rofi/themes
# cd Downloads 
# cp ~/Descargas/blue-sky/nord.rasi ~/.config/rofi/themes   
```
      # blue-sky lo hemos clonado mas arriba si recuerdas, ahi esta el tema nord, viene dentro del repo.

   # WIN_+D (si es tu caso)
    # Escribe : rofi-theme-selector , abajo del todo esta el tema nord.



# Instalamos feh 

```bash
sudo apt install feh
```
#nano o vim bspwmrc

```bash
cd ~ /.config/bspwm/bspwmrc 
 ```

# Añades esto dentro : 

```bash
feh --bg-fill /home/tmcyber/images/fondo.jpg  
    #(reemplaza con tu usuario, e directorios donde tengas la imagen..)
```

# Instalamos picom 

```bash
# sudo apt update
# cd Downloads 
$ git clone https://github.com/ibhagwan/picom.git
# cd picom/
# git submodule update --init --recursive
# meson --buildtype=release . build
# ninja -C build
# sudo ninja -C build install

# mkdir ~/.config/picom
# cp ~/Downloads/blue-sky/picom.conf  ~/.config/picom

```

    # nano o vim abres picom.conf y en mi caso , decomente glx" y comente # “xrender , ”glx tira de grafica entonces es eleccion tuya si queres dejarlo , en mi caso no (todo de glx fuera,comentado)
    # tambien decomente todo lo relacionado con blurring en las ventanas, si a ti te gusta puedes dejarlo ,,pero gasta recursos.

# WIN+AL+R reseteamos todo el gestor, y se deberia aplicar transparencia, en algunos casos suele tardar, paciencia, o si no sudo reboot y listo.


# Instalamos Powerlevel10k 

```bash
$ git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
```

   # En tu terminal escribe : zsh y sigue los pasos
   # IMPORTANTE: Para el usuario root debe hacer los mismos pasos.

  # Aplicamos zsh como nuestra shell por defecto 
   # es opcional, puedes seguir con bash o cualquier otra, pero zsh para mi es la mejor'

```bash
# usermod --shell /usr/bin/zsh tmcyber       (seguido de tu usuario)
# usermod --shell /usr/bin/zsh root            (para root tambien executas esto)
```

# Instalamos Brave Browser
  
  # brave es muy seguro 
  # rastreadores y bloqueadores incorporados 
  # no hace falta agregar extensiones como adblocker o parecidas
  # en recursos de sistema tiene muy bajo consumo, menos que firefox.

```bash
# sudo apt install apt-transport-https curl
# sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg
# echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list
# sudo apt update
# sudo apt install brave-browser
```


# Modulos en Polybar : 
     # Tuneamos Polybar ! ~
   ## HackMODE ON ~!
   
   #Por ahora añadimos ip_status en mi caso hago pentest a diario, entoces en todo momento necesito saber mi ip. 

# La estructura es la siguente:  
    
    # sigue los pasos a pie de letra

```bash
# cd /home/.config/
# mkdir bin
# cd bin
# touch ip_status.sh
# chmod + ip_status.sh
```

# En ip_status.sh pegas esto :

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


     # Guardas todo bien y sales.

# Te diriges a : cd ~/.config/polybar 
    
   # nano/vim current.ini y buscas esto ; [bar/secondary] despues de el pegas esto : 

```bash 
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
```

  # Ahora te diriges al final de todo, y pegas esto :

```bashh
[module/ip_status]
type = custom/script
interval = 2
exec = ~/.config/bin/ip_status.sh
```
    # bajas un poco el modulo sysmenu y pegas el modulo nuestro , ip_status primero y sysmenu secundo ..no invades territorio de ningun modulo.

   # IMPORTANTE : no hagas cambios si desconoces el leguaje / estructura.


# Arreglo de cursor X 

```bash
 cd ~/.config/bspwm 
```
  
Nano/Vim abres bspwmrc y pegas esto : 

```bash
# xsetroot -cursor_name left_ptr &
```


# Instalamos Ranger

```bash 
# sudo apt install ranger
# ranger 
```
    # en tu terminal (veras la diferencia)


# Instalamos Lsd

```bash
$ https://github.com/Peltoche/lsd/releases
```
      #ls vs lsd -l (prueba y veras)


# Instalamos Bat

```bash
$ https://github.com/sharkdp/bat/releases
```
    #cat vs bat (prueba y veras)
    

# Ire actualizando el repo semanal o mensual segun añade mas configs y modulos ~! 

 ## !~HackMODE On~!
#TMCYber 


