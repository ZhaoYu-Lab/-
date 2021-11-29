Ubuntu18.04 安装 Anaconda3


# 下载 Anaconda3-5.2.0-Linux-x86_64.sh (Ubuntu18.04的对应的Anaconda版本)：
https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/
# 安装
bash Anaconda3-5.2.0-Linux-x86_64.sh
# 结束后输入命令sudo gedit ~/.bashrc打开配置文件
# 在文件最后输入
export PATH="/home/zhaoyu/anaconda3/bin:$PATH"
# 关闭文件输入命令
source ~/.bashrc
# 创建虚拟环境
conda create -n mypytorch python=3.6
# 激活虚拟环境
source activate
conda activate mypytorch

# 查看已有的虚拟环境
conda env list 
# 创建
conda create -n env_name python=x.x
# 删除
conda remove -n env_name --all


# 激活
激活虚拟环境和关闭虚拟环境
conda activate env_name
# 关闭
conda deactivate
 # 环境恢复
 bash Anaconda3-5.2.0-Linux-x86_64.sh -u

# 已经有了环境 ，需要为该环境配置后在jupyter中使用 将虚拟环境添加到Jupyter Notebook
# 打开终端安装ipykernel
conda install ipykernel
# 为已有的环境下载kernel文件
conda install -n mypytorch ipykernel
# 如果我需要为名称为 new 的虚拟环境配置，则输入
conda install -n new ipykernel
# 进入该虚拟环境
source activate new
# 将该环境写入jupyter的kernel中
python -m ipykernel install --user --name 环境名称 --display-name "你想在jupyter中显示的该环境的名称"
eg: python -m ipykernel install --user --name new --display-name "jupyter环境"
# 启动jupyter
jupyter notebook


