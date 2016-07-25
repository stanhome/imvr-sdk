#Immersion API Index#

----------
**document version:**	1.0  
**author:** Xinjie  
**date:** 2016/4/13 16:11:33 

[Home](README.md "Home")

## for Unity3D 5.3 download:

###v2.0

备注：v2 .0版本需要先安装LibIVR模块，请转到[LibIVR-API.md](LibIVR-API.md)并按指示操作。

| 版本        					| 发布日期        					| 更新描述  	|
| :----------------------:					|:---------------------------------| :-----	|
| [2.0.10](attachment/unity/v2.0/ImmersionVRUnityIntegration_v2.0.10.unitypackage) | 2016/07/18 |1、PlayerLog.cs添加运行平台判断（windows）；<br/>2、更新了dll结构，分成ImmersionPlugin.dll和libIVRSDK_1.dll两个|
| [2.0.09](attachment/unity/v2.0/ImmersionVRUnityIntegration_v2.0.09.unitypackage) | 2016/07/11 |1、在Scripts文件夹中增加了脚本文件ServerManager，不用再单独下载了，原先有这个脚本的请删掉；<br/>2、更新了dll，减弱了飘的问题（其实是上个版本我忘记更新dll了）|
| [2.0.08](attachment/unity/v2.0/ImmersionVRUnityIntegration_v2.0.08.unitypackage) | 2016/06/27 |1.取消游戏子目录，直接将文本存储在D:\PlayerLog目录下；<br/>2.规范文本命名，如：SeaHunter_20160620|
| [2.0.07](attachment/unity/v2.0/ImmersionVRUnityIntegration_v2.0.07.unitypackage) | 2016/05/18 |1、同步 ImmersionPlugin.dll 更改， 将 IVR_Initialize， IVR_Destroy 返回值改为 int 类型，并处理重复初始化状态。<br/>**NOTE:** 该版本的游戏**32**位需要 [vc_redist.x86.exe](third-party.md)， **64**位需要 [vc_redist.x64.exe](third-party.md)|
| [2.0.06](attachment/unity/v2.0/ImmersionVRUnityIntegration_v2.0.06.unitypackage) 						| 2016/5/09		|1、陀螺仪转动时不再只转动摄像机物体，而是将根物体旋转。因此UI等元素可以直接挂在根物体下面；</br>2、修改左摄像机物体的名字为“mainCamera”（原先为“Camera_left”）；右摄像机名字为“rightCamera”（原先为“Camera_right”）；</br>3、儿童VR增加了护眼模式logo和商标logo；</br>4、在脚本中增加了selectMonitor的代码；</br>5、修复IVRDevice脚本里“Reset Tracker On Load”选项未选中时，场景会卡死的bug；</br>6、优化了文件结构。|
| [2.0.05](attachment/unity/v2.0/ImmersionVRUnityIntegration_v2.0.05.unitypackage) 						| 2016/4/27		|1、陀螺仪重置快捷键改为键盘上的“Alpha3”键；</br>2、**去掉2.0.03版本中的移屏功能**，Unity程序员在发布儿童VR游戏时，请不要在脚本中对分辨率和全屏进行任何修改，而是在PlayerSettings里设置游戏为**默认全屏启动**，并将分辨率改为1920\*1080。|
| [2.0.04](attachment/unity/v2.0/ImmersionVRUnityIntegration_v2.0.04.unitypackage) 						| 2016/4/25		|1、修复dll无头盔情况下场景无画面的bug；</br>2、修复dll无头盔情况下插入头盔陀螺仪无法工作的bug；</br>3、修复dll头盔多次插拔导致场景无响应的bug；</br>4、修复dll的运行环境过高的问题。|
| [2.0.03](attachment/unity/v2.0/ImmersionVRUnityIntegration_v2.0.03.unitypackage) 						| 2016/4/25		|儿童VR增加屏幕移动功能，可以自动将屏幕放置在第二块屏幕上并自动设置分辨率为1920*1080。Unity程序员请不要将PlayerSettings>produceName写成中文。使用该版本时请与胡鹏沟通。|
| [2.0.02](attachment/unity/v2.0/ImmersionVRUnityIntegration_v2.0.02.unitypackage) 						| 2016/4/20		|1、儿童VR加入了陀螺仪重置功能；</br>2、合并了儿童VR和星云VR的SDK代码，用全局变量控制，默认是星云VR的SDK。若要使用儿童VR的SDK，请在Unity5>Edit>ProjectSettings>PlayerSettings>OtherSettings>Scripting Define Symbols下方的文本框中输入“CHILDREN_VR”（不带引号）。|
| [ChildVR_2.0.01](attachment/unity/v2.0/ImmersionChildVRUnityIntegration_v2.0.01.unitypackage)</br>[NebulaVR_2.0.01](attachment/unity/v2.0/ImmersionNebulaVRUnityIntegration_v2.0.01.unitypackage)    				|2016/4/15 		|	增加支持LibVR.dll的功能性代码。请手动将LibVR.dll复制到C:\Windows\System32文件夹下。		|

#### Known Issues:
- **2.0.06**, **2.0.07** 版本在 **Unity 5.2.0f3**(Stan pc/ win7 sp1, en) 版本中使用，游戏全屏运行，1)最小化后无法恢复到全屏，程序无响应, 2)游戏运行过程中插拔头显，游戏黑屏。(Unity 5.3 版本无此问题)


----------
###v1.0   

| 版本        					| 发布日期        					| 更新描述  	|
| :----------------------:					|:---------------------------------| :-----	|
| [ChildVR_1.0](attachment/unity/v1.0/ChildVRUnityIntegration.unitypackage)</br>[NebulaVR_1.0](attachment/unity/v1.0/NebulaVRUnityIntegration.unitypackage)    				|2016/4/01 		|	儿童VR和星云VR的第一版SDK代码，参考DK1实现。		|