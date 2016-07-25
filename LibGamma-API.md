# LibGamma Interface API #

----------
**document version:**	1.0  
**author:** Stan  
**date:** 2016/4/25 10:10:26 

[Home](README.md "Home")

The only Shield-Eye feature version that just only for **ChildVR**


### dll download: ###
x86:  
  
| 版本 | 发布日期 | 更新描述 |
|:----:|:----:|:----|
|[0.0.2](attachment/sdk-other/x86/v0.0.2/libGamma.dll), [pdb](attachment/sdk-other/x86/v0.0.2/libGamma.pdb)|2016/4/29|- 增加开启、关闭护眼功能的返回状态<br /> - 修改护眼功能仅对“映墨头显”有效|
|[0.0.1](attachment/sdk-other/x86/v0.0.1/libGamma.dll), [pdb](attachment/sdk-other/x86/v0.0.1/libGamma.pdb)|2016/4/25|发布护眼功能模块(ChildVR 特供),目前只有一个护眼级别。<br />护眼参数： (r,g,b,contrast,brightness: **0.88, 0.88, 0.68, 0.6, 0.36**)|
 


| Method name  | Comment | Parameter  	| Return|
| -------------|:------	 | :-----       |:---   |
| `int IVR_Init()`				| 初始化		|	| 0 - successed|
| `int IVR_Destroy()`  				| 卸载 		|			| 0 - successed|
| `int IVR_EnableEyeshield(int level)`		| 启动护眼功能|level: 1 - 一级护眼 （目前只有一级，该值传入1即可）；| -3 - 未初始化; <br /> -2 - 映墨头显设备未发现； <br /> -1 - 失败； <br /> 0 - successed；|
| `int IVR_DisableEyeshield()` | 关闭护眼功能| |同上 |


### configuration tunning tools:
[GammaTunning.exe](attachment/assistant-tools/GammaTunning_v0.0.1.exe)

<br />
---------------------------------

<center>![](img/41.png) </center>
<center> 
###### Suport by Algorithm Team. 
</center>

