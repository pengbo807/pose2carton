# Pose2Carton 

EE228 课程大作业，利用3D骨架控制3D卡通人物。



# Maya 环境配置

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

首先，使用 fbx_parser.py 对 fbx 文件进行解析，得到存储有关节节点定义以及拓扑关系的 txt 文件
（若已有该文件则无需解析）。
然后，使用 transfer.py 脚本，读取该 txt 文件，并返回模型关节名以及其拓扑关系。
最后，根据人体关节的拓扑关系，综合模型关节名、人体关节拓扑图 [1] 找到与人体关节相对应的
关节，将其更新后的序号与人体关节序号一一匹配，存储在 manual_model_to_smpl 中。之后，再次运
行 transfer.py，脚本将会按照给定的匹配信息，将模型与指定动作或者动作序列进行匹配。之后，再使
用 vis.py 脚本，将动作序列可视化，并以 MP4 格式保存。

对于在线模型，我们还需要对其进行蒙皮。正常的模型在 parser 以后，会生成 intermediate.obj、 intermediate.mtl 文件以及.fbm 文件夹。在运行 transfer 脚本后，脚本会自动将.mtl 文件移入 obj_seq_5_3dmodel
文件夹中。我们还需要手动将.fbm 文件夹内的材质文件移到 obj_seq_5_3dmodel 中，再手动编辑该文
件夹下的.mtl 文件，将其中材质的路径改为当前文件夹下的相对路径。
至此蒙皮完成。在 vis.py 中将 use_online_model 改为 True 后，运行脚本，就可以看到带蒙皮的可
视化模型。



# 新增脚本说明

无



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
