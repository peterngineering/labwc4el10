# labwc4el10
*testing on EL10 *only build for v3(the default) but one can be rebuild for x86_64_v2 and aarch64 using the SRPMS*


## Install:
<code>
#>dnf install *.rpm
</code>

<hr>

## Basic Setup:

*create config dirs, create basic menus,set sakura as default terminal.*

<code>

mkdir -p ~/.config/labwc

cp -av /usr/share/doc/labwc/* ~/.config/labwc/

sed -i 's/alacritty/sakura/g' ~/.config/labwc/menu.xml

sed -i 's/alacritty/sakura/g' ~/.config/labwc/rc.xml.all

mkdir -p ~/.config/sfwbar

cp -av /usr/share/sfwbar/sfwbar.config ~/.config/sfwbar/

sed -i 's/alacritty/sakura/g' ~/.config/sfwbar/sfwbar.config

echo "sfwbar >/dev/null 2>&1 &"> ~/.config/labwc/autostart

</code>
<hr>

## Usage:
*If you only have a minimal install with console:*
<code>
$>labwc
</code>

*If you have gdm installed,  you can choose labwc as a session.*

<hr>
<img width="1280" height="800" alt="alma10-labwc-1-vm" src="https://github.com/user-attachments/assets/9b5fefaa-e88d-4a25-8c4a-5b1e3f55787b" />



<hr>
<img width="1920" height="1080" alt="alma10-labwc-2" src="https://github.com/user-attachments/assets/389aaa82-ae7c-4799-933d-d9b37e452ba9" />



<hr>
<img width="1920" height="1080" alt="alma10-labwc-3" src="https://github.com/user-attachments/assets/baf2e7b9-7c65-49f9-bc87-6ad05b84afc6" />



<hr>
<img width="1920" height="1080" alt="alma10-labwc-4" src="https://github.com/user-attachments/assets/cbf3d850-7de5-436e-82f5-90a203c879f0" />




<hr>
<hr>

## Links:

https://labwc.github.io/index.html

https://github.com/LBCrion/sfwbar

https://wiki.archlinux.org/title/Labwc

https://github.com/jtheoof/swappy













