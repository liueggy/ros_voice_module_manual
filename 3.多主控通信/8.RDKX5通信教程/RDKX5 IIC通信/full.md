注意：语音交互模块需要烧录出厂固件，语音芯片到手之后没有刷过固件的则不需要

# 1.实验准备

RDKX5主板  
语音交互模块   
杜邦线

# 2.接线示意图

接线图

<table><tr><td>RDKX5</td><td>语音交互模块</td></tr><tr><td>3</td><td>SDA</td></tr><tr><td>5</td><td>SCL</td></tr><tr><td>GND</td><td>GND</td></tr><tr><td>5V</td><td>5V</td></tr></table>

注意：

下图是新版本的模块的语音交互模块，需要根据引脚线序来接线，不能根据颜色进行接线

![](images/52d852a50f44a95e1d4e91178e0075a302695e578f6788a19cd16507c1473de8.jpg)

<details>
<summary>text_image</summary>

5V GND TX RX
RX1TX1 GND 5V GND SDA SCL 5V
</details>

下图是旧版本的接线，根据引脚线序接线

![](images/810475a7182787422e1d66f01952262482bfc1329077f673ddf1ca0b9a8b5e44.jpg)

<details>
<summary>text_image</summary>

5V GND TX RX
RX/TX1 GND-5V SDA 3CL IND-5V
TRICOM
PROJOSSENIX
NVIDIA X 2024
CX7T4
RDK-X5
DATA
YI/0001A
</details>

将模块滑动模块拨到靠右位置，使用stc固件的串口，

![](images/128f61def8d07c3b03f992242c25e42d6f2014d001499e9a5a28d8f661603d2d.jpg)

<details>
<summary>text_image</summary>

RST
MIC
481237A_Y37_258205
5V GND SCLSDA
5VGNDTX1RX1
YAH800M
YB-MAE01-0.1
</details>

终端输入，之后输入5回车，出现iic设备地址表示正常识别到了

```txt
python3 /app/40pin_samples/test_i2c.py 
```

```txt
sunrise@ubuntu:~$ python3 /app/40pin_samples/test_i2c.py
Starting demo now! Press CTRL+C to exit
List of enabled I2C controllers:
/dev/i2c-0 /dev/i2c-2 /dev/i2c-3 /dev/i2c-4 /dev/i2c-5 /dev/i2c-6 /dev/i2c-7 /dev/i2c-8
Please input I2C BUS num:5
0 1 2 3 4 5 6 7 8 9 a b c d e f
00: -- -- -- -- -- -- -- --
10: -- -- -- -- -- -- -- -- -- -- -- -- --
20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- - 2b
30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- - 2b
40: -- -- -- -- -- -- -- -- -- -- -- -- -- - 2b
50: -- -- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
60: -- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 
70: -- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---
Please input I2C device num(Hex): 
```

# 3.实现效果

以通过修改程序中得代码来选择播报播报内容如下图

![](images/44d0d998b74bd5b1106bbbae35d1b80caaff866a92009a2eb2c2760211bcf2a8.jpg)

<details>
<summary>text_image</summary>

#播报词 Active broadcast content
This_red=0x60
This_green=0x61
This_yellow=0x62
Recognize_yellow=0x63
Recognize_green=0x64
Recognize_blue=0x65
Recognize_red=0x66
init=0x67

def set_voice(data):
    bus.write_byte_data(address, register, data)

set voice(init)
time.sleep(0.5)
</details>

播报的内容可以根据附件提供的命令词播报词协议列表V3\_中文文件查看协议，

其中第一第二个字节AA FF表示的是协议的帧头，第三个字节FF表示的是播报功能，第四个就是播报内容的ID，这里能看到“初始化完成”是16进制的67，所以程序里给寄存器0x03发送0x67即可播报对应内容。第五个字节是结束帧

<table><tr><td>84</td><td>这是红色</td><td>命令词</td><td>这是红色</td><td>被</td><td>AA 55 FF 5F FB</td><td></td><td>AA 55 FF 5F FB</td></tr><tr><td>85</td><td>这是蓝色</td><td>命令词</td><td>这是蓝色</td><td>被</td><td>AA 55 FF 60 FB</td><td></td><td>AA 55 FF 60 FB</td></tr><tr><td>86</td><td>这是绿色</td><td>命令词</td><td>这是绿色</td><td>被</td><td>AA 55 FF 61 FB</td><td></td><td>AA 55 FF 61 FB</td></tr><tr><td>87</td><td>这是黄色</td><td>命令词</td><td>这是黄色</td><td>被</td><td>AA 55 FF 62 FB</td><td></td><td>AA 55 FF 62 FB</td></tr><tr><td>88</td><td>识别到黄色</td><td>命令词</td><td>识别到黄色</td><td>被</td><td>AA 55 FF 63 FB</td><td></td><td>AA 55 FF 63 FB</td></tr><tr><td>89</td><td>识别到绿色</td><td>命令词</td><td>识别到绿色</td><td>被</td><td>AA 55 FF 64 FB</td><td></td><td>AA 55 FF 64 FB</td></tr><tr><td>90</td><td>识别到蓝色</td><td>命令词</td><td>识别到蓝色</td><td>被</td><td>AA 55 FF 65 FB</td><td></td><td>AA 55 FF 65 FB</td></tr><tr><td>91</td><td>识别到红色</td><td>命令词</td><td>识别到红色</td><td>被</td><td>AA 55 FF 66 FB</td><td></td><td>AA 55 FF 66 FB</td></tr><tr><td>92</td><td>初始化完成</td><td>命令词</td><td>初始化完成</td><td>被</td><td>AA 55 FF 67 FB</td><td></td><td>AA 55 FF 67 FB</td></tr></table>

终端输入以下指令运行程序，听到初始化完成，即表示程序正在运行

```batch
python3 iic_test.py 
```

![](images/c114303795db68ae923ff50d025d4f97f202068a78aef6fb814408525373f91f.jpg)

<details>
<summary>text_image</summary>

sunrise@ubuntu:~/Downloads$ python3 iic_test.py
Read data:0
Read data:0
Read data:0
Read data:0
Read data:0
Read data:0
Read data:0
Read data:0
Read data:0
Read data:0
</details>

当我说出唤醒词唤醒之后，说“关灯”调试助手会回复接收10

```txt
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:10
Read data:20 
```

这时候可以打开附件的命令词播报词协议列表V3\_中文文件查看“关灯”的协议

<table><tr><td>20</td><td>关灯</td><td>命令词</td><td>好的,已关灯</td><td>主</td><td>AA 55 00 0A FB</td><td>AA 55 00 0A FB</td></tr><tr><td>21</td><td>亮红灯</td><td>命令词</td><td>好的,已亮红灯</td><td>主</td><td>AA 55 00 0B FB</td><td>AA 55 00 0B FB</td></tr></table>

其中第一第二个字节AA FF表示的是协议的帧头，第三个字节表示的是芯片的十个功能词的ID，第四个就是命令词的ID，这里能看到“关灯”是16进制的0A，十进制是10。第五个字节是结束帧。

说其他的命令词，串口调试助手也会打印相对应得命令词ID，可以自行尝试