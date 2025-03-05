这个项目我是配合HackRF来跑校园跑的，所以功能能用就行
代码都是ai写出来的，我是小白，主要用途就是gps-sdr-sim的轨迹生成，支持百度、谷歌、高德地图的坐标并且转为WGS-84（来自：https://github.com/wandergis/coordTransform_py）
说人话就是a点到b点的轨迹生成，并且支持速度调节（走路、慢跑、快跑、开车），路程时间是ai算的，速度跟高度都有浮动，支持n个点生成轨迹
使用教程：python start.py
可添加的参数：
  -x, --clear           清空 trajectory.csv 文件后运行。
  -n NEWFILE, --newfile NEWFILE
                        指定新的轨迹文件（不存在则创建）。
  -g, --gaode           使用高德/谷歌坐标（GCJ-02），转换为 WGS-84。注：谷歌坐标需要反转使用
  -b, --baidu           使用百度坐标（BD-09），转换为 WGS-84。

  示例：
  E:\gps>python start.py -g
请输入高德坐标系的起点经纬度，格式为: 经度,纬度 (例如 119.231495,39.865392)
请输入起点经纬度：116.407792,39.989342
请输入终点经纬度（格式: 经度,纬度）：116.409353,39.934766
选择运动模式：1. 走路 2. 慢跑 3. 快跑 4. 开车
请输入模式编号（1-4）：2
继续输入新的经纬度？(输入 'x' 退出)：x

百度坐标获取：https://api.map.baidu.com/lbsapi/getpoint/index.html
高德坐标获取（需要开发者）：https://lbs.amap.com/tools/picker

本人在闲鱼店：兮辰666，可以提供这个脚本的技术支持和代生成轨迹以及gps-sdr-sim解除300秒的限制
跪求路过的大佬帮忙优化一下，百度坐标我没试过，理论上应该可以的
