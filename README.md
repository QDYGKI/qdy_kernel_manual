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
2. 下载安装 **Sukisu Ultra 管理器** 和 **MT 管理器** 这两个 app，并用你现在的 root 方案的管理器授予其 root 权限。  
3. 手机上有一个可用的 **VPN**（国外或软路由用户可忽略），如果开启了应用白名单，需要把 MT 管理器添加至白名单。  

---

## 快速开始  

1. 在 Telegram 中找到秋刀鱼内核下载 bot：[`@qdykernel_download_bot`](https://t.me/qdykernel_download_bot)，发送 `/download` 指令。  
2. 复制 bot 回复的命令，打开 **MT 管理器**，从左上角菜单键打开工具栏中的 **终端模拟器**（MT 终端扩展包装不装都行）。  
3. 在终端中粘贴命令并回车，等待几秒。  
4. 如果一切正常，终端将输出设备码，例如：

Please copy the following string and send it to the bot(including ==). ↓ ↓ ↓ ↓ ↓ ↓ ↓ ↓ BwRaWFcMFVlnhdzhiufBSTIKCEFRQT8fDmMjIj9QVVEwXFRHQ0ddT1xWX0UiJ0NYRA==

5. 复制设备码（注意 ↓↓↓ 下方的才是设备码，不要把英文提示也复制了。设备码末尾是否有等号、有几个等号都不重要），将设备码发送给 bot，等待内核上传（访问量小的情况下大概 10 秒，内核文件大小在 30Mb 左右）。  
6. 下载内核，保存到自己能找到的路径。  
7. 打开 **Sukisu Ultra app**，点主页上方的状态显示。  

---

