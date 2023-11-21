# Minecraft-Server-On-Github-CodeSpaces
Run Your Own Minecraft Server On Github CodeSpaces
This is a guide for Minecraft on Github Codespace.

- [Minecraft Server On Github CodeSpaces](#Minecraft-Server-On-Github-CodeSpaces)
  - [Install](#install)
    - [Install Java JRE](##Install-Java-JRE)
      - [Upgrade Outdated Package](###Upgrade-Outdated-Package)
  - [Install Minecraft Server](##Install-Minecraft-Server)
      - [Download server file](###Download-server-file)

# Install

## Create-A-CodeSpace
First at all, create [a codespace](https://docs.github.com/en/codespaces/developing-in-a-codespace/creating-a-codespace-for-a-repository).

## Install-Java-JRE

### Upgrade-Outdated-Package
Upgrade outdated package file list:
```
sudo apt-get update
```

### Install-JDK
And install JDK: ([Newest Version](https://www.oracle.com/tw/java/technologies/downloads/))
```
sudo apt install openjdk-{Version}-jre-headless
```

## Install-Minecraft-server

### Download-server-file
You can download server file on [this website](https://mcversions.net/)

### Install Server

### First Run
Upload the server file.
```
java -Xms2G -Xmx2G -jar {File Name}.jar nogui
```

### Edit Eula
```eula.txt```>>>```eula=true```
```
java -Xms2G -Xmx2G -jar {File Name}.jar nogui
```
```server.properties``` >>> ```use-native-transport=false```


## Download Ngrok
Download [Ngrok](https://dashboard.ngrok.com/get-started/setup) first.
<img src="https://github.com/senina4/MC-Server-On-Github-CodeSpaces/raw/main/IMG_0266.jpeg"/>

Upload to Codspace.
```
tar zxvf {filename}.tgz
./ngrok config add-authtoken <token>
./ngrok tcp 25565 --region jp
```
