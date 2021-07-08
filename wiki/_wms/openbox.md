---
layout: default
title:  "Openbox"
nav_order: 0
---

# Openbox Window Manager

Openbox is the primary window manager of Archcraft. Written almost entirely in C, openbox is fast and snappy. It is especially great for beginners because, unlike traditional window managers that rely almost entirely on keyboard, Openbox has a **right click** menu with 
useful options. [SS of the menu here] In archcraft, this menu is customised to contain almost all the options that anyone would need. You can use this menu to change your desktop theme, access applications, open your frequenct places etc.

Openbox for archcraft uses polybar as the default status bar. Polybar is heavily customisable while being incredibly light on resources. 

## Customisation:
Archcraft comes with a total of 7 homemade themes for openbox by default. Whilst everything is tuned keeping in mind what users would want, it's very simple to change any element of the setup upto your personal needs.
We'll cover this below.

### Changing/Viewing the default keybindings:
Openbox for Archcraft comes with a plethora of keyboard shortcuts by default. Whilst most of these keybinds are set to what most people generally use, it is understandable that you might want to change them or view them. This can be done easily by:
`Right Click-> Preferences -> Openbox -> Edit rc.xml`
The path for the same is `~/.config/openbox/rc.xml`
This openbox folder has a file named `kbinds.txt` that lists all the default keybinds. 
#### Some important default keybinds:
Please note that windows/super is the default mod key. We will use win to denote it
- `Win + Return = Terminal(Alacritty)`
- `Win + F = File Manager(Thunar)`
- `Win + W = Browser(Midori)`
- `Win + C = Close the currently open application`
- `Win + X = Powermenu`
- `Win     = Application menu(Rofi)`
- `Win + N = Network Menu`

### Polybar
Polybar is used as the default status bar. In archcraft, it comes pre-loaded with a bunch of useful modules, the config for which are located at `~/config/polybar/<theme name>`.
You can tweak the positions of the modules or add new ones via the config file located here.
#### Music Module:
Archcraft uses MPD for playing music via ncmpcpp. The music module of polybar fetches the output from mpd and then displays it on polybar. Adding new music to ncmpcpp can be a bit tricky for new users. The steps below can be used to easily add new music to your playlist.
1. Add your music to `~/Music`
2. Open ncmpcpp via a terminal
3. Press 2 and then press U. This should update your playlist and now you should be able to see the newly added song(s)
4. Now simply select the song(s) and press space to add songs to your current playlist.

###### If the above method doesn't work for you, you can try:
1. Open a terminal and type the following:
    - `$ pkill mpd`
    - `$ cd ~/.mpd`
2. Delete the existing database by
    - `$ rm mpd.db`
3. Now start the mpd and open ncmpcpp again by
    - `$ mpd &`
    - `$ ncmpcpp`
4. Now repeat steps 3 and 4 from the method above to add the songs to your current playlist.
#### Some useful polybar modules:
1. [Spotify now-playing](https://github.com/mihirlad55/polybar-spotify-module): Show the currently playing song in spotify
2. [Polywins](https://github.com/tam-carre/polywins): A module to add a taskbar to your polybar along with some extra controls.

### Tiling in openbox:
Openbox is a stacking windows manager, which means by default it doesn't tile your windows. You can still control the position of windows and tile them manually using `Win + Num Pad` keys.
If you want automatic tiling, you could use [Zen-tile](https://github.com/blrsn/zentile) or any other script that you like. 
### 
# WIP 
