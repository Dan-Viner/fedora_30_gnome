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
	"topIcons plus" "dash to panel" "system monitor"

