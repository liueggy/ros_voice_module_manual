打开附件中的命令词播报词协议列表V3\_中文文件，能看到发送协议和接收协议，

# 1.功能性词条解析

根据文件能看到10个功能性词条的发送和接收协议，

<table><tr><td>语义标签</td><td>命令词</td><td>功能类型</td><td>播报语句</td><td>播报模式</td><td>发送协议</td><td>接收协议</td></tr><tr><td>1</td><td>欢迎语</td><td>欢迎语</td><td>欢迎使用小亚</td><td>被</td><td>AA 55 01 00 FB</td><td>AA 55 01 00 FB</td></tr><tr><td>2</td><td>休息语</td><td>休息语</td><td>我去休息啦</td><td>主</td><td>AA 55 02 00 FB</td><td>AA 55 02 00 FB</td></tr><tr><td>3</td><td>小亚小亚</td><td>唤醒词</td><td>在的</td><td>主</td><td>AA 55 03 00 FB</td><td>AA 55 03 00 FB</td></tr><tr><td>4</td><td>增大音量</td><td>增大音量</td><td>增大音量</td><td>主</td><td>AA 55 04 00 FB</td><td>AA 55 04 00 FB</td></tr><tr><td>5</td><td>减小音量</td><td>减小音量</td><td>减小音量</td><td>主</td><td>AA 55 05 00 FB</td><td>AA 55 05 00 FB</td></tr><tr><td>6</td><td>最大音量</td><td>最大音量</td><td>最大音量</td><td>主</td><td>AA 55 06 00 FB</td><td>AA 55 06 00 FB</td></tr><tr><td>7</td><td>中等音量</td><td>中等音量</td><td>中等音量</td><td>主</td><td>AA 55 07 00 FB</td><td>AA 55 07 00 FB</td></tr><tr><td>8</td><td>最小音量</td><td>最小音量</td><td>最小音量</td><td>主</td><td>AA 55 08 00 FB</td><td>AA 55 08 00 FB</td></tr><tr><td>9</td><td>开启播报</td><td>开播报</td><td>开启播报</td><td>主</td><td>AA 55 09 00 FB</td><td>AA 55 09 00 FB</td></tr><tr><td>10</td><td>关闭播报</td><td>关播报</td><td>关闭播报</td><td>主</td><td>AA 55 0A 00 FB</td><td>AA 55 0A 00 FB</td></tr></table>

功能性词条我们可以通过解析协议的第三个字节来区分

<table><tr><td colspan="2">发送协议</td><td>接收协议</td></tr><tr><td>AA 55</td><td>01 00 FB</td><td>AA 55 01 00 FB</td></tr><tr><td>AA 55</td><td>02 00 FB</td><td>AA 55 02 00 FB</td></tr><tr><td>AA 55</td><td>03 00 FB</td><td>AA 55 03 00 FB</td></tr><tr><td>AA 55</td><td>04 00 FB</td><td>AA 55 04 00 FB</td></tr><tr><td>AA 55</td><td>05 00 FB</td><td>AA 55 05 00 FB</td></tr><tr><td>AA 55</td><td>06 00 FB</td><td>AA 55 06 00 FB</td></tr><tr><td>AA 55</td><td>07 00 FB</td><td>AA 55 07 00 FB</td></tr><tr><td>AA 55</td><td>08 00 FB</td><td>AA 55 08 00 FB</td></tr><tr><td>AA 55</td><td>09 00 FB</td><td>AA 55 09 00 FB</td></tr><tr><td>AA 55</td><td>0A 00 FB</td><td>AA 55 0A 00 FB</td></tr></table>

其中第一第二个字节（AA 55）表示帧头，第三个字节表示功能字的ID，第四个字节表示命令词的ID,第五个字节（FB）表示帧尾

# 2.命令词条

命令词条示例如下，命令词中的第四个字节表示ID

<table><tr><td>11</td><td>小车停止</td><td>命令词</td><td>好的,已停止</td><td>主</td><td>AA 55 00 01 FB</td><td>AA 55 00 01 FB</td></tr><tr><td>12</td><td>停车</td><td>命令词</td><td>好的,已停止</td><td>主</td><td>AA 55 00 02 FB</td><td>AA 55 00 02 FB</td></tr><tr><td>13</td><td>小车休眠</td><td>命令词</td><td>好的,已休眠</td><td>主</td><td>AA 55 00 03 FB</td><td>AA 55 00 03 FB</td></tr><tr><td>14</td><td>小车前进</td><td>命令词</td><td>好的,正在前进</td><td>主</td><td>AA 55 00 04 FB</td><td>AA 55 00 04 FB</td></tr><tr><td>15</td><td>小车后退</td><td>命令词</td><td>好的,正在后退</td><td>主</td><td>AA 55 00 05 FB</td><td>AA 55 00 05 FB</td></tr><tr><td>16</td><td>小车左转</td><td>命令词</td><td>好的,正在向左转</td><td>主</td><td>AA 55 00 06 FB</td><td>AA 55 00 06 FB</td></tr><tr><td>17</td><td>小车右转</td><td>命令词</td><td>好的,正在向右转</td><td>主</td><td>AA 55 00 07 FB</td><td>AA 55 00 07 FB</td></tr><tr><td>18</td><td>小车左旋</td><td>命令词</td><td>好的,正在向左旋转</td><td>主</td><td>AA 55 00 08 FB</td><td>AA 55 00 08 FB</td></tr><tr><td>19</td><td>小车右旋</td><td>命令词</td><td>好的,正在向右旋转</td><td>主</td><td>AA 55 00 09 FB</td><td>AA 55 00 09 FB</td></tr><tr><td>20</td><td>关灯</td><td>命令词</td><td>好的,已关灯</td><td>主</td><td>AA 55 00 0A FB</td><td>AA 55 00 0A FB</td></tr></table>

