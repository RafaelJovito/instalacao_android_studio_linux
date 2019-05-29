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
```

* Instalar OpenGL

```shell

sudo apt-get install libglu1-mesa-dev freeglut3-dev mesa-common-dev
```

* Variáveis de ambiente

Adicionar as variaváveis de ambiente em:```shell  /etc/profile ou o ~/.bashrc ```

Adicionar os caminhos:

```shell

export ANDROID_HOME=/opt/android/android-sdk-linux
export ANDROID_SDK_ROOT=/opt/android/android-sdk-linux
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
```

Depois disso, reiniciar o computador.
