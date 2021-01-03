## ROS Qt Deskotp GUI App
***
 简体中文 | [English](./README_en.md)

- 使用qt5实现ros机器人人机界面

- 注意！未经作者的许可，此代码仅用于学习，不能用于其他用途。


- 持续更新中.....

- 欢迎在issues提交bug

## 分支

**~~kinetic 版本分支(分支已合并)~~**
- ~~[kinetic-devel](https://github.com/chengyangkj/Ros_Qt5_Gui_App/tree/kinetic-devel "kinetic-devel")~~

**2. Qml版本分支（待完善）**

- 界面更加美观，功能简单，可作为机器人机载端显示
- [qml_simple](https://github.com/chengyangkj/Ros_Qt5_Gui_App/tree/qml_simple)


**3. Lite branch**

- 此版本为《ROS人机交互软件开发》系列课程中实现的版本，实现了master分支的基本功能，代码易懂
- [simple](https://github.com/chengyangkj/Ros_Qt5_Gui_App/tree/simple)


**4. Windows版本分支**
- [windows_devel](https://github.com/chengyangkj/Ros_Qt5_Gui_App/tree/windows_devel)

**5,rviz菜单树分支**

- 使用rviz自带的菜单树，去实现添加显示图层。master分支所有的图层及菜单均需要手动去写代码实现（并且目前仅支持部分图层显示），此分支调用librviz现成api，所有图层均可以实现,不用去手动创建图层菜单和display

- [rviz_tree](https://github.com/chengyangkj/Ros_Qt5_Gui_App/tree/rviz_tree)

- [![image.png](https://i.postimg.cc/KY0XyzKD/image.png)](https://postimg.cc/2qL9QC71)

***


### 一，功能介绍

#### 1,速度仪表盘

- 使用前须在菜单->设置->话题设置中设置odom话题：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507124144542.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NDQxNjky,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200405102549333.gif)

#### 2, 机器人速度控制
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200405104454149.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NDQxNjky,size_16,color_FFFFFF,t_70)

#### 3, 电量显示

- 使用前须在菜单->设置->话题设置中设置电量话题(Std_msg/Float32)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200405153102508.png)
#### 4, rviz模块
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200405151916473.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NDQxNjky,size_16,color_FFFFFF,t_70)
##### 4.1 订阅map话题
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200408122253344.gif)

##### 4.2 激光雷达图层显示
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200408194648822.gif)

##### 4.3 设置导航初始点
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200411201723417.gif)

##### 4.4 设置导航目标点
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200411201804722.gif)

##### 4.5 定点返航

- 使用前须在菜单->设置->话题设置中设置amcl话题
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200413204212739.gif)

##### 4.6 订阅图像话题

- Provides four image display forms that can display four images at the same time
- 提供四个图像显示窗体，可以同时显示四个图像

![加粗样式](https://img-blog.csdnimg.cn/20200507093831130.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NDQxNjky,size_16,color_FFFFFF,t_70)



##### 4.7 快捷指令
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429204153916.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NDQxNjky,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200429204233788.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NDQxNjky,size_16,color_FFFFFF,t_70)

##### 4.8 显示机器人模型
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200501165154149.gif)

##### 4.9 提供六种rviz工具
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200515184545845.png)

##### 4.10 显示话题列表
[![image.png](https://i.postimg.cc/Z5bGBfgk/image.png)](https://postimg.cc/svL6bJsK)
.
##### 4.11 待完善....
### 二，安装教程

#### 1，首先安装ros对qt pkg的支持

```cpp
sudo apt-get install ros-melodic-qt-create
```

```cpp
sudo apt-get install ros-melodic-qt-build
```
```cpp
sudo apt-get install qtmultimedia5-dev
```

#### 2，编译
Put the package in the ros src package directory：
将软件包放入ros src软件包目录下：
```cpp
catkin_make
```
#### 3,运行
```cpp
rosrun robot_monitor robot_monitor
```
***

### 开源协议
**GNU GPL（GNU General Public License，GNU通用公共许可证）**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200408135643929.png)


- 只要软件中包含了遵循本协议的产品或代码，该软件就必须也遵循 GPL 许可协议，也就是必须开源免费，不能闭源收费，不能作为商用软件。

*GPL 开源协议的主要特点*

- 复制自由 	允许把软件复制到任何人的电脑中，并且不限制复制的数量。

- 传播自由 	允许软件以各种形式进行传播。

- 收费传播 	允许在各种媒介上出售该软件，但必须提前让买家知道这个软件是可以免费获得的；因此，一般来讲，开源软件都是通过为用户提供有偿服务的形式来盈利的。

- 修改自由 	允许开发人员增加或删除软件的功能，但软件修改后必须依然基于GPL许可协议授权。
