# Fedora30 Gnome
a new Fedora 30 WS initialization notes and files.

### starting up
	sudo dnf update -y

### Enabling the RPM Fusion repositories
#### free repositories:
	sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm

#### non-free repositories:
	sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm

### install some important apps
	sudo dnf install clipit htop meld anki git lyx (chromium) gnome-tweak-tool (qemu virt-manager) eclipse snapd vlc i3 timeshift thunderbird dconf-editor
	

### adding multimedia codecs:
	sudo dnf -y install gstreamer1-plugins-base gstreamer1-plugins-good gstreamer1-plugins-ugly gstreamer1-plugins-bad-free gstreamer1-plugins-bad-freeworld gstreamer1-plugins-bad-free-extras

### adding support of hebrew fonts
	sudo dnf install culmus-* alef-fonts* google-noto-sans-hebrew-fonts

### install some important apps through snap
	snap install sublime pycharm-community android-studio spotify

### important Gnome-extensions
	"topIcons plus" "dash to panel"

### configurations
*clipit:*
	check: "use primary" "automatically paste selected items"
	uncheck: "use copy" "synchronize clipboards" "save URLs" "capture hyperlinks only" "use right click menu"
		(in History:) "show in reverse order" "purge history after timeout"

*add online accounts*

*Gnome-tweaks:*
	appearance, color theme, touchpad & mouse, startup applications	

*language:*
	add language & shortcuts for switching layouts.
	The default encoding of "UTF-8" is suppose to work fine, but for documents that were written on Windows - the encoding will be "Windows-1253", so you'll have to first convert it to the right encoding: "iconv -f Windows-1253 -t UTF-8 input.txt > output.txt"
	I chnaged the default font in Gedit to "aleph regular", and if open a file through the app (and not by double-click on the file)- you can also choose a specific encoding and see which encodings are available for Hebrew. (you can change the default encoding for Gedit by adding it to the top of the list in dconf: org -> gnome -> gedit -> preferences -> encodings)
	There is still the issue of rtl + ltr combined view that I don't know how to solve yet

*Terminal:* set Ctrl+V to paste, Colors, Fonts, New terminal name

*Thunderbird:* rtl language add-on (BiDi mail UI)

*Firefox:* tab session manager, adBlocker

*dconf editor:* in org -> gnome -> shell -> app-switcher change "current-workspace-only" to true

*add the files:* .inputrc (to define default behavior), .bash_aliases, .bashrc, .vimrc, etc.

*Scaling:* cahnge the scaling factor in gnome tweaks, and then change the inner fonts in each app.
	in Firefox: serach the web to fing how to scale the entire app: https://support.mozilla.org/en-US/questions/1239467.
	there is also a new experimental feature in gnome that allows fractional scaling even for x-severs (gsettings set org.gnome.mutter experimental-features "['scale-monitor-framebuffer']"). see here: https://www.linuxuprising.com/2019/04/how-to-enable-hidpi-fractional-scaling.html

*virtual machine (KVM):* I used these instructions: https://computingforgeeks.com/how-to-install-kvm-on-fedora/. but this looks simpler and mybe worth a shot: https://www.youtube.com/watch?v=IqB8zJ9aTWA.
	included packages: bridge-utils libvirt virt-install qemu-kvm (Install KVM / QEMU on Fedora 30), virt-top libguestfs-tools (virtual machine management), virt-manager (Virtual machine Manager GUI).
	how to initiate a KVM: https://www.linux.com/tutorials/creating-virtual-machines-kvm-part-1/
	for testing see: https://computingforgeeks.com/how-to-create-and-configure-bridge-networking-for-kvm-in-linux/.
	for video instructions: https://www.youtube.com/watch?v=IqB8zJ9aTWA
