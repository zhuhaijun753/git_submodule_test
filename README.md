# Embedded System Integration
## v0.753版本
1.修改

2.修改

3.修改

4.修改

## v0.752
1.修改

2.增加

3.修改



# Decision Control
## 模型V0.756版本改动说明
1、修改驾驶员接管逻辑，

改成没有车道线的时候提醒驾驶员接管，并且系统停止控制；

定位不好时，提醒驾驶员接管，但是系统不会自己退出控制；

2、修改部分建模规范问题

3、修改l1valid、l2valid、r1valid、r2valid这几个接口名称，改为L1Quality、L2Quality、R1Quality、R2Quality

4、修改匝道工况的角度限幅，改为+-180

5、将驾驶员确认换道改为按钮确认

6、修改限速接口

l1VelLimitKmph接融合给的本车道限速；

HDMVelUpperKmph接方向盘限速；

7、将PLKSRampULower设置为标定量

8、修改驾驶员确认换道的可行性

对应模块：LKS2CLOKLeft、LKS2CLOKRight

9、修改提示换道信号

对应模块：LeBuzzer、RiBuzzer

10、恢复DriverTakeOver接口（之前版本错误删除了）

11、修改一次拨杆导致多次换道bug

对应模块：Turn2LeftTrig、Turn2RightTrig

12、屏蔽汇入点限速模块

13、修改高速出口限速模块：如果第二段道路信息行驶方向为前行，则将该模块输出的限速置为道路限速


## base是HW_ADAS_V66_0809WL
1)将驾驶场景触发的换道意图处的换道方向，由原来写成常量1改为依据融合信息取。

2）修改TrgLanePropJudg模块中，分叉目标车道的数值，8改为9。

3）在横向不控制时，将安全检测模块输出的角度强制设置为0.

>>HW_ADAS_V67_0814WL
## base是HW_ADAS_V67_0814WL
1)与鹏飞修改的建模规范集成在一起

>>HW_ADAS_V68_0815WL

## base是HW_ADAS_V68_0815WL

1)继续修改建模规范

2）按照长城8月15号完提供的横向控制优化方案修改模型

3）增加代码接口：

实际方向盘转角：currentStrWhelAngl

>>HW_ADAS_V69_0815WL

## base是HW_ADAS_V69_0815WL

1)修改mainRoadWarningJudge中的连线错误

>>HW_ADAS_V70_0816WL

## base是HW_ADAS_V70_0816WL

1)将期望满足度中的自车期望距离改为最高车速极限距离

2）删除期望满足度中的空车道分支

3)将期望满足度的阈值由0.7改为0.6

4）在换道可行性条件中，增加当前车道类型是 “普通车道(主道)”

5）增加换道意图和换道可行性的稳定性判断。

目前设置的是二者同时成立5个周期以后才发出换道请求

LatDecis/LKS2CLJudg/CLFilt

6）在换道可行性的本车到前方目标可行性中增加条件：

本车道前方最近的目标的距离>(动作距离*0.3)

7）改了一个代码接口名字

CLDirection改为CLDirectionFilt

>>HW_ADAS_V71_0819WL

注：上述修改3属于修改错误，为更易于换道，该值应该变大，修改为0.8（卜玉帅）

## base是HW_ADAS_V70_0819WL

修改横向控制中的表定量：

PKPDataForLKS[25] = { 4.0, 4.0, 4.0, 3.7, 3.2, 3.1, 2.9,2.5, 2.1, 2.0, 2.0,?3.0, 2.9, 2.9, 2.9, 3.0, 3.0,?2.5, 2.4, 2.35, 2.3, 2.1,2.0, 2.0, 2.1 } ;

PLKSFFWgt =1.5;




