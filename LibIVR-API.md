#LibIVR Interface API#

----------
**document version:**	1.0  
**author:** Stan  
**date:** 2016/4/13 10:17:10 

[Home](index.html "Home")

## Install Instructions ##
### install automatically ###
- Download **[sdk.zip](attachment/sdk/sdk.zip)** package.
- Uncompress **sdk.zip**.
- Run "**IVR_install.bat**" as administrator.

### install manually ###
- Download dll files which architecture(x86 or x64) you need.
- Mark sure "libIVR.dll" file in your "**%SystemRoot%\system32**" folder.(*NOTE*: architecture **x64** need in **system32**, **x86** need in **syswow64**). You can run **"[IVR_install.bat](attachment/sdk/IVR_install.bat)"** to help you do that.


## Download: ##
x86: [libIVR_v0.05.dll](attachment/sdk/x86/libIVR.dll)   
x64: [libIVR_v0.05.dll](attachment/sdk/x64/libIVR.dll) 


## Basic Module ##
| Method name        					| Comment | Parameter  	| Return |
| ----------------------					|:---------------------------------| :-----	|:-----|
| `int IVR_Init()`						| 初始化		|			| 1 - repeat init; <br/>**0 - successed**;<br/> -1 failed;|
| `int IVR_Deinit()`  					| 卸载 		|			|1 - repeat deinit; <br/>**0 - successed**;<br/> -1 failed;|
| `int IVR_SetDisplayCapturerPath(const char *path)` |设置双屏程序文件路径| path: 双屏程序路径，注意 \ 需要转义||
| `int IVR_StartDisplayCapturer()`		| 启动双屏功能|	| -2 The **"ScreenCapturer.exe"** file can't be found. <br />  -1 - failed;<br />0 - successed; |
| `int IVR_StopDisplayCapturer()`		| 关闭双屏功能| | -1 - failed <br /> 0 - successed|


## Eyeshield ##

| Method name        					| Comment   | Parameter | Return|
| ----------------------					|:------------| :-----	|:-----|
| `int IVR_EnableEyeshield(int level)`		| 启动护眼功能|level: 1 - 一级护眼 （目前只有一级，该值传入1即可）；| -3 - 未初始化; <br /> -2 - 映墨头显设备未发现； <br /> -1 - 失败； <br /> 0 - successed；|
| `int IVR_DisableEyeshield()` | 关闭护眼功能| |同上 |


## Game Stuff ##

| Method name        					| Comment        	| Parameter  	|Return|
| ----------------------					|:-----------------| :-----	|:---|
| `UINT IVR_GetWindowMessage(const char *message)`| 获取消息对应的 WM 值|Message Name 详见下面代码| WM value|
| `int IVR_NotifyGameStart()`		| 通知 IVR 游戏启动（由 Unity/UE 调用） |	||
| `int IVR_NotifyGameStop()`| 通知 IVR 游戏停止(由Unity/UE 调用) |
| `int IVR_GameSendAliveMessage()` | 发送 游戏 “活着” 信息给 IVR(由Unity/UE 调用，需每过n秒发送一次)|
| `bool IVR_IsGameStart()`		| 主动询问是否游戏已启动 |					|**true** - game start.<br>**false** - .. |


##### IVR_GetWindowMessage(const char *message) 

		// 游戏开始消息
		const char *SWM_GAME_START		= "WM_GAME_START";
		// 游戏结束消息
		const char *SWM_GAME_STOP		= "WM_GAME_STOP";
		// 发送游戏“活着”的消息（类似心跳包，但不是通过Socket实现）
		const char *SWM_GAME_ALIVE		= "WM_GAME_ALIVE";
		//映墨头显 HDMI 插入消息
		const char *SWM_IMMER_MONITOR_ADDED		= "WM_IMMER_MONITOR_ADDED";
		//映墨头显 HDMI 移除消息
		const char *SWM_IMMER_MONITOR_REMOVED	= "WM_IMMER_MONITOR_REMOVED";
		//映墨头显 USB 插入消息
		const char *SWM_IMMER_HID_ADDED			= "WM_IMMER_HID_ADDED";
		//映墨头显 USB 移除消息
		const char *SWM_IMMER_HID_REMOVED		= "WM_IMMER_HID_REMOVED";





