# 2、语音控制小车运动

以本公司产品Rosmaster-X3为例，说明如何在程序中调用Speech\_Lib库进行语音识别，进而控制小车/机器人运动。本节课程需要结合Rosmaster-X3小车硬件，这里只做代码解析。首先，我们看下内置的语音指令，

<table><tr><td>功能词</td><td>语音模块识别结果</td><td>语音播报内容</td></tr><tr><td>小车停车</td><td>2</td><td>好的,已停止</td></tr><tr><td>小车前进</td><td>4</td><td>好的,正在前进</td></tr><tr><td>小车后退</td><td>5</td><td>好的,正在后退</td></tr><tr><td>小车左转</td><td>6</td><td>好的,正在向左转</td></tr><tr><td>小车右转</td><td>7</td><td>好的,正在向右转</td></tr></table>

<table><tr><td>功能词</td><td>语音模块识别结果</td><td>语音播报内容</td></tr><tr><td>关灯</td><td>10</td><td>好的,已关灯</td></tr><tr><td>亮红灯</td><td>11</td><td>好的,已亮红灯</td></tr><tr><td>亮绿灯</td><td>12</td><td>好的,已亮绿灯</td></tr><tr><td>亮蓝灯</td><td>13</td><td>好的,已亮蓝灯</td></tr><tr><td>亮黄灯</td><td>14</td><td>好的,已亮黄灯</td></tr><tr><td>打开流水灯</td><td>15</td><td>好的,已打开流水灯</td></tr><tr><td>打开渐变灯</td><td>16</td><td>好的,已打开渐变灯</td></tr><tr><td>打开呼吸灯</td><td>17</td><td>好的,已打开呼吸灯</td></tr><tr><td>显示电量</td><td>18</td><td>好的,已显示电量</td></tr></table>

# 1、启动程序

终端输入，

```batch
ros2 run yahboomcar_voice_ctrl Voice_Ctrl_Mcnamu_driver_X3 
```

```txt
root@jetson-desktop:~# ros2 run yahboomcar_voice_ctrl Voice_Ctrl_Mcnamu_driver_X3
Speech Serial Opened! Baudrate=115200
Rosmaster Serial Opened! Baudrate=115200
X3
imu_link

1.0
1.0
1.0
----create receive threading----
0
4
Go ahead! 
```

# 2、核心代码

代码路径：  
\~/driver\_ws/src/yahboomcar\_voice\_ctrl/yahboomcar\_voice\_ctrl/Voice\_Ctrl\_Mcnamu\_driver\_X3.py   
```python
# 导入相对应的语音库
from Speech_Lib import Speech
# 导入相对应的底层驱动库
from Rosmaster_Lib import Rosmaster
# 创建语音控制对象
spe = Speech()
# 创建底层控制的对象
self.car = Rosmaster()
# 读取语音板识别的结果，speech_r 就是识别的结果，是底层库解析后会返回一个数字，通过这个数字来识别指令
speech_r = spe.speech_read()
if speech_r == 2 or speech_r == 0 :
...
# 写入指令，播报语音结果，这里的发送指令后，底层库会包装打包后发送给语音板，语音板接收到后，发出相对的音频文件
spe. void_write(speech_r)
# 控制小车运动和灯带，直接对接底层库，没有通过 ros 发布
self.car.set_car_motion(vx, vy, angular) # 小车运动
self.car.set_colorful_effect(6, 6, parm=1) # 灯带效果
```