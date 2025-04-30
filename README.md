2025.4.30，Switch系统更新20.0.0

（1） 任天堂官方更新Switch的系统20.0.0，熔断21，在相册一排的小圆图标新增“游戏分享”和“虚拟游戏卡”两个图标，数字版游戏可以分享，只玩破解游戏的玩家无视，只玩虚拟系统的玩家也无视。Game-based learning solutions

（2）已经提取20.0.0的离线升级固件，19.0.1和之前几个版本都是229个系统文件，这次20.0.0是235个系统文件，因为增加了数字游戏分享的功能。
提取离线升级固件挺简单的，Hekate6.2.2开机，更多加载，lockpick_rcm可以提取19.0.1或以下的虚拟系统本主机prod.keys，原来备份过的也能用，正版系统升级20.0.0后，再关机重启进更多加载，选“tegraexplorer.bin”可以dump出sys emmc就是正版系统的离线固件。

（3）目前大气层1.8.0只能破到19.0.1，所以想升级20.0.0玩破解游戏的只能等atmosphere，hekate，sigpatch这三件套更新支持20.0.0才行。现在已经升级正版系统20.0.0的玩家，不能通过Hekate启动的方式进真实（正版）系统或真实（破解）系统，只能点Hekate右下角的重启-官方系统，才能进20.0.0正版系统。

（4）双系统玩家，尤其是续航、OLED和Lite这类mariko型号这几天就不要进正版系统联机玩游戏了，一旦正版系统升级20.0.0，熔断21，缺少20.0.0的warmboot_mariko补丁，还会影响虚拟系统19.0.1或以下，就是休眠死机。非续航的不影响，正版系统升级20.0.0也可以同时继续玩虚拟系统19.0.1。

（5）只玩虚拟系统的玩家完全不用理会20.0.0的系统升级，暂时乖乖呆在19.0.1玩破解游戏，虚拟系统有90dns和隐藏序号保护，离线升级也不会影响熔断，所以可以开着wifi畅快看wiliwili刷B站或tinfoil使用黑商店，等大气层三件套更新支持20.0.0以后再daybreak离线更新虚拟系统20.0.0。

<img src="[https://github.com/rumla3434/NX_Firmware/Switch20.0.0.jpg?raw=true](https://github.com/rumla3434/NX_Firmware/blob/main/Switch20.0.0.jpg?raw=true)" >

2024.10.7，Switch系统更新19.0.0

2024.10.29，Switch系统更新19.0.1

2025.1.7，Switch系统更新19.0.1rebootless（无重启的系统更新，更新内容不涉Switch系统启动模块）

大气层1.8.0最高支持NX-19.0.1系统。先更新SD卡上的大气层文件，再解压缩官方离线升级固件文件夹，把文件夹复制到SD卡，进系统，找到相册Daybreak刷离线固件升级包

离线升级固件下载地址

https://github.com/rumla3434/NX_Firmware/releases

https://codeberg.org/rumla34/NX-Firmware/releases

「分享」新人必看的大气层更新和升级Switch系统教程

一、基础常识

（1）大气层整合包、Switch系统离线升级固件这两样都是通用的，不区分Switch的机器型号和破解芯片，最新的大气层整合包向下兼容Switch系统。整合包大气层就像搭积木一样。但是整合包里的插件和软件太多的话，会影响大气层系统的稳定运行，所以朗姆不会在整合包里添加那些中看不中用的垃圾插件。这也是每个人发布的大气层整合包都不太一样的原因。而Switch系统离线升级固件是任天堂的Switch主机官方系统，所有人发布的同一个系统版本的Switch系统离线升级固件都一样。

（2）破解的开机启动只有软破和硬破的区别。

硬破的直接按主机的电源键开机，SX芯片，Hwfly芯片，树莓派芯片都一样。

软破的需要先短接，然后注入根目录的payload.bin文件，注入方法有电脑端注入，手机端注入，注入器注入等多种方法，结果都是一样的，没区别。

因为软破比较麻烦，现在树莓派芯片便宜又稳定，所以朗姆建议能软破的也可以花80元-120元包芯包焊接费，改成硬破。

