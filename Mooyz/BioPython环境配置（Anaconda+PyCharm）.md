### BioPython环境配置（Anaconda+PyCharm）

#### 1. 软件简介

工欲善其事，必先利其器。Python的学习也是如此。使用Python的过程，离不开包管理器和集成开发环境（Integrated Development Environment，IDE）的帮助。本文推荐的包管理器为Conda，IDE则是PyCharm。相较于Python自带的包管理器PIP，Conda的使用更为便捷与灵活。但我们也并不直接使用Conda，而是使用数据科学中更为常用的Anaconda作为包管理工具。关于Anaconda和PyCharm的简介如下：

Anaconda（[官方网站](https://www.anaconda.com/)）

> Anaconda是一个免费开源的Python和R语言的发行版本，用于计算科学（数据科学、机器学习、大数据处理和预测分析），Anaconda致力于简化包管理和部署。Anaconda的包使用软件包管理系统Conda进行管理。超过1200万人使用Anaconda发行版本，并且Anaconda拥有超过1400个适用于Windows、Linux和MacOS的数据科学软件包。（[维基百科](https://zh.wikipedia.org/wiki/Anaconda_(Python发行版))）

PyCharm（[官方网站](https://www.jetbrains.com/pycharm/)）

> PyCharm是一个用于计算机编程的集成开发环境（IDE），主要用于Python语言开发，由捷克公司JetBrains开发，提供代码分析、图形化调试器，集成测试器、集成版本控制系统，并支持使用Django进行网页开发。PyCharm是一个跨平台开发环境，拥有Microsoft Windows、macOS和Linux版本。社区版在Apache许可证下发布，另外还有专业版在专用许可证下发布，其拥有许多额外功能。（[维基百科](https://zh.wikipedia.org/wiki/PyCharm)）
>

#### 2. 软件安装（Win10）

首先，从[Anaconda官方网站](https://www.anaconda.com/)或[清华大学镜像站](https://mirrors.tuna.tsinghua.edu.cn/anaconda/)下载系统对应的Anaconda版本，本文以Win10 64位版本为例。

下载后，双击exe文件进行安装。

![image-20200915231840234](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915231840234.png)

点击Next。

![image-20200915232422374](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915232422374.png)

软件授权协议，点击I Agree。

![image-20200915231954681](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915231954681.png)

安装类型，这里推荐使用默认的仅为我安装（Just Me），点击Next。

![image-20200915232101322](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915232101322.png)

安装路径选择。

![image-20200915235537817](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915235537817.png)

如果是第一次安装，可以钩选第一项添加路径。点击Install。

![image-20200915232402690](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915232402690.png)

Anaconda安装完成。点击Next。

![image-20200915232512381](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915232512381.png)

如果不想了解Anaconda教程或使用说明，可以直接关闭软件。

安装完成后，使用Win+R打开运行，输入cmd，打开终端，输入Python，如果能显示版本等信息则安装成功。

确认成功后，使用Ctrl+Z退出python，或再次打开终端，使用cd切换到Anaconda安装路径，如“cd D:\Anaconda3”，输入conda list，可以查看安装了哪些包。初次安装的包一般比较老，为了避免之后使用报错，可以输入 conda update --all 命令，把所有包进行更新，在提示是否更新的时候输入 y（Yes）让更新继续，等待完成即可。



下面进行PyCharm的安装。

从[PyCharm官方网站](https://www.jetbrains.com/pycharm/download)载系统对应的PyCharm版本，PyCharm有专业版和社区版两种版本。专业版需付费使用，社区版则是免费使用。尽管社区版相比专业版功能有所删减，但足够学习使用。如果确有需求，可以自行搜索购买或破解方法，本文不建议使用非正版软件。

双击打开下载好的应用。

![image-20200915234235110](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915234235110.png)

点击Next。

![image-20200915234322373](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915234322373.png)

选择合适的安装路径，选好后点击Next。

![image-20200915235150526](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915235150526.png)

四个选项分别为“创建桌面快捷方式”、“添加右键快捷方式”、“添加PyCharm进入PATH”和“关联.py文件”，可以按需求勾选。设置好后点击Next。

![image-20200915235315341](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915235315341.png)

选择创建开始菜单的位置，设置好后点击Install。

![image-20200915235712150](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200915235712150.png)

安装完成后勾选打开PyCharm，点击Finish结束安装。

#### 3. 软件使用

本部分内容为在PyCharm中创建项目并配置Anaconda。

<img src="BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916000657104.png" alt="image-20200916000657104"  />

点击左下角的“Skip Remaining and Set Default”，跳过设置。如需设置（如安装R插件、VIM插件等）可以在软件中随时调整。

![image-20200916001011717](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916001011717.png)

点击“New Project”

![image-20200916001258350](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916001258350.png)

设置项目位置和环境。位置建议不要有空格或中文，Python Interpreter即解释器选择Existing interpreter，点击右侧"..."。

<img src="BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916001519331.png" alt="image-20200916001519331" style="zoom:80%;" />

在路径中找到Anaconda安装目录中的python.exe作为解释器，点击OK。

![image-20200916001647152](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916001647152.png)

点击Create。

![image-20200916001927783](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916001927783.png)

点击左上角File-New-Python File建立一个新的Python文件。

![image-20200916002131638](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916002131638.png)

输入文件名称 Hello World，双击选择Python File。

<img src="BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916002259755.png" alt="image-20200916002259755" style="zoom: 50%;" />



键入第一行代码

`print("Hello World")`

<img src="BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916002459271.png" alt="image-20200916002459271" style="zoom:50%;" />

右击，选择Run “Hello World”，或使用快捷键Ctrl+Shift+F10运行当前文件。

![image-20200916002628775](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916002628775.png)

Anaconda和PyCharm设置大体上就完成了。

下面进行主题和字体的设置。

点击File-Settings

![image-20200916003012083](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916003012083.png)

在这里可以进行PyCharm菜单栏、文件栏等处的主题、字体和字号。

![image-20200916003107849](BioPython环境配置（Anaconda+PyCharm）.assets/image-20200916003107849.png)

如需调整代码的字体和字号等设置，则需要进入Editor-Font。

至此，个性化的Anaconda和PyCharm设置就完成了。希望能够给读者提供一些帮助。