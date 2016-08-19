# apks安装截图及调试说明文档

------

该文档根据平时工作整理，**适用于公司adb命令初级使用**,如有错漏，请指出 ：

> * ADB调试前置条件
> * ADB连接机顶盒命令
> * ADB卸载及安装apks
> * ADB截图

------

### 1.  ADB调试前置条件
- [x] 主机支持远程连接和（普通机顶盒等可以在设置中打开）
- [x] 操作时候弹出的如提示确认对话框需要点击确认（普通机顶盒连接过程中会弹出对话框）
- [x] 确定本地有adb命令包（可以到各网站下载）
- [x] 确保处于同一网络下

### 2. ADB连接机顶盒命令
```cmd
adb connect ip地址:端口号
```
对于天猫和小米等机顶盒，不需要指定连接端口号。公司机顶盒需要制定端口号5114 

### 3. ADB卸载及安装apks
安装（可以替换当前安装）
```cmd
adb install -r xxx.apks
```
卸载
```cmd
adb uninstall 包名
```

### 4. ADB截图
截图到SD卡：
```cmd
adb shell /system/bin/screencap -p /sdcard/screenshot.png
```

从SD卡保存到本地D盘下：
```cmd
adb pull /sdcard/screenshot.png D:\
```
