# Ubuntu_Dev - Ubuntu 24.04.2 LTS x86_64

## 🤖Caso quiser uma instalação automatizada.
### 1. baixar o documento "ubuntu-dev-setup.sh"
#### 2. Dê permissão de execução:
```bash 
chmod +x ubuntu-dev-setup.sh
```
#### 3. Execute com:
```bash 
./ubuntu-dev-setup.sh
```


## ⬇️abaixo segue comandos unitarios. 

## 🚀 Script Pós-Instalação - Ubuntu
### Este script contém comandos e instruções para configurar um sistema Ubuntu após uma instalação limpa.

## ✅ Atualizar o sistema

```bash 
sudo apt-get updade && sudo apt-get upgrade && sudo apt-get dist-upgrade && sudo apt-get autoremove -y 
```

## 🖥️ Instalar Neofetch
```bash
sudo apt install -y neofetch
```
#### Após a instalação, você pode rodar o comando:
```bash
neofetch
```

## 🛠️ Instalar utilitários básicos
Gnome Tweaks para ajustar temas, fontes, comportamento de janelas etc.

Gnome Extensions App: gerenciador gráfico de extensões GNOME.
Git, Curl, Rsync, Vim: ferramentas essenciais para terminal e desenvolvimento.

VLC: reprodutor de mídia completo.

Htop: visualizador interativo de processos.
```bash 
sudo apt-get install gnome-tweaks gnome-extensions-app git curl rsync vim vlc htop
```
##  Plano para Instalação Automática das Extensões GNOME
#### 01.Instalar o gnome-shell-extension-installer
```bash
sudo apt install -y git curl

curl -Lo gnome-shell-extension-installer https://raw.githubusercontent.com/brunelli/gnome-shell-extension-installer/master/gnome-shell-extension-installer
chmod +x gnome-shell-extension-installer
sudo mv gnome-shell-extension-installer /usr/local/bin/
```
#### 02.Instalar as extensões GNOME automaticamente
```bash
gnome-shell-extension-installer 615 AppIconsTaskbar --yes
gnome-shell-extension-installer 6 AppsMenu --yes
gnome-shell-extension-installer 517 Caffeine --yes
gnome-shell-extension-installer 2087 DesktopIconsNG --yes
gnome-shell-extension-installer 615 MediaControls --yes
gnome-shell-extension-installer 516 QuickSettingsAudioPanel --yes
gnome-shell-extension-installer 435 ResourceMonitor --yes
gnome-shell-extension-installer 5721 TailscaleStatus --yes
gnome-shell-extension-installer 615 UbuntuAppIndicators --yes
gnome-shell-extension-installer 307 UbuntuDock --yes
gnome-shell-extension-installer 19 UserThemes --yes
```
#### 03.Ativar as extensões automaticamente (opcional)
```bash
gnome-extensions enable app-icons-taskbar@p11y.com
gnome-extensions enable apps-menu@gnome-shell-extensions.gcampax.github.com
gnome-extensions enable caffeine@patapon.info
gnome-extensions enable ding@rastersoft.com
gnome-extensions enable mediacontrols@clameur.me
gnome-extensions enable quicksettings-audio-panel@pappas.dev
gnome-extensions enable resource-monitor@paradoxxx.zero.gmail.com
gnome-extensions enable tailscale-status@k3a.me
gnome-extensions enable ubuntu-appindicators@ubuntu.com
gnome-extensions enable ubuntu-dock@ubuntu.com
gnome-extensions enable user-theme@gnome-shell-extensions.gcampax.github.com
```
## 📦 Instalar Snap e Flatpak (opcional)
```bash 
sudo apt install -y snapd flatpak gnome-software-plugin-flatpak
```

## 🌐 Navegador Google Chrome

```bash 
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install -y ./google-chrome-stable_current_amd64.deb
```


## 🧰 Instalar ferramentas de desenvolvimento

📄 Visual Studio Code
```bash 
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/
sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] \
https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
sudo apt update
sudo apt install -y code
```
## 📦 Instalar extensões recomendadas
### ⚠️ Importante: 

Esse comando só funciona depois que o VS Code for instalado e o comando code estiver disponível no terminal. Normalmente, ele já é ativado automaticamente, mas se não funcionar, você pode abrir o VS Code, pressionar Ctrl+Shift+P e executar o comando:
Shell Command: Install 'code' command in PATH.
```bash 
code --install-extension GitHub.copilot-chat
```
```bash 
code --install-extension vscode-icons-team.vscode-icons
```
```bash 
code --install-extension Vue.volar
```
```bash 
code --install-extension ms-azuretools.vscode-containers
```
```bash 
code --install-extension ms-vscode-remote.remote-containers
```
```bash 
code --install-extension ms-azuretools.vscode-docker
```
```bash 
code --install-extension docker.docker
```
```bash 
code --install-extension dracula-theme.theme-dracula
```
```bash 
code --install-extension waderyan.gitblame
```
```bash 
code --install-extension GitHub.copilot
```
```bash 
code --install-extension ecmel.vscode-html-css
```
```bash 
code --install-extension oderwat.indent-rainbow
```
```bash 
code --install-extension VisualStudioExptTeam.vscodeintellicode
```
```bash 
code --install-extension Zignd.html-css-class-completion
```
```bash 
code --install-extension ms-vscode.live-server
```
```bash 
code --install-extension ritwickdey.LiveServer
```
```bash 
code --install-extension DavidAnson.vscode-markdownlint
```
```bash
code --install-extension bmewburn.vscode-intelephense-client
```
```bash
code --install-extension MS-CEINTL.vscode-language-pack-pt-BR
```
```bash
code --install-extension esbenp.prettier-vscode
```
```bash
code --install-extension hollowtree.vue-snippets
```
```bash
code --install-extension
```
```bash
code --install-extension
```
```bash
code --install-extension
```
```bash
code --install-extension
```
```bash
code --install-extension
```
```bash
code --install-extension
```

