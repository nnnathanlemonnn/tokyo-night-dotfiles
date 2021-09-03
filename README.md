# Tokyo Night Dotfiles
## description:
> a simple dark theme rice configuration for linux

- clone this repository

```
https://github.com/nnnathanlemonnn/tokyo-night-dotfiles.git
```
## visuals
![gif](assets/preview.gif)
### what's on the preview?
#### rofi 
> A window switcher, application launcher and dmenu replacement
> Custom Rofi theme.. based on: 
##### Qball's dmenu rofi theme
> ![rofi](assets/rofidark10.png)
##### adi1090x powermenu
> ![powermenu](assets/rofipowmen10dark.png)
#### tint2
> Basic, good-looking task manager for WMs
>-	 Custom made tint2 bar
 ![tint2](assets/tint2.png)	 
#### cava 
>Console visualizer
#### cmus
>Feature-rich ncurses-based music player
#### top
> task manager
#### picom rounded
> X Compositor (a fork of xcompmgr-dana) (with rounded corners patch)
#### Suckless Simple Terminal
> build from source terminal emulator, perfect for customization
> "but I don't use/like st.." no problem I have the color palette!
> ![color palette](backgrounds/cp.png)
> ![foreground background and cursor](backgrounds/fgbgcs.png)
#### Neofetch 
> A CLI system information tool written in BASH that supports displaying images.
#### i3-gaps
>A fork of i3wm tiling window manager with more features, including gaps

## installation
### get :
- neofetch

``` bash
# arch based
$ sudo pacman -S neofetch

# ubuntu/debian based
$ sudo apt-get install neofetch

```

- tint2

``` bash
# arch based
$ sudo pacman -S tint2

# ubuntu based
$ sudo apt install tint2

```

- cava

``` bash
https://github.com/karlstav/cava.git
```

- cmus

``` bash
# arch based
$ sudo pacman -S cmus

#Ubuntu based
$ sudo apt-get install cmus
```

- picom rounded

```
https://github.com/sdhand/picom
```

- rofi 

```
https://github.com/davatorium/rofi
```

- w3m & image magick (optional, if you want images on neofetch)

``` bash
$ sudo pacman -S w3m

Ubuntu/Debian based
$
```
#### install
- rofi

``` config
# make a shortcut first
# for example  i3

bindsym $mod+d exec --no-startup-id rofi -show run
```
> now move/copy the file 'dmenu-forked.rasi' from this repo to 

 ```/usr/share/rofi/themes```


> then open rofi with your shortcut that you have made (mine is win/$mod + d)

> now type 'rofi-theme-selector' 
![rofi select theme](assets/rofip1.png)

> select the theme 'dmenu-forked by nnnathanlemonnn'

- rofi powermenu

> clone adi1090x's repo ```https://github.com/adi1090x/rofi.git``` and install it
on your machine, after that, go to ```~/.config/rofi/powermenu```.

> move/copy 'dmenu-forked-powermenu.rasi' from this repo to ```~/.config/rofi/powermenu```

> configure the ```powermenu.sh``` script 


``` bash
theme="dmenu-forked-powermenu"
dir="$HOME/.config/rofi/powermenu"

# random colors
#styles=($(ls -p --hide="colors.rasi" $dir/styles))
#color="${styles[$(( $RANDOM % 8 ))]}"

# comment this line to disable random colors
#sed -i -e "s/@import .*/@import \"$color\"/g" $dir/styles/colors.rasi

# comment these lines to disable random style
#themes=($(ls -p --hide="powermenu.sh" --hide="styles" --hide="confirm.rasi" --hide="message.rasi" $dir))
#theme="${themes[$(( $RANDOM % 24 ))]}"

```

> make sure these random commands are commented, use '#' to comment. now save and quit. test it by 

```
$ ./powermenu.sh
```

> if it works, copy ```powermenu.sh``` to ```/usr/bin/```. now add it to your window manager config (i3)

```config
bindsym $mod+Shift+e exec --no-startup-id powermenu.sh
```

> now test it (mine's win+shift+e)


- tint2

> copy ```tokyo-night.tint2rc``` from this repo to ```~/.config/tint2/```. select the theme by running 'tint2conf'

- neofetch


## note

## project status
- still work in progress, testing, also finding & fixing bugs