二、更新大气层文件

比如当前大气层1.8.0最高支持NX-19.0.1系统，可以先更新大气层1.8.0，再升级19.0.1系统。

（1）大气层整合包可以更换不同人发布的，首次更换的教程

（1-1）备份atmosphere/contents/下的金手指和游戏MOD

「分享」一键清理contents的旧插件和删主题20241212更新

https://www.tekqart.com/thread-403632-1-1.html

执行以后，删除contents里的各种旧插件和主题，再备份contents目录到电脑。

（1-2）首次使用某个人发布的大气层整合包，包括朗姆发布的大气层整合包系统稳定版，都一样的。

https://www.tekqart.com/thread-386991-1-1.html

之前不管你使用的是谁发布的大气层整合包，都可以随时换，只要版本最新，向下兼容。

请在SD卡保留nintendo，emummc，jksv和switch/checkpoint/saves四个文件夹，删除其余的之后再将压缩包中的文件全选复制到SD卡覆盖，绝对没问题。

jksv，switch/checkpoint/saves，switch/dbi/这三个文件夹是游戏存档备份，没有就不需要备份

nintendo是正版系统有关，只玩虚拟系统的无视

emummc肯定有，不管是隐藏分区的虚拟系统还是文件格式的虚拟系统。

（2）如果你只用朗姆发布的大气层整合包系统稳定版

（2-1）如果你一直使用我发布的包，以后的更新中没有特别的提醒，都是直接覆盖就完成大气层文件的升级。

（2-2）朗姆的大气层整合包系统稳定版有极限超频插件，其实就是多了atmosphere/kips/loader.kip和加了“kip1=atmosphere/kips/loader.kip”的bootloader/hekate_ipl.ini文件，如果用极限超频的，每次覆盖更新大气层文件后，还要覆盖这两个文件。

三、更新Switch系统

（1）离线更新Switch系统

（1-1）更新完大气层最新整合包以后，可以复制最高支持的Switch系统固件，比如更新完大气层1.8.0整合包以后，解压缩Switch系统的19.0.1固件，把命名19.0.1的文件夹，文件夹的命名随意但不能出现中文，看清是文件夹，把文件夹复制到SD卡根目录。

（1-2）开机进真实（破解）系统或者虚拟（破解）系统，进真实系统，离线升级的是真实系统，进虚拟系统，离线升级的是虚拟系统。真实系统和虚拟系统在主机信息里有标注：比如19.0.1|AMS 1.8.0|S或者E，S=真实系统，E=虚拟系统。

（1-3）打开相册进入daybreak.nro，选择19.0.1的文件夹路径，然后一路选择右边的蓝色框选项，选择“continue”，“Preserve settings”，“install（fat32+exfat）”，最后一项：“reboot”重启主机。

（2）联网更新Switch系统

联网更新只限正版系统，更新完大气层1.8.0以后，开机Hekate进真实（正版）系统，连上wifi就可以升级，如果更新速度慢，表示要买游戏加速器，国行正版系统不需要。

# Utility
Firmware database for a discord bot

![poyo]([https://github.com/THZoria/NX_Firmware/assets/50277488/337489f9-b2c8-416a-8355-31820ca2a7a1](https://github.com/rumla3434/NX_Firmware/blob/main/Switch20.0.0.jpg?raw=true))

# More information

More information will be detailed in the [wiki](https://github.com/THZoria/NX_Firmware/wiki), both the new versions that will be released, as well as their technical details.

# To find us

[![Discord](https://img.shields.io/discord/643436008452521984.svg?logo=discord&logoColor=white&label=Discord&color=7289DA
)](https://discord.gg/6zRbG3FsJH)

# Add our bot Poyo

Our bot, currently developed in Discord JS V13 (click to be redirected to the link to add the bot)

[![poyo](https://user-images.githubusercontent.com/50277488/156135958-a87fadb8-841e-4eec-bfb8-32340417fa17.png)](https://discord.com/oauth2/authorize?client_id=854048178907512884&scope=bot&code=GhN3fCiOkdvULwgGFbPp134oJo1FW5&guild_id=55540872135914291520applications.commands)
