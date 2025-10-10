# 秋刀鱼内核用户手册  

---

## 秋刀鱼内核适用范围  
- **品牌**：一加、真我  
- **处理器**：骁龙8至尊版、天玑9400+  
- **内核版本**：6.6.X  
- **系统**：ColorOS 或 OxygenOS（第三方系统可能无法获取设备码）  

---

## 前提条件  
1. 手机已有 **root 权限**（无论是 Magisk、KernelSU 还是 Apatch）。  
2. 下载安装 [Sukisu Ultra 管理器](https://github.com/SukiSU-Ultra/SukiSU-Ultra/releases) 和 [MT 管理器](https://mt2.cn/download/) 这两个 app，并用你现在的 root 方案的管理器授予其 root 权限。  
3. 手机上有一个可用的 **VPN**（国外或软路由用户可忽略），如果开启了应用白名单，需要把 MT 管理器添加至白名单。  

---

## 快速开始  

1. 在 Telegram 中找到秋刀鱼内核下载 bot：[@qdykernel_download_bot](https://t.me/qdykernel_download_bot)，发送 `/download` 指令。  
2. 复制 bot 回复的命令，打开 **MT 管理器**，从左上角菜单键打开工具栏中的 **终端模拟器**（MT 终端扩展包装不装都行）。  
3. 在终端中粘贴命令并回车，等待几秒。  
4. 如果一切正常，终端将输出设备码，例如：
```bash
Please copy the following string and send it to the bot(including ==). 
↓ ↓ ↓ ↓ ↓ ↓ ↓ ↓ 
BwRaWFcMFVlnhdzhiufBSTIKCEFRQTafDmMjIj9QVVEwXFRHQ0ddT1xWX0UiJ0NYRA==
```
5. 复制设备码（注意 ↓↓↓ 下方的才是设备码，不要把英文提示也复制了。设备码末尾是否有等号、有几个等号都不重要，但如果有等号一定不要漏掉），将设备码发送给 bot，等待内核上传（访问量小的情况下大概 10 秒，内核文件大小在 30Mb 左右）。  
6. 下载内核，保存到自己能找到的路径。（不要试图解压下载的zip文件，保持原样。）
7. 打开 **Sukisu Ultra app**，点主页上方的状态显示（显示未安装或工作中的大方框），点击 刷写AnyKernel3，选择刚才保存的zip格式的内核文件（使用系统文件选择器而不是MT管理器等第三方文件管理器），选择槽位不用动，保持默认，点确认，KPM修补保持跟随内核，点下一步。
8. 刷入内核时，脚本会询问是否修补KPM，如果你不知道什么是KPM，建议直接按一下音量上键，跳过修补。当跳转浏览器显示秋刀鱼内核声明时，表示内核安装成功，可以重启手机了。

设备码理论上只需要获取一次，后续获取内核时可以先发送 `/download` 指令，再复制粘贴发送之前聊天记录中的设备码给bot，无需再次到MT管理器执行命令获取。
使用bot时务必遵循发送 `/download` 指令、发送设备码的顺序。如果连发两次指令或者连发两次设备码，bot不会回应。

---

## 视频演示


https://github.com/user-attachments/assets/1e3e39ec-3e71-411f-8895-dbd39310c8c4


https://github.com/EU65/qdy_bot_manual/raw/refs/heads/main/media/video_guide.mp4