## 📮 Postman (via Snap)

```bash 
sudo snap install postman
```
## 🐬 MySQL Workbench
```bash 
sudo apt install -y mysql-workbench
```
#### Obs: Pode ser necessário instalar o servidor MySQL também:
```bash 
sudo apt install -y mysql-server
```
## 🐳 Instalar Docker Engine (via repositório oficial)
#### 1. Remover versões antigas (se existirem)
```bash 
sudo apt remove -y docker docker-engine docker.io containerd runc
```
#### 2. Atualizar pacotes e instalar dependências
```bash 
sudo apt update
sudo apt install -y ca-certificates curl gnupg lsb-release
```
#### 3. Adicionar a chave GPG oficial do Docker
```bash 
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg \
  | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
#### 4. Adicionar o repositório do Docker
```bash 
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" \
  | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
#### 5. Atualizar índice de pacotes e instalar Docker Engine
```bash 
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
#### 6.Verificar instalação
```bash 
docker --version
```
#### 7. Comando.
```bash 
sudo docker ps
```
## 👤 Utilize o Docker sem sudo
### 📌 Exemplo automático (para o usuário atual)
 Ao instalar o Docker, um grupo chamado docker é criado. Para permitir que o usuário atual use o Docker sem digitar sudo, basta adicioná-lo automaticamente ao grupo.
 ```bash 
sudo usermod -aG docker $(whoami) && newgrp docker
```
## 📄 Instalar ONLYOFFICE Desktop Editors (via repositório oficial)
#### 1.Adicionar repositório oficial do ONLYOFFICE
 ```bash 
echo "deb https://download.onlyoffice.com/repo/debian squeeze main" | sudo tee /etc/apt/sources.list.d/onlyoffice.list
```
#### 2. Adicionar chave pública do repositório
```bash
wget -qO - https://download.onlyoffice.com/repo/onlyoffice.key | sudo apt-key add -
```
#### 3. Atualizar lista de pacotes e instalar
```bash
sudo apt update
sudo apt install -y onlyoffice-desktopeditors
```
## 🖥️ Instalar Remmina (com suporte RDP, VNC, SSH)
```bash
sudo apt update
sudo apt install -y remmina remmina-plugin-rdp remmina-plugin-vnc remmina-plugin-secret
```
## 🧑‍💻 Instalar AnyDesk (via repositório oficial)
#### 01.Adicionar chave GPG do repositório
 ```bash
wget -qO - https://keys.anydesk.com/repos/DEB-GPG-KEY | sudo gpg --dearmor -o /usr/share/keyrings/anydesk.gpg

```
#### 02. Adicionar o repositório do AnyDesk
```bash
echo "deb [signed-by=/usr/share/keyrings/anydesk.gpg] http://deb.anydesk.com/ all main" \
| sudo tee /etc/apt/sources.list.d/anydesk.list

```
#### 03.Atualizar lista de pacotes e instalar o AnyDesk
```bash
sudo apt update
sudo apt install -y anydesk
```
## 🎵 Instalar Spotify (via repositório oficial)
#### 1.Adicionar chave GPG do repositório
```bash
curl -sS https://download.spotify.com/debian/pubkey_0D811D58.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/spotify.gpg > /dev/null
```
#### 2.Adicionar repositório Spotify à lista de fontes
```bash
echo "deb [signed-by=/usr/share/keyrings/spotify.gpg] http://repository.spotify.com stable non-free" \
| sudo tee /etc/apt/sources.list.d/spotify.list
```
#### 3.Atualizar pacotes e instalar
```bash
sudo apt update
sudo apt install -y spotify-client
```
## 🔐 Instalar Bitwarden (via Snap)
```bash
sudo snap install bitwarden
```

```bash

```


## 🎥 Instalar OBS Studio
### 📦 Via APT (recomendado)
```bash 
sudo apt update
sudo apt install -y obs-studio
```

## ✅ Atualizar o sistema (Rodar apos instalação de tudo.)

```bash 
sudo apt-get updade && sudo apt-get upgrade && sudo apt-get dist-upgrade && sudo apt-get autoremove -y 
```
```bash
sudo apt clean
```
