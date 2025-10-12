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
3. 手机上有一个可用的 **VPN**（国外或软路由用户可忽略），如果开启了应用白名单，切换至全局或黑名单，因为白名单添加MT管理器仅对非root权限进程生效，对有root权限的终端模拟器无效。  

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

## 常见问题解答

写在前面：如果有一些术语或简单操作你不了解，例如怎么用fastboot刷img、怎么解锁和回锁，请先到酷安等平台搜索学习，ChatGPT、Deepseek等AI可能也能帮到你，管理员或群友没有义务为你回答这些解锁前理应自学掌握的知识，询问太低级的问题可能被禁言一天。  
**未经允许私聊群组内的其他成员（包括管理员），尤其是主页明确标注禁止私聊的人，违者将被禁言并举报，请提前了解相关Telegram服务条款，不要将QQ的使用思维代入TG。私聊申诉bot(@qdykernel_Appeal_bot)问非申诉相关的事将被永久禁言。**

### 内核常见问题

1. 内核什么时候更新的，sukisu版本是什么？  
关注[频道内消息](https://t.me/qdyKernel)，每次内核更新都会在频道内发更新日志，没发就代表没有更新。  
2. 一机一码会影响恢复出厂设置吗？  
不影响，但强烈不建议恢复出厂设置，OPPO近期系统存在问题，恢复出厂可能无法开机，需要fastboot刷一遍全量包才能开机，天玑甚至可能需要售后刷机才能恢复。  
3. 如果一机一码不匹配，会出现什么？我的数据安全吗？  
如果校验失败，系统会在开机1~2分钟后崩溃重启，你的数据不会丢失，fastboot刷回原厂内核即可。按开机键几秒就重启的和玩游戏偶尔重启的不是校验失败。  
4. 我不想使用GKI了，如何回LKM？  
先用管理器直接安装修补init_boot安装LKM模式，然后重启到fastboot，刷回原厂boot.img。  
5. GKI如何OTA保root?  
注:由于OPPO系统bug太多，强烈不建议OTA后将Anykernel3包刷到另一槽位然后重启  
当系统更新安装完成但尚未重启之前，从Sukisu管理器的安装按钮选择LKM 修补/安装 - 安装到未使用的槽位，然后使用OPPO系统更新内的重启按钮，不要点Sukisu管理器的重启。  
成功开机后再刷入Anykernel3内核转到GKI模式。（刷AK3之前并不需要还原原厂init_boot.img或卸载LKM。因为可以共存且GKI优先级更高，刷入GKI内核后LKM模式会被忽略）  
6. 我不想玩机了，怎么回锁？  
使用系统更新的本地安装功能刷两遍最新系统全量包，刷完一遍，重启，再本地更新一遍，确保两个槽都是官方系统，然后再到fastboot回锁。  
7. 防格机能百分比保护我的基带和ocdt吗？  
不能，防格机针对已知的格机手段尽可能实现了最大保护，但安全性与便捷性永远也不可能平衡，为了不对用户的正常操作产生干扰，防格机仍然存在少数绕过方式，请自行甄别运行的程序和脚本的可信度。  
8. 如何验证防格机是否生效？  
使用[自检脚本](https://github.com/QDYGKI/LSM-test-scripts)测试。  
9. 内核需要与管理器版本匹配吗？  
不需要。你可以选择从Sukisu的Release中下载稳定版管理器，也可以从SukiSU或秋刀鱼频道下载bot发送的CI版，遇到问题了就切换一下稳定版/CI版，内核与管理器版本并不需要一致，也不是每个内核都有对应小版本的管理器。   

### bot常见问题
1. 为什么下载时 bot 提示“你已达到最大设备限制，如果你确实需要更多设备，请联系管理员”  
2025.10.01 上午 5:13 - 上午 8:05 分期间向bot发送过下载命令，包括下载失败均会被记录设备码，请联系群聊内管理员进行重置。  
如果你向bot申请下载的设备大于3台，同样会触发此问题，这是预期的，请向群聊内管理员证明多台设备均为个人自用，即可添加设备数。  
2. 为什么下载时 bot 提示“错误: 该机型暂不支持。仅提供一加和真我6.6.X内核，欧加真6.1.X内核请从频道下载小小w提供的文件。”  
首先，请检查你的设备id是否为最新，我们于 2025.09.30 下午 7:35 分更换了read-id-elf的密钥，早于此时间的密钥无法下载，请执行bot发送的指令后重试。  
否则，请跟随bot指引下载小小w的文件。  
3. 错误: 设备码解析失败，请重新执行 /dl  
首先请检查你的设备id是否为最新，我们于 2025.09.30 下午 7:35 分更换了read-id-elf的密钥，早于此时间的密钥无法下载，请执行bot发送的指令后重试。  
否则，检查你发送的文本是否正确。  
4. 错误: 内核制作失败，服务器内部问题。  
请重新执行bot发送的最新命令，若问题仍然存在，请加入[bot反馈频道](https://t.me/+yfaQ5ZcBg8BmNDE1)反馈。  
5. 执行 bot 发送的命令没有任何输出?  
通常为网络问题，请检查VPN可用性。  
也可以尝试使用此备用命令：  
```bash
/system/bin/su -c "curl -L https://sstaticstp.1007890.xyz/read-id -o /data/read-id-elf.sh&&chmod +x /data/read-id-elf.sh&&/data/read-id-elf.sh"
````

## 常用工具链接
### 官方固件下载
[大侠阿木云盘](https://yun.daxiaamu.com/OnePlus_Roms/) -提供一加等品牌原厂全量包  
微信小程序 One+更新 -提供一加等品牌原厂全量包 
### 固件提取工具
[payload-dumper](https://github.com/5ec1cff/payload-dumper) -一个用于从全量包里面提取boot等分区映像的工具，支持直接从上述两个全量包获取网站给出的链接提取，无需下载完整全量包   
[FastbootEnhance](https://github.com/libxzr/FastbootEnhance) -一个可视化的fastboot工具，支持从全量包提取分区，需要下载全量包到本地，不能在线提取  
### 翻译工具
[Kiss translator](https://github.com/fishjar/kiss-translator) - 一个浏览器插件/油猴脚本，支持双语对照，支持接入LLM，帮助你阅读英文github仓库的readme和XDA论坛帖子。  
[Pot](https://github.com/pot-app/pot-desktop) - 一个PC端划词翻译或OCR翻译软件，支持LLM。
