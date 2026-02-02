# 秋刀鱼内核用户手册  

---
**通知：2026年2月2日起，bot下载的内核由SukiSU Ultra切换至ReSukiSU，请使用频道内给出的最新管理器，并查看[ReSukiSU官网](https://resukisu.github.io/)或[Telegram频道](https://t.me/ReSukiSU)了解详情。ReSukiSU在用户操作上与SukiSU类似，切换后无需重新配置授权应用或重新安装模块。遇到问题请勿到SukiSU Ultra反馈。**

## 秋刀鱼内核适用范围  
- **品牌**：一加、真我  
- **处理器**：骁龙8至尊版、天玑9400+  
- **内核版本**：6.6.X  
- **系统**：Android版本16的ColorOS、RealmeUI

频道偶尔也会发联想平板的或转发xiaoxiaow、yc、冷雨、cctv18等的内核，但bot仅支持上述条件的设备。

---

## 前提条件  
1. 手机已有 **root 权限**（无论是 Magisk、KernelSU 还是 Apatch）。  
2. 下载安装 ReSukisu 管理器(频道内每次发布更新推送时会附上最新管理器) 和 [MT 管理器](https://mt2.cn/download/) 这两个 app，并用你现在的 root 方案的管理器授予其 root 权限。  
3. 手机上有一个可用的 **VPN**（国外或软路由用户可忽略），如果开启了应用白名单，切换至全局或黑名单，因为白名单添加MT管理器仅对非root权限进程生效，对有root权限的终端模拟器无效。  

---

## 快速开始  
1. 在 Telegram 中找到秋刀鱼内核下载 bot：[@qdykernel_download_bot](https://t.me/qdykernel_download_bot)，发送 `/download` 或 `/dl` 指令。  
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
7. 打开 **ReSukisu app**，点主页上方的状态显示（显示未安装或工作中的大方框），点击 刷写AnyKernel3，选择刚才保存的zip格式的内核文件（使用系统文件选择器而不是MT管理器等第三方文件管理器），选择槽位不用动，保持默认，点确认，KPM修补保持跟随内核，点下一步。
8. 刷入内核时，脚本会询问是否修补KPM，如果你不知道什么是KPM，建议直接按一下音量上键，跳过修补。当跳转浏览器显示秋刀鱼内核声明时，表示内核安装成功，可以重启手机了。

设备码理论上只需要获取一次，后续获取内核时可以先发送 `/download` 或 `/dl` 指令，再复制粘贴发送之前聊天记录中的设备码给bot，无需再次到MT管理器执行命令获取。

**相同设备每两小时只能从bot获取一次内核。**

如果下载bot或telegram故障，您也可以使用此网站获取内核 [备用下载站](https://ttydtest0.1007890.xyz/) . 请注意，您需要拥有一个github账户，但不在注册时间、贡献度等方面设置门槛。网站和bot共享两小时的设备限速，bot和备用下载站获取到的内核是一样的，都是预置的而不是现场编译的。

---

## 视频演示
https://github.com/user-attachments/assets/1e3e39ec-3e71-411f-8895-dbd39310c8c4

（未压缩）https://github.com/QDYGKI/qdy_kernel_manual/raw/refs/heads/main/media/video_guide.mp4

## 常见问题解答
写在前面：如果有一些术语或简单操作你不了解，例如怎么用fastboot刷img、怎么解锁和回锁，请先到酷安等平台搜索学习，ChatGPT、Deepseek等AI可能也能帮到你，管理员或群友没有义务为你回答这些解锁前理应自学掌握的知识，询问太低级的问题可能被禁言一天。  
**未经允许私聊群组内的其他成员（包括管理员），尤其是主页明确标注禁止私聊的人，违者将被禁言并举报，请提前了解相关[Telegram服务条款](https://telegram.org/tos)，不要将QQ的使用思维代入TG。私聊申诉bot(@qdykernel_Appeal_bot)问非申诉相关的事将被永久禁言。**
**进群须知：只要你加入挂群了，无论目的是什么，你都面临着随时被整个SukiSU联盟封禁的风险！被封禁的同时你将失去下载bot的使用权限。即使被挂出共同群，被攻击，你还击也是你的错，你占理也无条件封禁，不要指望管理员都是机器人严格按规则执行操作，事实上玩机的绝大多数人对外挂是痛恨的。**

### 内核常见问题
1. 内核什么时候更新的，resukisu版本是什么？  
关注[频道内消息](https://t.me/qdyKernel)，每次内核更新都会在频道内发更新日志，没发就代表没有更新。  
2. 刷内核会影响恢复出厂设置吗？  
影响，由于OPPO的不完全开源，GKI内核恢复出厂设置很容易砖，需要到恢复模式手动格式化data一次甚至fastboot再刷一遍全量包才能开机，天玑甚至可能需要售后刷机才能恢复。非必要不要恢复出厂设置，若实在需要，请刷回原厂boot.img.  
3. 如果一机一码不匹配，会出现什么？我的数据安全吗？  
如果校验失败，系统会在开机1~2分钟后崩溃重启，你的数据不会丢失，fastboot刷回原厂内核即可。按开机键几秒就重启的和玩游戏偶尔重启的不是校验失败。  
4. 秋刀鱼内核修改了哪些分区？我不想使用GKI了，如何回LKM？  
秋刀鱼内核刷入后仅修改boot。先用管理器直接安装修补init_boot安装LKM模式，然后重启到fastboot，刷回原厂boot.img。  
5. GKI如何OTA保root?  
注:由于OPPO系统bug太多，强烈不建议OTA后将Anykernel3包刷到另一槽位然后重启  
当系统更新安装完成但尚未重启之前，从ReSukisu管理器的安装按钮选择LKM 修补/安装 - 安装到未使用的槽位，然后使用OPPO系统更新内的重启按钮，不要点ReSukisu管理器的重启。  
成功开机后再刷入Anykernel3内核转到GKI模式。（如果之前使用的是lkm模式，刷入ak3后应还原原厂init_boot，因为ksu1.0到ksu2.0有较大改动，若1.0的lkm和2.0的built-in共存可能不开机）  
6. 我不想玩机了，怎么回锁？  
使用系统更新的本地安装功能刷两遍最新系统全量包，刷完一遍，重启，再本地更新一遍，确保两个槽都是官方系统，然后再到fastboot回锁。  
7. bbg防格机能百分百保护我的基带和ocdt吗？  
首先，答案是不能，防格机针对已知的格机手段尽可能实现了最大保护，但安全性与便捷性永远也不可能平衡，为了不对用户的正常操作产生干扰，防格机仍然存在少数绕过方式，请自行甄别运行的程序和脚本的可信度。其次，防格机这个叫法并不准确，bbg是基带守护（baseband guard），保护关键分区避免主板返厂，被格机后仍然可能黑砖、用户数据丢失，只是更容易救砖。  
8. 如何验证防格机是否生效？  
使用[自检脚本](https://github.com/QDYGKI/LSM-test-scripts)测试。  
9. 内核需要与管理器版本匹配吗？  
不需要。频道内每次发布更新推送时会附上最新管理器文件或链接，最好使用该版本。您也可以到ReSukiSU群组获取最新测试版管理器   
10. 我需要安装susfs4ksu模块吗？
不需要。ReSukiSU管理器自带susfs管理，从主页右上角的设置按钮进入。配置后会自动生成SuSFS Manager模块，删除后可重置susfs配置。如果SUSFS Manager模块存在的情况下再安装一个susfs4ksu模块，可能会冲突导致susfs不工作。    
如果你的内核内置的susfs太新或太旧，ReSukiSU管理器不支持，那么可以安装susfs4ksu模块，但请确同时只有一个susfs相关模块开启。
11. 内核支持风驰吗？为什么我打开游戏调速器不切换？   
内核支持风驰，但风驰具体是否有效需要用户空间配合，需要游戏和游戏模式受支持且游戏助手运行正常网络正常相关域名未被屏蔽。风驰是否有效是内核、OEM驱动、游戏助手共同决定的。不要相信所谓的全局风驰模块能给不支持风驰的游戏和设备带来实质性效果。     
12. 为什么加载nohello、Cherish Peekaboo等隐藏用途的KPM后黑屏死机？    
SukiSU移植的KPM来源于bmax121/KernelPatch但并不兼容所有Apatch KPM，尤其是隐藏用途的KPM。   
13. ReSukiSU能和Magisk等其他root方案共存吗？   
基本上不能。    
14. 如何在KSU、Apatch、ReSukiSU之间互转？      
对于built-in模式，可以直接刷另一个root方案的anykernel3（转到Apatch需要先还原原厂boot），但如果挂载方式改变，需要先卸载所有模块，否则切换后可能出现bug。     
15. 秋刀鱼ak3内核能否通过twrp安装？    
能，虽然因为twrp无法打开网页导致最后出现红字报错，但不影响内核刷写。中文在rec环境可能显示为乱码。     
16. 关于内核自带救砖    
ReSukiSU具有KSU同款救砖，触发方式参见KSU文档，但只能禁用模块，不能恢复冻结的系统应用。   
17. ColorOS16如何获取全量包？    
OPPO给服务器加了额外的验证，c16包无固定直链，每次抓取的链接只有9分钟有效期，建议更新前自行保存全量包便于救砖。文末的常用链接给出了能够获取全量包的网站。      
18. 从旧版本升级到 SukiSU 4.0.0 及以上版本的注意事项    
由于V4更换了supercall实现，向后不兼容，内核与管理器大版本必须对应，否则无法获取root权限。    
如果使用 SukiSU V3 或更早版本修补过LKM，刷入 SukiSU v4 或ReSukiSU 的GKI后应当在下次开机前还原原厂init_boot，否则会遇到很多奇怪的bug。
19. 为什么刷入了20260202发布的内核，SukiSU管理器显示未安装？   
秋刀鱼内核已切换至ReSukiSU，必须卸载SukiSU Ultra管理器后安装ReSukiSU管理器。

### bot常见问题
1. 为什么下载时 bot 提示“你已达到最大设备限制，如果你确实需要更多设备，请联系管理员”  
2025.10.01 上午 5:13 - 上午 8:05 分期间向bot发送过下载命令，包括下载失败均会被记录设备码，请联系群聊内管理员进行重置。  
如果你向bot申请下载的设备大于3台，同样会触发此问题，这是预期的，请向群聊内管理员证明多台设备均为个人自用，即可添加设备数。  
2. 为什么下载时 bot 提示“错误: 该机型暂不支持。仅提供一加和真我6.6.X内核，欧加真6.1.X内核请从频道下载小小w提供的文件。”  
首先，请检查你的设备id是否为最新，我们于 2025.09.30 下午 7:35 分更换了read-id-elf的密钥，早于此时间的密钥无法下载，请执行bot发送的指令后重试。  
5.10.X - 6.1.X内核请加入[小小w的群组](https://t.me/gki_kernels_xiaoxiaow)获取内核。  
3. 错误: 设备码解析失败，请重新执行 /dl  
首先请检查你的设备id是否为最新，我们于 2025.09.30 下午 7:35 分更换了read-id-elf的密钥，早于此时间的密钥无法下载，请执行bot发送的指令后重试。  
否则，检查你发送的文本是否正确。  
4. 错误: 内核制作失败，服务器内部问题。  
若两小时内相同设备已经获取过内核，请两小时后再试。若首次获取，请尝试重新执行bot发送的最新命令获取识别码，若问题仍然存在，请加入[bot反馈频道](https://t.me/+yfaQ5ZcBg8BmNDE1)反馈。  
5. 执行 bot 发送的命令没有任何输出?  
通常为网络问题，请检查VPN可用性。  
也可以尝试使用以下两组备用命令：  
```bash
/system/bin/su -c "curl -L https://sstaticstp.1007890.xyz/read-id -o /data/read-id-elf.sh&&chmod +x /data/read-id-elf.sh&&/data/read-id-elf.sh"
````
```bash
su -c "curl -L https://sstaticstp.1007890.xyz/read-id -o /data/read-id-elf.sh&&chmod +x /data/read-id-elf.sh&&/data/read-id-elf.sh"
````
### 群组和频道常见问题
1. 与群组相关的几个bot和频道都有什么用？  
   ~~@qdykernel_Appeal_bot(已废弃，联盟封禁请使用@vc_yc_bot) 封禁或禁言申诉专用，答题不通过被临时封禁不得申诉。发送与申诉无关的消息将被永久封禁。~~  
   @qdykernel_download_bot 内核下载bot。  
   @Yet_Another_Captcha_Bot 入群答题bot，不要屏蔽或归档，申请进群后尽快查看bot私信。  
   [qdykernel Admin Logs](https://t.me/qdykernel_admin_logs) 操作日志频道，记录用户加入、禁言、封禁等事件和原因，申诉前务必先查询。   
   @sukisu_fedlog SukiSU联盟封禁日志   
   @vc_yc_bot SukiSU联盟封禁申诉bot(虽然内核已切换至ReSukiSU，但群组仍订阅SukiSU联盟封禁)

## 常用工具链接
### 官方固件下载
[一个神秘的rom直链解析网站](https://roms.danielspringer.at/ota.php) 从OPPO官方服务器解析ColorOS16/OxygenOS16全量包直链，无需百度网盘，可配合下方的payload-dumper实现免下载完整全量包获取boot，且用且珍惜   
[大侠阿木云盘](https://yun.daxiaamu.com/OnePlus_Roms/) -提供一加等品牌原厂全量包(由于OPPO加密了ColorOS16全量包链接,C16只提供百度网盘下载,无OPPO直链)  
微信小程序 One+更新 -提供一加等品牌原厂全量包(由于OPPO加密了ColorOS16全量包链接,C16只提供百度网盘下载,无OPPO直链) 
### 固件提取工具
[payload-dumper](https://github.com/5ec1cff/payload-dumper) -一个用于从全量包里面提取boot等分区映像的工具，支持直接从上述3个全量包获取网站给出的链接提取，无需下载完整全量包。需要python环境   
[安卓版payload dumper](https://github.com/rcmiku/Payload-Dumper-Compose) -一个用于从全量包里面提取boot等分区映像的工具，支持直接从上述3个全量包获取网站给出的链接提取，无需下载完整全量包。apk直接安装打开   
[FastbootEnhance](https://github.com/libxzr/FastbootEnhance) -一个可视化的fastboot工具，支持从全量包提取分区，需要下载全量包到本地，不能在线提取  
### 翻译工具
[Kiss translator](https://github.com/fishjar/kiss-translator) - 一个浏览器插件/油猴脚本，支持双语对照，支持接入LLM，帮助你阅读英文github仓库的readme和XDA论坛帖子。  
[Pot](https://github.com/pot-app/pot-desktop) - 一个PC端划词翻译或OCR翻译软件，支持LLM。
### 相关仓库地址     
[susfs4ksu](https://gitlab.com/simonpunk/susfs4ksu)   
[ReSukiSU](https://github.com/ReSukiSU/ReSukiSU)   
[SukiSU Ultra](https://github.com/SukiSU-Ultra/SukiSU-Ultra)     
[OnePlus Open Source Software](https://github.com/oneplusoss) -一加内核开源地址（组织）   
[kernel_manifest](https://github.com/OnePlusOSS/kernel_manifest) -一加内核开源地址（清单）一般在这里提issue催一加开源新版本      
