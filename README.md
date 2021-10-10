Ubuntu18.04 安装 Anaconda3


1.下载 Anaconda3-5.2.0-Linux-x86_64.sh (Ubuntu18.04的对应的Anaconda版本)：
https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/
2.安装
bash Anaconda3-5.2.0-Linux-x86_64.sh
3.结束后输入命令sudo gedit ~/.bashrc打开配置文件
在文件最后输入
export PATH="/home/zhaoyu/anaconda3/bin:$PATH"
关闭文件输入命令
source ~/.bashrc
