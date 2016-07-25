#Immersion API Index#

----------
## Download: 

 [**Unreal-SDK-4_12.rar**](attachment/unreal/4_12/IVR.rar) 





## 参数列表(Command Argument List)：
- ResX=1920 -ResY=1080 -FULLSCREEN -WinX=1920 -WinY=0

##用法： 

- 新建一个unreal c++ project   
- 进入这个project folder
- 新建一个Plugins文件夹，并把 IVR 放入 
- 右击拓展名为**.uproject**（文件蓝色带u字的图标）的文件，点击**Generate Visual Studio project files**
- 打开拓展名为.sln（需安装vs2015）的文件，即可打开工程
- 此时IVR插件已经被放入工程目录里，进行编译一次，再运行，即可打开unreal editor
- 在play mode列表里选择**VR Preveiew**,即可播放VR模式     


##关于儿童VR和普通VR的切换：

- 打开IVR里的**IVRHMD.cpp**
- 在**class FIVRHMD**构造函数的成员变量初始化列表里会看到一个**bIsChildrenEnable**，设置它为 **true/false** 即可 **开启/关闭** 儿童VR
- 需重新编译一次代码再运行，即可打开unreal editor
- 在play mode列表里选择**VR Preveiew**,即可播放VR模式     

## 技术支持：
- 任何有疑问的来问我，





---------------------------------


<center>![](img/UE_plugin_logl.png) </center>
<center> 
</center>

<center>![](img/ekcfj.jpeg) </center>
<center> 
###### Suport by Algorithm Team. 
</center>





