# pygame
# 安装遇到的问题：

## step1.首先更新pip
以下两种方法更新pip均失败
pip install --upgrade pip
pip3 install --upgrade pip
以下方法更新pip成功
python3 -m pip install --upgrade pip

## step2.尝试安装python3下的pygame：
在pypi网站的pygame项目中找到合适的pygame版本，
https://pypi.org/project/pygame/#history
安装包的命名方式如下：pygame-2.0.0.dev3-cp27-cp27m-macosx_10_11_intel.whl
2.0.0是pygame的版本号，cp27代表适用于python2.7,macosx_10_11代表适用于10.11版本的mac
我的mac是10.9版本，但没有合适的pygame版本，无法安装
pygame从1.9.4版本以后都是适用于10.11的macOS，所以放弃python3下的pygame

## step3.安装 python2.7
https://www.python.org/downloads/release/python-2716/ 下载macOS的安装包，根据提示安装
此种方法安装的python2不带pip功能，所有需要手动安装python2.7的pip
执行如下两行安装pip:
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py

## step4. 下载pygame安装包，拷贝到/Users/xintong/下，然后执行如下代码
pip2 install pygame - 1.9.3 - cp27 - cp27m - macosx_10_9_intel.whl
命令行提示安装成功

测试是否安装成功：
import pygame
不报错即为安装成功

## step5. 在pyCharm里也要安装pygame
PyCharm -- Preference -- Project -- Project Interpreter -- + -- 搜索pygame -- 勾选 Special Version 1.9.3
安装成功 -- 测试成功
