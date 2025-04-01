# Installation-of-YOLO-environment-in-Ubuntu

## 先教一些ubuntu常用技巧：

1. 按下CTRL+ALT+T即可打开终端
   
2. deb文件安装命令：sudo dpkg -i deb文件名
   eg: sudo dpkg -i google-chrome-stable_current_amd64.deb
   
3. .sh文件执行命令：bash .sh文件名
   eg:  bash Anaconda2-5.2.0-Linux-x86_64.sh
   
4. 鱼香大佬一键安装指令：
   ` wget http://fishros.com/install -O fishros && . fishros`

相当强大的一个指令，包含大多数常用软件和ROS系统一键安装，相当省时省力

# *在此鸣谢鱼香大佬*

# 正文

## 第一步：依旧是安装Anconda

进入清华源，选择Anaconda2-5.2.0-Linux-x86_64.sh这个版本，双击开始下载
![images](https://github.com/luyu512/Installation-of-YOLO-environment-in-Ubuntu/blob/main/pictures/%E6%88%AA%E5%9B%BE%202025-04-01%2020-48-45.png)

下载完成后，进入文件下载位置，右击空白位置，选择在终端中打开
![images](https://github.com/luyu512/Installation-of-YOLO-environment-in-Ubuntu/blob/main/pictures/%E6%88%AA%E5%9B%BE%202025-04-01%2020-56-50.png）

执行命令：`bash Anaconda2-5.2.0-Linux-x86_64.sh `

回车，然后一路按照指引进行下去即可完成安装（ps: 如图所示这一步输入yes）
![images](https://github.com/luyu512/Installation-of-YOLO-environment-in-Ubuntu/blob/main/pictures/%E6%88%AA%E5%9B%BE%202025-04-01%2020-58-58.png)

安装成功后重启终端，会发现绿色名称前会出现（base）字样

若没有出现，不用慌，我来助你！

输入：
```
# luyu改成自己的当初设定的名称
echo ". /home/luyu/anaconda2/etc/profile.d/conda.sh" >> ~/.bashrc
source ~/.bashrc
```
即可成功解决这个问题

## 第二步： 依旧是创建虚拟环境

输入`conda create -n yolo python=3.8`

静待虚拟环境创建完成，

随后输入：`conda activate yolo'

若绿色名称前出现（yolo）字样，则说明虚拟环境创建成功

至此，ubuntu系统下yolo环境已经配置完毕，之后的部署流程同之前的步骤
