# CCU-WAR

**安装JDK**  
1.1 下载JDK  

> 官网：https://www.oracle.com/java/technologies/javase-jdk8-downloads.html  

1.2 将JDK放到指定目录 如：/usr/local/java  
1.3 解压JDK 命令：tar -zxvf jdk包名   
1.4 写入环境变量 如：vi /etc/profile  
1.5 写入内容如下：  
```
export JAVA_HOME=目录
export CLASSPATH=.:${JAVA_HOME}/jre/lib/rt.jar:${JAVA_HOME}/lib/dt.jar:${JAVA_HOME}/lib/tools.jar
export PATH=$PATH:${JAVA_HOME}/bin
```
1.6 更新环境变量 命令：source /etc/profile  
1.7 测试 命令：java -v  

**安装Android SDK**  
2.1 下载Android ADT  

> 地址：http://tools.android-studio.org/index.php/adt-bundle-plugin    

2.2 解压adt 命令：tar -zxvf sdk包名  
2.3 写入环境变量 如：vi /etc/profile  
2.4 写入内容如下：  
```
export ANDROID_HOME=目录
export PATH=${PATH}:${ANDROID_HOME}/tools:${ANDROID_HOME}/platform-tools
```
2.5 更新环境变量 命令：source /etc/profile  

**安装genymotion**  

3.1 下载 genymotion-2.8.0-linux_x64.bin  
> 链接：https://pan.baidu.com/s/1esUU9dq7XNLBn1FDCc9xjg  
> 提取码：k4rn  

3.2 安装`genymotion`  
命令：`sudo ./genymotion-2.4.0_x64.bin`
> 一般安装目录为：/opt/genymobile/genymotions/  

3.3 替换文件  
使用 genymotion_crack 下的文件替换到 genymotion  
`sudo cp -f <替换文件(from)> <被替换文件(to)>`

3.4 出现异常
> **异常：** undefined symbol: xcb_wait_for_reply64  
> **解决：** 将 genymotion 目录下的 libxcb.so.1 删除或是移动到其他的地方即可解决。  
> **异常：** undefined symbol: drmGetDevice2  
> **解决：** 将 genymotion 目录下的 libdrm.so.2 删除或是移动到其他的地方即可解决。  
> **异常：** INSTALL_FAILED_CPU_ABI_INCOMPATIBLE  
> **解决：** 在模拟器中安装Genymotion-ARM-Translation  
> **或使用其他版本 其他版本并没有出现此问题**  

**安装appium**  
4.1 下载 `appium`  
> 官网：https://github.com/appium/appium-desktop/releases/tag/v1.15.1  
4.2 运行 `Appium-linux-1.15.1.AppImage`

**离线安装SDK**  
5.1 下载SDK和SDK System images  
地址：https://www.androiddevtools.cn/  
5.2 将SDK解压到 sdk 文件下的platforms文件夹中  
5.3 将 SDK System images 解压到sdk文件夹下的 system-images 文件夹中 如果没有就手动创建一个  
5.4 tools->options->clear cache  
5.5 创建AVD  
Tools->Manage AVDs->create  
5.6 运行AVD  

**安装Anbox**  
6.1 简洁版安装  
```
sudo add-apt-repository ppa:morphis/anbox-support
sudo apt install -y anbox-modules-dkms
sudo modprobe ashmem_linux
sudo modprobe binder_linux
sudo snap install --devmode --beta anbox
```

**安装xDroid**  
7.1 下载 xDroid  
地址：https://www.linzhuotech.com/index.php/home/index/xdroid.html  
7.2 解压 xDroid 
`tar -zxvf xDroidInstall-x86_64-v3.0007.tar.gz`
7.3 设置安装文件权限 
`chmod +x install.sh`
7.4 执行安装脚本
`./install.sh`
7.5 图形化安装 一直下一步