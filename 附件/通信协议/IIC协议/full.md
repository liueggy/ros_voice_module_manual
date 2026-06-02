注意：主机设备与语音交互模块的供电电源可以不同，但在连接时必须要共地，才可以提供稳

# 定的通讯电平

# 1.语音交互模块当从机

接收解析主机发送的信号：

等待 IIC 信号中断，若 IIC 有数据接收到，则根据 IIC 接收到的寄存器地址信息，调用对应的函数功能。

数据处理与反馈：

当语音交互模块接收到读取寄存器命令时，则需要调用对应的发送函数，将识别到的数据发送给主机设备。

# 2.IIC设备地址及寄存器功能

语音交互模块的 IIC 从机的设备地址为 0x2b。

<table><tr><td>寄存器</td><td>作用</td></tr><tr><td>0x64</td><td>存放识别到结果的寄存器,主机需要读取1个字节数据,即识别结果的ID号。(未识别到时,结果为0x00)</td></tr><tr><td>0x03</td><td>设置被动播报语音的寄存器,主机需要发送1个字节数据。(发送字节为0x00,0x00为被动播报语类型,</td></tr><tr><td>0x04</td><td>设置功能词播报语音的寄存器,主机需要发送1个字节数据。(发送字节为0x00,0x00为功能词播报语类型,</td></tr><tr><td>0x05</td><td>设置命令词播报语音的寄存器,主机需要发送1个字节数据。(发送字节为0x00,0x00为命令词播报语类型,</td></tr></table>

# 3.获取命令词条。

打开附件中的命令词播报词协议列表V3\_中文文件，能看到通信协议协议以 0xAA、0x55 开头，以 0xFB结尾，中间 2 个字节，分别为功能类型和 ID 号。

<table><tr><td>11</td><td>小车停止</td><td>命令词</td><td>好的,已停止</td><td>主</td><td>AA 55 00 01 FB</td><td>AA 55 00 01 FB</td></tr><tr><td>12</td><td>停车</td><td>命令词</td><td>好的,已停止</td><td>主</td><td>AA 55 00 02 FB</td><td>AA 55 00 02 FB</td></tr><tr><td>13</td><td>小车休眠</td><td>命令词</td><td>好的,已休眠</td><td>主</td><td>AA 55 00 03 FB</td><td>AA 55 00 03 FB</td></tr><tr><td>14</td><td>小车前进</td><td>命令词</td><td>好的,正在前进</td><td>主</td><td>AA 55 00 04 FB</td><td>AA 55 00 04 FB</td></tr><tr><td>15</td><td>小车后退</td><td>命令词</td><td>好的,正在后退</td><td>主</td><td>AA 55 00 05 FB</td><td>AA 55 00 05 FB</td></tr><tr><td>16</td><td>小车左转</td><td>命令词</td><td>好的,正在向左转</td><td>主</td><td>AA 55 00 06 FB</td><td>AA 55 00 06 FB</td></tr><tr><td>17</td><td>小车右转</td><td>命令词</td><td>好的,正在向右转</td><td>主</td><td>AA 55 00 07 FB</td><td>AA 55 00 07 FB</td></tr><tr><td>18</td><td>小车左旋</td><td>命令词</td><td>好的,正在向左旋转</td><td>主</td><td>AA 55 00 08 FB</td><td>AA 55 00 08 FB</td></tr><tr><td>19</td><td>小车右旋</td><td>命令词</td><td>好的,正在向右旋转</td><td>主</td><td>AA 55 00 09 FB</td><td>AA 55 00 09 FB</td></tr><tr><td>20</td><td>关灯</td><td>命令词</td><td>好的,已关灯</td><td>主</td><td>AA 55 00 0A FB</td><td>AA 55 00 0A FB</td></tr><tr><td>21</td><td>亮红灯</td><td>命令词</td><td>好的,已亮红灯</td><td>主</td><td>AA 55 00 0B FB</td><td>AA 55 00 0B FB</td></tr><tr><td>22</td><td>亮绿灯</td><td>命令词</td><td>好的,已亮绿灯</td><td>主</td><td>AA 55 00 0C FB</td><td>AA 55 00 0C FB</td></tr><tr><td>23</td><td>亮花灯</td><td>命令词</td><td>好的,已亮花灯</td><td>主</td><td>AA 55 00 0D FB</td><td>AA 55 00 0D FB</td></tr></table>

当语音交互模块识别到“停车”命令词时，会回应“好的，已停止”，主控可在识别结果寄存器（0x64）上读取到 0x02一个字节数据，该数据与“停车”的发送协议中第 4 个字节相同。

<table><tr><td>AA 55 00 01 FB</td><td>AA 55 00 01 FB</td></tr><tr><td>AA 55 00 02 FB</td><td>AA 55 00 02 FB</td></tr><tr><td>AA 55 00 03 FB</td><td>AA 55 00 03 FB</td></tr><tr><td>AA 55 00 04 FB</td><td>AA 55 00 04 FB</td></tr><tr><td>AA 55 00 05 FB</td><td>AA 55 00 05 FB</td></tr><tr><td>AA 55 00 06 FB</td><td>AA 55 00 06 FB</td></tr><tr><td>AA 55 00 07 FB</td><td>AA 55 00 07 FB</td></tr><tr><td>AA 55 00 08 FB</td><td>AA 55 00 08 FB</td></tr><tr><td>AA 55 00 09 FB</td><td>AA 55 00 09 FB</td></tr><tr><td>AA 55 00 0A FB</td><td>AA 55 00 0A FB</td></tr><tr><td>AA 55 00 0B FB</td><td>AA 55 00 0B FB</td></tr></table>

# 4.播报语词条

播报语词条不会主动播报，必须要主控通过 IIC 设置才会进行播报（命令词条的播报语也可以进行播报）。

主控通过 IIC 在播报寄存器地址（0x03）上写入 一个1个字节，为命令词 ID 号，语音播报模块就会播报对应的语句，0xFF 为普通播报语。

<table><tr><td>84</td><td>这是红色</td><td>命令词</td><td>这是红色</td><td>被</td><td>AA 55 FF 5F FB</td><td>AA 55 FF 5F FB</td></tr><tr><td>85</td><td>这是蓝色</td><td>命令词</td><td>这是蓝色</td><td>被</td><td>AA 55 FF 60 FB</td><td>AA 55 FF 60 FB</td></tr><tr><td>86</td><td>这是绿色</td><td>命令词</td><td>这是绿色</td><td>被</td><td>AA 55 FF 61 FB</td><td>AA 55 FF 61 FB</td></tr><tr><td>87</td><td>这是黄色</td><td>命令词</td><td>这是黄色</td><td>被</td><td>AA 55 FF 62 FB</td><td>AA 55 FF 62 FB</td></tr><tr><td>88</td><td>识别到黄色</td><td>命令词</td><td>识别到黄色</td><td>被</td><td>AA 55 FF 63 FB</td><td>AA 55 FF 63 FB</td></tr><tr><td>89</td><td>识别到绿色</td><td>命令词</td><td>识别到绿色</td><td>被</td><td>AA 55 FF 64 FB</td><td>AA 55 FF 64 FB</td></tr><tr><td>90</td><td>识别到蓝色</td><td>命令词</td><td>识别到蓝色</td><td>被</td><td>AA 55 FF 65 FB</td><td>AA 55 FF 65 FB</td></tr><tr><td>91</td><td>识别到红色</td><td>命令词</td><td>识别到红色</td><td>被</td><td>AA 55 FF 66 FB</td><td>AA 55 FF 66 FB</td></tr><tr><td>92</td><td>初始化完成</td><td>命令词</td><td>初始化完成</td><td>被</td><td>AA 55 FF 67 FB</td><td>AA 55 FF 67 FB</td></tr></table>

例如：

用户需要播放“这是红色”时，主控需要通过 IIC 在播报寄存器（0x03）上写入“0x5F”，语音交互模块即会播报“这是红色”。

<table><tr><td>83</td><td>这是什么垃圾</td><td>命令词</td><td>这是什么垃圾</td><td>主</td><td>AA 55 00 5E FB</td><td>AA 55 00 5E FB</td></tr><tr><td>84</td><td>这是红色</td><td>命令词</td><td>这是红色</td><td>被</td><td>AA 55 FF 5F FB</td><td>AA 55 FF 5F FB</td></tr><tr><td>85</td><td>这是蓝色</td><td>命令词</td><td>这是蓝色</td><td>被</td><td>AA 55 FF 60 FB</td><td>AA 55 FF 60 FB</td></tr><tr><td>86</td><td>这是绿色</td><td>命令词</td><td>这是绿色</td><td>被</td><td>AA 55 FF 61 FB</td><td>AA 55 FF 61 FB</td></tr><tr><td>87</td><td>这是黄色</td><td>命令词</td><td>这是黄色</td><td>被</td><td>AA 55 FF 62 FB</td><td>AA 55 FF 62 FB</td></tr></table>

# 5.播报功能词条

功能词条可以识别到命令词的时候播报，也可以通过iic写入特定的字节播报。

主控通过 IIC 在播报寄存器地址（0x04）上写入 一个1个字节，为命令词 ID 号，语音播报模块就会播报对应的语句，0xFF 为普通播报语。

<table><tr><td>语义标签</td><td>命令词</td><td>功能类型</td><td>播报语句</td><td>播报模式</td><td>发送协议</td><td>接收协议</td></tr><tr><td>1</td><td>欢迎语</td><td>欢迎语</td><td>欢迎使用小亚</td><td>被</td><td>AA 55 01 00 FB</td><td>AA 55 01 00 FB</td></tr><tr><td>2</td><td>休息语</td><td>休息语</td><td>我去休息啦</td><td>主</td><td>AA 55 02 00 FB</td><td>AA 55 02 00 FB</td></tr><tr><td>3</td><td>小亚小亚</td><td>唤醒词</td><td>在的</td><td>主</td><td>AA 55 03 00 FB</td><td>AA 55 03 00 FB</td></tr><tr><td>4</td><td>增大音量</td><td>增大音量</td><td>增大音量</td><td>主</td><td>AA 55 04 00 FB</td><td>AA 55 04 00 FB</td></tr><tr><td>5</td><td>减小音量</td><td>减小音量</td><td>减小音量</td><td>主</td><td>AA 55 05 00 FB</td><td>AA 55 05 00 FB</td></tr><tr><td>6</td><td>最大音量</td><td>最大音量</td><td>最大音量</td><td>主</td><td>AA 55 06 00 FB</td><td>AA 55 06 00 FB</td></tr><tr><td>7</td><td>中等音量</td><td>中等音量</td><td>中等音量</td><td>主</td><td>AA 55 07 00 FB</td><td>AA 55 07 00 FB</td></tr><tr><td>8</td><td>最小音量</td><td>最小音量</td><td>最小音量</td><td>主</td><td>AA 55 08 00 FB</td><td>AA 55 08 00 FB</td></tr><tr><td>9</td><td>开启播报</td><td>开播报</td><td>开启播报</td><td>主</td><td>AA 55 09 00 FB</td><td>AA 55 09 00 FB</td></tr><tr><td>10</td><td>关闭播报</td><td>关播报</td><td>关闭播报</td><td>主</td><td>AA 55 0A 00 FB</td><td>AA 55 0A 00 FB</td></tr></table>

例如：

用户需要播放“这是红色”时，主控需要通过 IIC 在播报寄存器（0x04）上写入“0x01”，语音交互模块即会播报“欢迎使用小亚”。

<table><tr><td>语义标签</td><td>命令词</td><td>功能类型</td><td>播报语句</td><td>播报模式</td><td>发送协议</td><td>接收协议</td></tr><tr><td>1</td><td>欢迎语</td><td>欢迎语</td><td>欢迎使用小亚</td><td>被</td><td>AA 55 01 00 FB</td><td>AA 55 01 00 FB</td></tr><tr><td>2</td><td>休息语</td><td>休息语</td><td>我去休息啦</td><td>主</td><td>AA 55 02 00 FB</td><td>AA 55 02 00 FB</td></tr><tr><td>3</td><td>小亚小亚</td><td>唤醒词</td><td>在的</td><td>主</td><td>AA 55 03 00 FB</td><td>AA 55 03 00 FB</td></tr><tr><td>4</td><td>增大音量</td><td>增大音量</td><td>增大音量</td><td>主</td><td>AA 55 04 00 FB</td><td>AA 55 04 00 FB</td></tr><tr><td>5</td><td>减小音量</td><td>减小音量</td><td>减小音量</td><td>主</td><td>AA 55 05 00 FB</td><td>AA 55 05 00 FB</td></tr><tr><td>6</td><td>最大音量</td><td>最大音量</td><td>最大音量</td><td>主</td><td>AA 55 06 00 FB</td><td>AA 55 06 00 FB</td></tr><tr><td>7</td><td>中等音量</td><td>中等音量</td><td>中等音量</td><td>主</td><td>AA 55 07 00 FB</td><td>AA 55 07 00 FB</td></tr><tr><td>8</td><td>最小音量</td><td>最小音量</td><td>最小音量</td><td>主</td><td>AA 55 08 00 FB</td><td>AA 55 08 00 FB</td></tr><tr><td>9</td><td>开启播报</td><td>开播报</td><td>开启播报</td><td>主</td><td>AA 55 09 00 FB</td><td>AA 55 09 00 FB</td></tr><tr><td>10</td><td>关闭播报</td><td>关播报</td><td>关闭播报</td><td>主</td><td>AA 55 0A 00 FB</td><td>AA 55 0A 00 FB</td></tr></table>

# 5.播报命令词条

命令词条可以识别到命令词的时候播报，也可以通过iic写入特定的字节播报。

主控通过 IIC 在播报寄存器地址（0x05）上写入 一个1个字节，为命令词 ID 号，语音播报模块就会播报对应的语句，0xFF 为普通播报语。

<table><tr><td>11</td><td>小车停止</td><td>命令词</td><td>好的,已停止</td><td>主</td><td>AA 55 00 01 FB</td><td>AA 55 00 01 FB</td></tr><tr><td>12</td><td>停车</td><td>命令词</td><td>好的,已停止</td><td>主</td><td>AA 55 00 02 FB</td><td>AA 55 00 02 FB</td></tr><tr><td>13</td><td>小车休眠</td><td>命令词</td><td>好的,已休眠</td><td>主</td><td>AA 55 00 03 FB</td><td>AA 55 00 03 FB</td></tr><tr><td>14</td><td>小车前进</td><td>命令词</td><td>好的,正在前进</td><td>主</td><td>AA 55 00 04 FB</td><td>AA 55 00 04 FB</td></tr><tr><td>15</td><td>小车后退</td><td>命令词</td><td>好的,正在后退</td><td>主</td><td>AA 55 00 05 FB</td><td>AA 55 00 05 FB</td></tr><tr><td>16</td><td>小车左转</td><td>命令词</td><td>好的,正在向左转</td><td>主</td><td>AA 55 00 06 FB</td><td>AA 55 00 06 FB</td></tr><tr><td>17</td><td>小车右转</td><td>命令词</td><td>好的,正在向右转</td><td>主</td><td>AA 55 00 07 FB</td><td>AA 55 00 07 FB</td></tr><tr><td>18</td><td>小车左旋</td><td>命令词</td><td>好的,正在向左旋转</td><td>主</td><td>AA 55 00 08 FB</td><td>AA 55 00 08 FB</td></tr><tr><td>19</td><td>小车右旋</td><td>命令词</td><td>好的,正在向右旋转</td><td>主</td><td>AA 55 00 09 FB</td><td>AA 55 00 09 FB</td></tr><tr><td>20</td><td>关灯</td><td>命令词</td><td>好的,已关灯</td><td>主</td><td>AA 55 00 0A FB</td><td>AA 55 00 0A FB</td></tr><tr><td>21</td><td>亮红灯</td><td>命令词</td><td>好的,已亮红灯</td><td>主</td><td>AA 55 00 0B FB</td><td>AA 55 00 0B FB</td></tr><tr><td>22</td><td>亮绿灯</td><td>命令词</td><td>好的,已亮绿灯</td><td>主</td><td>AA 55 00 0C FB</td><td>AA 55 00 0C FB</td></tr><tr><td>23</td><td>亮蓝灯</td><td>命令词</td><td>好的,已高蓝灯</td><td>主</td><td>AA 55 00 0D FB</td><td>AA 55 00 0D FB</td></tr></table>

例如：

用户需要播放“这是红色”时，主控需要通过 IIC 在播报寄存器（0x05）上写入“0x01”，语音交互模块即会播报“好的，已停止”。

<table><tr><td>11</td><td>小车停止</td><td>命令词</td><td>好的,已停止</td><td>主</td><td>AA 55 00 01 FB</td><td>AA 55 00 01 FB</td></tr><tr><td>12</td><td>停车</td><td>命令词</td><td>好的,已停止</td><td>主</td><td>AA 55 00 02 FB</td><td>AA 55 00 02 FB</td></tr><tr><td>13</td><td>小车休眠</td><td>命令词</td><td>好的,已休眠</td><td>主</td><td>AA 55 00 03 FB</td><td>AA 55 00 03 FB</td></tr><tr><td>14</td><td>小车前进</td><td>命令词</td><td>好的,正在前进</td><td>主</td><td>AA 55 00 04 FB</td><td>AA 55 00 04 FB</td></tr><tr><td>15</td><td>小车后退</td><td>命令词</td><td>好的,正在后退</td><td>主</td><td>AA 55 00 05 FB</td><td>AA 55 00 05 FB</td></tr><tr><td>16</td><td>小车左转</td><td>命令词</td><td>好的,正在向左转</td><td>主</td><td>AA 55 00 06 FB</td><td>AA 55 00 06 FB</td></tr><tr><td>17</td><td>小车右转</td><td>命令词</td><td>好的,正在向右转</td><td>主</td><td>AA 55 00 07 FB</td><td>AA 55 00 07 FB</td></tr><tr><td>18</td><td>小车左旋</td><td>命令词</td><td>好的,正在向左旋转</td><td>主</td><td>AA 55 00 08 FB</td><td>AA 55 00 08 FB</td></tr><tr><td>19</td><td>小车右旋</td><td>命令词</td><td>好的,正在向右旋转</td><td>主</td><td>AA 55 00 09 FB</td><td>AA 55 00 09 FB</td></tr><tr><td>20</td><td>关灯</td><td>命令词</td><td>好的,已关灯</td><td>主</td><td>AA 55 00 0A FB</td><td>AA 55 00 0A FB</td></tr></table>