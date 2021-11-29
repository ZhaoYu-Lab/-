# window中anaconda安装后jupyter notebook更改启动目录  


1、Anaconda Prompt中 输入 以下并回车  
jupyter notebook --generate-config  
会提示  
Writing default config to: C:\Users\Username\.jupyter\jupyter_notebook_config.py  

2、找到这个文件，打开这个配置文件jupyter_notebook_config.py  
找到下面的  
#c.NotebookApp.notebook_dir = ''  

并修改为下面的  
c.NotebookApp.notebook_dir = 'G:/Notebook'  

3、修改快捷方式的属性  

将目标 里的%。。。%两个百分号之间的内容删除（包括%）  

将起始位置内容删除  

重新启动即可  

