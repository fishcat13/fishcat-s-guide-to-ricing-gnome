# fishcat's guide to ricing gnome
![](https://github.com/fishcat13/fishcat-s-guide-to-ricing-gnome/blob/main/Screenshot%20From%202024-09-25%2021-39-37.png)

**everything you need to know to turn gnome into a modern butifull desktop with gnome**


**get the needed extensions**

 - we will use a few extensions to make gnome feel and work better

1. [dash to dock](https://extensions.gnome.org/extension/307/dash-to-dock/)

2. [burn my windows with the tv effect](https://extensions.gnome.org/extension/4679/burn-my-windows/)

3. [magic lamp](https://extensions.gnome.org/extension/3740/compiz-alike-magic-lamp-effect/)

4. [compiz windows](https://extensions.gnome.org/extension/3210/compiz-windows-effect/)

5. [blur my shell](https://extensions.gnome.org/extension/3193/blur-my-shell/)  <br>
 

**create a theme directory**

<br>

    mkdir .themes
    mkdir .icons

<br>
 
 **get your themes and move your icons and cursor to .icons and your gtk and shell theme to .themes**

<br>

i will add a theme directory with the theme and wallpaper i use

<br>
 
if youre using mine the file contains three themes (i use the dark one)

<br>

go to extentions and enable user themes 

<br>

go to the gnome tweaks app and equip the theme you chose 

<br>

now all you need is to change the gtk adwite theme with a script 
which i will provide a link for tho there obviously other ways to do it manually

<br>

credit to [this guy](https://github.com/odziom91/libadwaita-theme-changer)

<br>

    git clone https://github.com/odziom91/libadwaita-theme-changer.git
    cd libadwaita-theme-changer
    chmod +x libadwaita-tc.py
    ./libadwaita-tc.py

<br>

**you may have noticed the theme does not apply to all apps**

<br>

**lucily this can be fixed**

<br>

    vim /etc/environment  

<br>

**it should look like this**

<br>

     GTK_THEME=Your-Theme-Name

<br>

**this should work perfectly on all not flatpak apps**

<br>

to fix it on flatpak

<br>


     flatpak --user override --filesystem=/home/$USER/.icons/:ro
     flatpak --user override --filesystem=/usr/share/icons/:ro 
     flatpak --user override --filesystem=~/.config/gtk-4.0
     flatpak --user override --filesystem=~/.themes


<br>

if you found this guide helpfull and would like to fix typos i would apricciate it 

<br>

# byeeeeeeeee :D

<br>

**credits and sources**
<br>
[shell/gtk theme](https://www.gnome-look.org/p/2014493)
[cursors](https://www.gnome-look.org/p/1818760)
[icons](https://www.pling.com/p/1686927/)





     