<table><tr><td>AA 55 00 01 FB</td><td>AA 55 00 01 FB</td></tr><tr><td>AA 55 00 02 FB</td><td>AA 55 00 02 FB</td></tr><tr><td>AA 55 00 03 FB</td><td>AA 55 00 03 FB</td></tr><tr><td>AA 55 00 04 FB</td><td>AA 55 00 04 FB</td></tr><tr><td>AA 55 00 05 FB</td><td>AA 55 00 05 FB</td></tr><tr><td>AA 55 00 06 FB</td><td>AA 55 00 06 FB</td></tr><tr><td>AA 55 00 07 FB</td><td>AA 55 00 07 FB</td></tr><tr><td>AA 55 00 08 FB</td><td>AA 55 00 08 FB</td></tr><tr><td>AA 55 00 09 FB</td><td>AA 55 00 09 FB</td></tr><tr><td>AA 55 00 0A FB</td><td>AA 55 00 0A FB</td></tr></table>

例子：

比如我们对模块说小车停止，模块会通过串口发送AA 55 00 01 FB五个字节，我们可以通过主控串口服务函数获取到这一组数据，之后通过解析第四个字节得到ID:01，这个时候就得知现在是小车停止。

# 3.播报语词条

播报语词条不会主动播报，必须要主控通过串口发送指令才会进行播报（命令词条的播报语也可以进行播报）。

<table><tr><td>84</td><td>这是红色</td><td>命令词</td><td>这是红色</td><td>被</td><td>AA 55 FF 5F FB</td><td>AA 55 FF 5F FB</td></tr><tr><td>85</td><td>这是蓝色</td><td>命令词</td><td>这是蓝色</td><td>被</td><td>AA 55 FF 60 FB</td><td>AA 55 FF 60 FB</td></tr><tr><td>86</td><td>这是绿色</td><td>命令词</td><td>这是绿色</td><td>被</td><td>AA 55 FF 61 FB</td><td>AA 55 FF 61 FB</td></tr><tr><td>87</td><td>这是黄色</td><td>命令词</td><td>这是黄色</td><td>被</td><td>AA 55 FF 62 FB</td><td>AA 55 FF 62 FB</td></tr><tr><td>88</td><td>识别到黄色</td><td>命令词</td><td>识别到黄色</td><td>被</td><td>AA 55 FF 63 FB</td><td>AA 55 FF 63 FB</td></tr><tr><td>89</td><td>识别到绿色</td><td>命令词</td><td>识别到绿色</td><td>被</td><td>AA 55 FF 64 FB</td><td>AA 55 FF 64 FB</td></tr><tr><td>90</td><td>识别到蓝色</td><td>命令词</td><td>识别到蓝色</td><td>被</td><td>AA 55 FF 65 FB</td><td>AA 55 FF 65 FB</td></tr><tr><td>91</td><td>识别到红色</td><td>命令词</td><td>识别到红色</td><td>被</td><td>AA 55 FF 66 FB</td><td>AA 55 FF 66 FB</td></tr><tr><td>92</td><td>初始化完成</td><td>命令词</td><td>初始化完成</td><td>被</td><td>AA 55 FF 67 FB</td><td>AA 55 FF 67 FB</td></tr></table>

其中第一第二个字节（AA 55）表示帧头，第三个字节表示播报功能FF的，第四个字节表示需要播报内容的ID,第五个字节（FB）表示帧尾

例字：

但我们需要播报“初始化完成”时，主控需要通过串口发送AA 55 FF 67 FB给语音交互模块，发送完成之后，语音交互模块即可播报“初始化完成”

<table><tr><td>92</td><td>初始化完成</td><td>命令词</td><td>初始化完成</td><td>被</td><td>AA 55 FF 67 FB</td><td>AA 55 FF 67 FB</td></tr><tr><td>93</td><td>第一、第四、第五、第六、第七、第九、第十、第十一、第十二、第十三、第十四、第十五、第十六、第十七、第十八、第十九、第二十、第二十一、第二十二、第二十三、第二十四、第二十五、第二十六、第二十七、第二十八、第二十九、第三十、第三十一、第三十二、第三十三、第三十四、第三十五、第三十六、第三十七、第三十八、第三十九、第四十、第四十一、第四十二、第四十三、第四十四、第四十五、第四十六、第四十七、第四十八、第四十九、第五十、第五十一、第五十二、第五十三、第五十四、第五十五、第五十六、第五十七、第五十八、第五十九、第六十、第六十一、第六十二、第六十三、第六十四、第六十五、第六十六、第六十七、第六十八、第六十九、第七十、第七十一、第七十二、第七十三、第七十四、第七十五、第七十六、第七十七、第七十八、第七十九、第八十、第八十一、第八十二、第八十三、第八十四、第八十五、第八十六、第八十七、第八十八、第八十九、第九十、第九十一、第九十二、第九十三、第九十四、第九十五、第九十六、第九十七、第九十八、第九十九、第一百零一零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零二零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零零0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000</td><td></td><td></td><td></td><td></td><td></td></tr></table>