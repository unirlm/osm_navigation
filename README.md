# osm_navigation

### 更新：
2019-04-27
* 修改params/base_local_planner_params.yaml中occdist_scale (0.4 -> 0.02). (参考文献：http://kaiyuzheng.me/documents/navguide.pdf ）
* 增大fake_laser_scan节点中障碍物的大小(span 5->15).

2019-04-15
* launch文件取消了osm_helper节点, 增加fake_localization节点，发布odom->map的tf关系


### 使用方法：
STEP 1: 运行 rbx1 模拟机器人
```bash
$ roslaunch rbx1_bringup fake_turtlebot.launch
```

STEP 2: 运行模拟雷达
```bash
$ roslaunch fake_laser_scan fake_laser_scan.launch
```

STEP 3: 运行导航
```bash
$ roslaunch osm_nav nav.launch
```

---
## TIPS
把source添加到.bashrc 就不需要每次都手动打了。
```bash
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
```

