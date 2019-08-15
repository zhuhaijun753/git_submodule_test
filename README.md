# Embedded System Integration
## v0.753版本软件功能增加/改动说明
1.修改在城市道路情况下道路类型为默认输出

2.修改车道筛选，修改最小二乘法添加的为0的判断，修改摄像头拟合策略环节

3.修改特征点距离赋值方式

4.修改收费站附近没有车道线导致死机的问题

## v0.752版本软件功能增加/改动说明
1.修改目标绝对速度计算导致的静止目标绝对速度超阈值问题

2.增加了车道线拟合取点的判断条件。增加了添加了索引

3.修改了车道线拟合宽度取值

4.修改了决策信号的车道线偏移

5.增加换道提醒信号

6.修改车道线存在接口

7.修改guid_info_link_pre_from_num json文件bug

8.增加应急车道接口

9.修改R2车道宽度的bug，导致右侧车道宽度小于3米

10.增加SPI CRC校验

## v0.751版本软件功能增加/改动说明
1.修改道路类型的输出

2.修改行车坐标转换及随动区域内目标属性输出

3.修改地图解析，导致保定侧测试崩溃的问题

4.修改navi pack json数据存储

5.修改了行车基准侧选择的Bug

6.修改了地图车道顺序

7.修改navi pack接口

8.目标行车横向最近点异常值处理

9.完善区域划分及随动区域属性信息

10.增加模型log输出

11.修改左前方跨区域目标属性

## v0.75版本软件功能增加/改动说明
1.增加cfg文件，配置控制/无控制版本，城市/高速版本

2.HDMAP新版地图解析，接口修改

3.json文件修改，地图数据拆分小包存储

4.加入激光雷达预处理程序，前方加入角雷达输出，区域划分程序优化

5.融合模块代码review重构

6.修改行车坐标转换程序

7.修改激光雷达输入接口为绝对速度相关程序

8.旁车道近距离角雷达目标输出优化更新

9.增加变长度拟合

10.增加反馈信号传输至MCU侧，以控制IO

11.增加特征点模块

## LC城市换道环境测试版本说明0718
1.增加横向决策模型及相关接口

## LC城市换道环境测试版本说明0717
1.增加纵向控制模型及相关接口

## LC城市换道环境测试版本说明0702
1.修改激光雷达缓存导致SPI死机问题

2.sensor和fusion通信方式修改为sensor侧获取数据后，通知fusion侧取数据，减少通信延迟

3.屏蔽道路融合打印和recodedata()离线数据记录

4.融合周期改为20ms

5.模型代码需要将最新版集成

## LC城市换道环境测试版本说明
1.SPI通信增加CL/CR/RL/RR角雷达数据

2.CL/CR/RL/RR角雷达解析

3.激光雷达增加目标边界点解析

4.共享内存增加目标边界点和单独激光目标结构体数据

5.增加激光雷达目标单独接口(含边界点)及激光雷达离线数据存储

6.增加CL控制模块及相关集成接口(未定标)

7.增加CL控制模块相应LOG输出信息

8.车道线集成接口由set_L1C0，set_L1C1，set_L1Dist，set_L1HeadingAngle修改为set_L1C2，set_L1C3，set_L1C0，set_L1C1；增加决策至融合反馈信息

9.屏蔽desStais信号(在LatDecis.c的HW_ADAS_B.desSatis值默认为1)，纵向最高限速设置为40kmph(在ADIF.cpp的get_velUpperKmph函数)

10.增加过线信号判断

11.增加以决策换道信号侧为基准的车道线拟合

12.增加过线信号与决策信号交互

13.统一边界/拟合的输入源为摄像头

14.该版本目前对应LC控制模型的测试，目标融合部分未集成

## v0.744版本软件功能增加/改动说明
1.更新摄像头可用标志位在预处理模块中的判断

2.更新地图点异常在api函数中直接返回的异常

3.修改行车系NAN值的BUG

4.修改车道线不更新BUG

5.删除预处理排序模块

6.优化地图点重复问题

7.修改全局车道线ID不正确BUG

8.修改激光雷达缓存导致内存溢出问题

9.修改进程间通信方式，由sensor通知fusion数据更新

10.增加对于地图异常数据的判断

11.优化行车系插值时遇到异常点的处理

12.修改异常地图点索引引用会越界问题

## v0.743版本软件功能增加/改动说明
1.更新在拟合源选择策略，优先提供给决策摄像头拟合车道线。

2.加入摄像头车道线曲率等计算

3.修改摄像头前后检测距离赋值问题

4.增加CAN通信filter设置

## v0.742版本软件功能增加/改动说明
1.更改激光雷达angle解析问题

2.修改道路融合边界偏移方式

3.修改log存储bug

## v0.741版本软件功能增加/改动说明
1.修改近距离cut-in时，自车不减速问题

2.增加离线数据record

3.弯道死机问题修改

## v0.74版本软件功能增加/改动说明
1.添加道路融合log输出

2.添加hmi相关发送代码，对应0.73版本的数据结构

3.传感器输入源为全部（包含地图）

4.修改logdebug信息

## v0.73版本软件功能增加/改动说明
1.修改目标横向位置选择问题

2.修改车道线固定宽度问题

## v0.72版本软件功能增加/改动说明
1.增加高精度地图解析模块

2.增加高精度地图融合

3.最高速度提高至100KMPH





