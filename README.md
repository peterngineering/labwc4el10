# labwc4el10
*testing on EL10 *

## Install:
<code>
#>dnf install *.rpm
</code>

<hr>

## Basic Setup:

*create config dirs, create basic menus, set 'sakura' as default terminal.*

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
*If you need a custom scale factor add a stanza to autostart, here is example for a eDP-1 display with 2x. Which is just appended to ~/.config/labwc/autostart*
<code>
wlr-randr --output eDP-1 --scale 2 >/dev/null 2>&1 &
</code>


*If you only have a minimal install with console:*
<code>
$>labwc
</code>

*If you have gdm installed,  you can choose labwc as a session.*

<pre>
<br>
<br>

<img width="1280" height="800" alt="alma10-labwc-1-vm" src="https://github.com/user-attachments/assets/9b5fefaa-e88d-4a25-8c4a-5b1e3f55787b" />

<br>
<br>

<img width="1920" height="1080" alt="alma10-labwc-2" src="https://github.com/user-attachments/assets/389aaa82-ae7c-4799-933d-d9b37e452ba9" />

<br>
<br>

<img width="1920" height="1080" alt="alma10-labwc-3" src="https://github.com/user-attachments/assets/baf2e7b9-7c65-49f9-bc87-6ad05b84afc6" />

<br>
<br>

<img width="1920" height="1080" alt="alma10-labwc-4" src="https://github.com/user-attachments/assets/cbf3d850-7de5-436e-82f5-90a203c879f0" /><br>

<br>
<br>
</pre>

<hr>

## Advanced:
*To rebuild from SRPMS, the easiest way is to use mock.*
*Here are examples I currently use to rebuild SRPMS.*
*This builds the whole chain and adds the arch appropriate suffix as well, eg (_v2)*

<code>
 
Typical normal modern x86_64 version 3 machines
  mock -r alma+epel-10-x86_64 --chain --recurse *.src.rpm

Older x86_64 hardware, version 2  
  mock -r alma+epel-10-x86_64_v2 --chain --recurse *.src.rpm

aarch64 targets
  mock -r alma+epel-10-aaarch64 --chain --recurse *.src.rpm
  
</code>

<hr>

## Links:

https://labwc.github.io/index.html

https://github.com/LBCrion/sfwbar

https://wiki.archlinux.org/title/Labwc

https://github.com/jtheoof/swappy













