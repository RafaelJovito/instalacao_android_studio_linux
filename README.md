# Instalação do Android Studio no Linux

* Atualizar o Sistema

```shell

sudo apt-get update
sudo apt-get upgrade
```
* Instalar JAVA 8 SDK e OpenJDK 8 e JRE

```shell

sudo apt install openjdk-8-jdk
sudo apt install openjdk-8-jre
sudo apt-get install openjdk-8-jre-headless

```
* Instalar Bibliotecas

```shell

sudo apt-get install libz1 libncurses5 libbz2-1.0:i386 libstdc++6 libbz2-1.0
```
* Instalar KVM

```shell

sudo apt-get install qemu-kvm libvirt-bin virtinst bridge-utils cpu-checker
testar comandos abaixo:

sudo apt-get install qemu-kvm libvirt-bin ubuntu-vm-builder bridge-utils
sudo adduserid -unlibvirtd
sudo ls -la /var/run/libvirt/libvirt-sock
sudo chown root:libvirtd /dev/kvm

```

* Instalar OpenGL

```shell

sudo apt-get install libglu1-mesa-dev freeglut3-dev mesa-common-dev
```

* Variáveis de ambiente

Adicionar as variaváveis de ambiente em: ```sudo vim /etc/profile ou o ~/.bashrc ```

Adicionar os caminhos:

```shell

export ANDROID_HOME=/usr/local/android/android-sdk-linux
export ANDROID_SDK_ROOT=/usr/local/android/android-sdk-linux
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
```

Depois disso, reiniciar o computador.


* Ativar VT-X no Windows e no VMware (caso esteja usando)

No Windows:  ```na barra de busca e digita CMD ```
Colocar os seguintes comandos: 

```
bcdedit /set hypervisorlaunchtype off
bcdedit /set nx AlwaysOn
```
E reinicia o computador.

No VMware:

Editar a configuração do processador:

Definir como VT-X e marcar as duas ultimas opções;
