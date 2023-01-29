# Aplicativos

## versão linnux 

```bash 
sudo apt install neofetch
```

```bash
neofetch
```

## Drive Nvidia linux

```bash
sudo apt search nvidia-driver
```

```bash
sudo apt install nvidia-driver-495  
```

## Sensor

```bash
sudo apt-get install lm-sensors
```

```bash
sudo sensors-detect
```

```bash
sudo sensors
```

```bash
sudo watch sensors
```

```bash
sudo apt-get install xfce4-sensors-plugin
```

```bash
sudo chmod u+s /usr/sbin/hddtemp
```

## Google Drive no XFCE, Debian e Ubuntu
Comando 01

```bash 
sudo apt-get install gnome-control-center gnome-online-accounts
```
Comando 02 
```bash 
sudo mkdir /opt/gnome-online-accounts
```
Comando 03 - criando Script

```bash 
sudo nano /opt/gnome-online-accounts/gnome-accounts
```
Colar texto abaixo de baixo no nano 

```bash 
#!/bin/sh

XDG_CURRENT_DESKTOP=GNOME gnome-control-center online-accounts
```
Salve teclando Ctrl + x confirme teclando s e tecle enter

Comando 04

```bash 
sudo chmod +x /opt/gnome-online-accounts/gnome-accounts
```
Comando 05

```bash 
sudo nano /usr/share/applications/Contas-Online.desktop
```
Colar texto abaixo de baixo no nano 

```bash 
[Desktop Entry]
Version=1.0
Name=Contas Online
Comment=Contas on-line                    
Exec=/opt/gnome-online-accounts/gnome-accounts
Icon=goa-panel
Terminal=true
Type=Application
Categories=XFCE;GTK;Settings;DesktopSettings;X-XFCE-SettingsDialog;X-XFCE-Perso$
StartupNotify=true
OnlyShowIn=XFCE;
X-XfcePluggable=true
```

Salve teclando Ctrl + x confirme teclando s e tecle enter

Para configurar a sua conta do Google vá ao Menu > Configurações > Gerenciador de configurações > Contas Online.