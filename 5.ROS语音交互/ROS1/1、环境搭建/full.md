# 1、环境搭建

# 1、安装Speech\_Lib库

把附件中的Python驱动库文件夹下的py\_install复制到自己的系统的根目录下，然后进入到该文件夹里边，

```batch
cd py_install
sudo python3 setup.py install 
```

```txt
yahboom@raspberrypi:~/Downloads/py_install $ sudo python3 setup.py install
running install
/usr/lib/python3/dist-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
warnings.warn(
/usr/lib/python3/dist-packages/setuptools/command/easy_install.py:146: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
warnings.warn(
running bdist_egg
running egg_info
writing Speech_Lib.egg-info/PKG-INFO
writing dependency_links to Speech_Lib.egg-info/dependency_links.txt
writing top-level names to Speech_Lib.egg-info/top_level.txt
reading manifest file 'Speech_Lib.egg-info/SOURCES.txt'
writing manifest file 'Speech_Lib.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-aarch64/egg
running install_lib
running build_py
creating build/bdist.linux-aarch64/egg
creating build/bdist.linux-aarch64/egg/Speech_Lib
copying build/lib/Speech_Lib/__init__.py -> build/bdist.linux-aarch64/egg/Speech_Lib
copying build/lib/Speech_Lib/Speech_Lib.py -> build/bdist.linux-aarch64/egg/Speech_Lib
byte-compiling build/bdist.linux-aarch64/egg/Speech_Lib/__init__.py to __init__.cpython-311.pyc
byte-compiling build/bdist.linux-aarch64/egg/Speech_Lib/Speech_Lib.py to Speech_Lib.cpython-311.pyc
creating build/bdist.linux-aarch64/egg/EGG-INFO
copying Speech_Lib.egg-info/PKG-INFO -> build/bdist.linux-aarch64/egg/EGG-INFO
copying Speech_Lib.egg-info/SOURCES.txt -> build/bdist.linux-aarch64/egg/EGG-INFO
copying Speech_Lib.egg-info/dependency_links.txt -> build/bdist.linux-aarch64/egg/EGG-INFO
copying Speech_Lib.egg-info/top_level.txt -> build/bdist.linux-aarch64/egg/EGG-INFO
zip_safe flag not set; analyzing archive contents...
creating 'dist/Speech_Lib-0.0.2-py3.11.egg' and adding 'build/bdist.linux-aarch64/egg' to it
removing 'build/bdist.linux-aarch64/egg' (and everything under it)
Processing Speech_Lib-0.0.2-py3.11.egg
Copying Speech_Lib-0.0.2-py3.11.egg to /usr/local/lib/python3.11/dist-packages
Adding Speech-Lib 0.0.2 to easy-install.pth file

Installed /usr/local/lib/python3.11/dist-packages/Speech_Lib-0.0.2-py3.11.egg
Processing dependencies for Speech-Lib==0.0.2
Finished processing dependencies for Speech-Lib==0.0.2 
```

用以下命令检查是否安装成功，

```txt
pip list 
```

```txt
six 1.16.0
smbus2 0.4.2
soupsieve 2.3.2
Speech-Lib 0.0.2
Speech-Lib 0.0.2 
```

# 2、绑定端口

查询USB设备ID，

```txt
1susb 
```

```txt
yahboom@raspberrypi:~ $ lsusb
Bus 004 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 003 Device 002: ID 1a86:7522 QinHeng Electronics CH340 serial converter
Bus 003 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub 
```

新建一个my\_speech.rules文件，终端输入，

```txt
sudo gedit /etc/udev/rules.d/my_speech.rules 
```

把以下内容复制到该文件中，

```javascript
KERNEL=="ttyUSB*",ATTRS{idVendor}=="1a86",ATTRS{idProduct}=="7522",MODE:="0777",SYMLINK+"myspeech" 
```

保存后退出，输入以下指令刷新端口规则文件，

```shell
sudo udevadm trigger
sudo service udev reload
sudo service udev restart 
```

```txt
yahboom@raspberrypi:~ $ ll /dev/myspeech
lrwxrwxrwx 1 root root 7 Feb 27 08:08 /dev/myspeech -> ttyUSBO
yahboom@raspberrypi:~ $ 
```

出现图上的内容则表示绑定成功。