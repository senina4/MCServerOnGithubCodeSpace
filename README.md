# Minecraft伺服器在Github-Codesaces上
使用 Github Codespaces 製作 Minecraft 伺服器。

- [Minecraft 伺服器在 Github Codesaces 上](#Minecraft伺服器在Github-Codesaces上)
  - [安裝指南](#安裝)
    - [安裝 Java JRE](##安裝-Java-JRE)
      - [Upgrade Outdated Package](###Upgrade-Outdated-Package)
  - [安裝 Minecraft 伺服器](##Install-Minecraft-Server)
      - [下載安裝檔](###Download-server-file)

# 安裝

## 創建-Github-Codespace
 [你可以參考 Github 文檔](https://docs.github.com/en/codespaces/developing-in-a-codespace/creating-a-codespace-for-a-repository).

## 安裝-Java-JRE

### 下載軟體包信息
指令用於從所有配置的來源下載軟體包信息
```
sudo apt-get update
```

### 安裝-JDK
Minecraft Server 需要用 JDK 才能執行

```
sudo apt install openjdk-17-jre-headless
```

## 安裝Minecraft-server

[從這個網站下載](https://mcversions.net/)後，上傳至你的 Codespace。

安裝步驟可以由[這裡](https://minecraft.fandom.com/zh/wiki/%E6%95%99%E7%A8%8B/%E6%9E%B6%E8%AE%BE%E6%9C%8D%E5%8A%A1%E5%99%A8?variant=zh-tw#Linux%E6%93%8D%E4%BD%9C%E6%8C%87%E5%AF%BC)設置，這裡不在敘述。

最後你必須把 ```server.properties``` 檔案裡的 ```use-native-transport``` 改成 ```false```


## 下載Ngrok
你可以從這下載 [Ngrok](https://dashboard.ngrok.com/get-started/setup)
<img src="https://github.com/senina4/MC-Server-On-Github-CodeSpaces/raw/main/IMG_0266.jpeg"/>

然後上傳至Codespace

並在終端機輸入以下解壓縮指令
```
tar zxvf {Ngrok 檔案}.tgz
```

然後複製你的token
<img src="https://github.com/senina4/MC-Server-On-Github-CodeSpaces/raw/main/IMG_0271.jpeg"/>

貼上至終端機
```
./ngrok config add-authtoken <token>
```

然後執行
```
./ngrok tcp 25565 --region jp
```
