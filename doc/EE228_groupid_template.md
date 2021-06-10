# Pose2Carton 

EE228 课程大作业，利用3D骨架控制3D卡通人物。



# Maya 环境配置

这里请简单描述你配置Maya环境的过程。
1.从官网上下载安装maya2020(申请教育权限后）.

2.安装完成后运行maya2020,准备安装pip和numpy
  
  首先要将maya2020重的bin文件夹添加到系统环境变量，如果在cmd中能够运行mayapy说明添加路径成功。
  
  接着安装pip,在cmd中输入：
  
    curl https://bootstrap.pypa.io/pip/2.7/get-pip.py -o get-pip.py
    mayapy get-pip.py
  
  下一步安装numpy,在cmd中输入：
  
    mayapy -m pip install -i https://pypi.anaconda.org/carlkl/simple numpy
  
3.检查安装是否成功，在mayapy中import库：

    import maya

    import maya.standalone

    maya.standalone.initialize(name='python')

    import maya.OpenMaya as om

    import maya.cmds as cmds

    import pymel.core as pm

    import maya.mel as mel

    import numpy as np

    import os

    import glob
    
    
   如果能成功运行，说明安装成功



# 匹配流程

这里请简单描述你熟悉/使用 匹配代码的流程，可以简述对代码的理解/各个函数作用等。



# 新增脚本说明

如果你写了自己的脚本来处理数据或进行可视化，请在这里进行相关说明(如何使用等)； 如果没有，请忽略该模块。



# 项目结果

10组匹配结果

![image](../doc/1update/11.jpg)
![image](../doc/1update/12.jpg)
![image](../doc/1update/13.jpg)
![image](../doc/1update/14.jpg)
![image](../doc/1update/15.jpg)
![image](../doc/1update/16.jpg)
![image](../doc/1update/17.jpg)
![image](../doc/1update/18.jpg)
![image](../doc/1update/19.jpg)
![image](../doc/1update/20.jpg)

5组匹配结果
![image](../doc/1update/51.jpg)
![image](../doc/1update/52.jpg)
![image](../doc/1update/53.jpg)
![image](../doc/1update/54.jpg)
![image](../doc/1update/55.jpg)


# 协议 
本项目在 Apache-2.0 协议下开源

所涉及代码及数据的最终解释权归倪冰冰老师课题组所有

Group 26
