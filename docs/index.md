# 1. 掌控板和mPython介绍
## 1.1. 认识掌控板
### 1.1.1. 掌控板的由来
掌控板由创客教育专家委员会推出，是一款为青少年学习Python编程和创意制造，特别是物联网应用而设计的开源硬件，为普及创客教育而生。掌控板委托创客教育知名品牌Labplus盛思设计、制造与发行，历经十几轮次研究讨论，三次升级改版，是国内第一款专为编程教育而设计的开源硬件！2018年9月15日，掌控板在第六届全国STEAM教育大会上正式发布！

![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giroy72yvsj30sq0jsnds.jpg)
### 1.1.2. 掌控板能做什么？
![](https://tva1.sinaimg.cn/large/007S8ZIlly1gisk29wso9j31ni0myaiu.jpg)
### 1.1.3. 认识掌控板
MicroPython是Python 3编程语言的精简高效实现，包括Python标准库的一小部分，并且经过优化，可在微控制器和受限环境中运行，旨在尽可能与普通Python兼容，以便您轻松地将代码从桌面传输到微控制器或嵌入式系统。MicroPython包含许多高级功能，如交互式提示，任意精度整数，闭包，列表理解，生成器，异常处理等。然而它非常紧凑，可以在仅256k的代码空间和16k的RAM内运行。

mPython掌控是一块MicroPython微控制器板，专为物联网设计。**板载ESP-WROOM-32双核芯片，支持WiFi和蓝牙双模通信。板上集成1.3英寸OLED显示屏、加速度计、地磁传感器、声、光传感器、蜂鸣器、2个物理按键、6个触摸按键。除此外，还有一个阻性输入接口，方便接入各种阻性传感器。丰富多样的传感器和小体积的尺寸、结合蓝牙和WiFi双无线通讯，可现实不同的物联网应用场景。** 内置micropython开源嵌入式python运行环境，可以直接运行python代码，以便您轻松地将代码从电脑传输到掌控板中，且配套mPython图形化编程软件，让您轻松为掌控板编程，体验程序创作的无穷乐趣！

- **元件布局**  
元件布局正面<br>  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giz75f9aa8j30n20fsgmv.jpg)<br>
元件布局背面<br>  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giz74d2w9qj310k0ky440.jpg)<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlly1gisjzs51rfj31sq0l64gr.jpg)<br>
- **引脚定义**<br>  
掌控板正反面有不同的引脚，掌控板正面下边沿的金手指是6个触摸按键，依次为P、Y、T、H、O、N，可监测是否被触摸，比如通过触摸按键控制电机、LED灯等。<br>
掌控板背面下边沿的金手指是通用拓展接口，它将掌控板的输入输出引脚接出，用来控制更多的外接设备,实现更丰富的创意。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlly1gismetak6gj30dr0azq4y.jpg)<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlly1gismfip9laj30d409gdhw.jpg)<br>

## 1.2. 认识mPython
### 1.2.1. mPython概述
mPython是一款支持掌控板使用、易上手、可图形化编程的软件。它具有以下优势：
1. 不依赖网络，可离线安装使用
2. 支持xml、py两种文件的读取
3. 支持“图形编译模式”/“代码编译模式”对应切换
4. 调试便捷。程序编写完成后通过右侧掌控板仿真即可运行验证程序无需连接掌控板，让调试更简单。
5. 教学模式实现双屏互动。直观呈现图形化与代码对照。
6. 支持Windows 7/8/10、Windows XP、Macos、树莓派、虚谷号，用户可根据操作系统选择合适的版本。
### 1.2.2. 软件界面介绍
![](https://tva1.sinaimg.cn/large/007S8ZIlly1gisnl63lnpj311z0ldwjw.jpg)
- **菜单栏：** 可以将程序进行处理，包含了编写程序过程中的一些基本功能（如打开、保存、运行、刷入程序等），学习使用菜单，将会使我们在编写程序的过程中如虎添翼。
- **编程区域/代码区：** 可以自动转换图形化程序为Python代码
- **模块指令区域：** 模块区包含“输入”、“显示”、“Wi-Fi”，“循环”和“逻辑”等类别，每个类别里面分为多种功能模块，可以在空白处“编程区域”按照特定逻辑组合这些功能模块以编写出各种功能的程序。
- **控制台/REPL：** 可以反馈信息，包括硬件信息、代码报错信息等。
### 1.2.3. 相关概念介绍
1. 新建文件</br>
该操作将清除编程区内所有模块和代码。
2. 控制台</br>
也叫REPL（read-evaluate-print loop），具有交互式的特性。可以反馈信息，包括硬件信息、代码报错信息、刷入程序信息、输入指令等。利用它我们可以查看程序是否成功运行，是否成功刷入到掌控板等。
3. 刷入</br>
“刷入”是把代码写入掌控板。因此，“刷入”的代码，在掌控板断电后，再次上电依然可以运行。
## 1.3. 掌控板与mPython的使用
### 1.3.1. 操作步骤
- **第一步：连接掌控板与mPython**   
    掌控板支持盛思开发的mPython图形化编程软件，用USB线一头接入掌控板，另一头接入电脑。打开掌控板的on开关，在软件端看到已正确识别后，在mPython的主界面的“未连接”点击下拉菜单中选择识别出来的掌控板，点击连接。若变成“已连接”表示掌控板与mPython连接成功。
    ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1girp9muoovj31c00u0ws0.jpg)
- **第二步：在编程区域编写程序**  
    在模块指令编程区域编写程序。选择左侧功能模块下的指令，在空白处编程区域编组合这些指令，实现相应功能。
- **第三步：在掌控板运行程序</br>**
    程序编写完成后，在界面右侧的仿真掌控板中，点击【三角按钮】运行程序以查看程序的效果。也可以点击界面上方的【运行】按钮，实现在掌控板中运行程序。【注】：在程序无错误的情况下，若运行后掌控板无反应，可在尝试在【设置】中点击【烧录固件】解决。
- **第四步：刷入程序到掌控板**  
    在确保程序没有错误之后，点击【刷入】将程序输入到掌控板中，以便下次直接在掌控板中查看程序的运行效果。
### 1.3.2. 实现你的第一个程序：Hello World！
1. 需求分析</br>
实现在OLED显示屏上显示Hello,world!
1. 操作步骤
- 连接掌控板与mPython  

- 编写“Hello world”程序  
点击左侧的模块指令区域的”显示”，尝试把相关指令拖动到程序编辑区域。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1girq8kmsdrj30rs094752.jpg)
- 运行程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1girqp6ued3j31yc0oogrx.jpg)
- 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlly1giskp0oi08j31400u01ky.jpg)

# 2. 玩转掌控板之OLED显示图像
## 2.1. OLED显示Hello world
### 2.1.1. 挑战目标
在上一节课程中我们对掌控板和mPython软件做了基本的介绍，并实现了OLED显示Hello，world！  

接下来我们会深入学习OLED设备的应用。本节课主要目标是认识掌控板的OLED屏幕，完成一个简单的程序——用4种语言，分别是中文、英语、韩语、日语，**实现在掌控板OLED屏幕显示“Hello world!”**。
### 2.1.2. 知识点
1. 认识OLED屏幕
2. 掌握OLED显示文本内容
3. 了解屏幕坐标
4. 设置OLED显示位置
### 2.1.3. 信息窗
- **什么是OLED屏幕?**  
掌控板板载1.3英寸OLED显示屏，分辨率128x64。采用Google Noto Sans CJK 16x16字体，支持简体中文，繁体中文，日文和韩文语言。  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gispwz2o6wj30a4078gnq.jpg)
- **“显示”类的模块指令**</br>
想要控制掌控板载的OLED，需要使用mPython中“显示”类的模块指令。<br>  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisq6a5e3oj30jf0k1aco.jpg)<br>
利用这些模块指令，我们可以让OLED显示支持符号，图案，动画、简体中文，繁体中文，英文、日文和韩文语言。<br>
- **OLED的像素**</br>
如果我们把OLED屏幕上的图像放大若干倍，就会发现其实这些图案是由一个个细小的像素点组成的。一个像素可以理解为屏幕上的一个点。当这些点按照指定的顺序排列好，就可以形成成各种各样的图案。而掌控板上的像素点是128 * 64，表示在水平方向x轴含有128个像素点，垂直方向y轴含有64个像素点。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisqdjvipuj30gg0ay430.jpg)
- **OLED显示文本所占用的像素**
    - 每个中文字符占12x16个像素，中文字符指中文输入法下的文字、标点符号等；
    - 每个英文字符占6x16个像素，英文字符指英文输入法下的字母、标点符号等；
    - 数字及数学运算符号（+、-、*、/等）占8x16个像素；
    - 每个字符的坐标值是指组成该字符的左上角第一个像素点位置。
- **通过坐标设置文本显示位置**</br>
前面说到屏幕有128*64个像素点，不同的点位置不同，而我们可以通过这些像素点来构成一个直角坐标系，左上角的坐标为坐标系的原点（0,0），水平方向为X轴，越往右数值越大，由于OLED 屏幕水平方向上分布了128个点，所以X坐标的范围为（0-127）；同样的，垂直方向为Y轴，越往下数值越大，OLED 屏幕的垂直方向上分布了64个点，所以Y坐标的范围为（0-63）。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisq220zmoj30f009gtaj.jpg)<br>
在软件当中，“显示”类的许多指令都需要用坐标，通过更改x，y坐标的数值，确定一个起始位置，我们就可以将图案，文本，显示在不同的位置上。   
### 2.1.4. 操作步骤
最后让我们通过刚刚所学到的知识，尝试让掌控板居中显示4种不同语言的文字。  
**1. 准备文本内容文本内容**   
'你好世界'  
'Hello, world!'  
'안녕하세요'  
 'こんにちは世界'  
**2. 编写程序**  
  我们可以在“显示”指令模块组里面将显示文本指令；显示清空指令；显示生效指令拖拽到白色区域中，摆放顺序如下图所示。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisqjyj3isj30bj055wex.jpg)<br>
显示文本指令：x和y为OLED 显示起始x、y坐标，内容为显示文本内容。  
显示清空指令：熄灭所有屏幕像素点  
显示生效指令：将显示文本内容送至OLED刷新并显示屏幕。  
**3. 运行刷入**  
现在我们需要将写好的程序运行并刷入掌控板。用usb数据线连接上我们的掌控板，依次点击运行、刷入。REPL调试区会显示是否刷入成功。当然在运行刷入到掌控板之前，可以通过掌控板仿真预览效果，若没有达到效果，可进行程序调试。
### 2.1.5. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisqoblcg6j308b07raag.jpg)
## 2.2. OLED显示内置图片
### 2.2.1. 挑战目标
在上一节课程中，我们学会了怎样通过掌控板显示不同语言的文字，当然，OLED屏的功能不仅仅于此，我们可以利用它显示各种内置图像，甚至上传、显示自己本地的图片。  
今天我们来实现“心动”显示，即**在掌控板OLED屏幕中显示一个心形，并使之看起来有“心动”的效果**。同学们，现在是不是就已经心动要跃跃欲试了呢？
### 2.2.2. 知识点
1. 了解bmp和pbm两种图片格式的区别
2. 掌握OLED显示图片内容
3. 掌握调用内置图像
4. 掌握动态显示图像
5. 掌握事件触发
### 2.2.3. 信息窗
- 掌控板载的OLED屏显示图像有两种方法
   - bmp格式的图片，可以用取模软件转换为16进制图像数据，在OLED屏显示图像
   - pbm格式的图片，在OLED屏显示图像
   - 板内内置图片为pbm格式，相对于16进制图像数据，pbm格式占用内存更少，可以使掌控板储存更多的图片，我们也可以将自己制作的图片，转换为pbm或者bmp格式显示在掌控板上。
-  通过mPython烧录固件的掌控板，内置有pbm格式的图片，我们可以通过调用相关指令使用。在“显示”类模块指令的最下方，可以找到显示图像的一系列指令。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gist3b2xhbj30k70io76b.jpg)
-  事件触发  
按下一个按键，就是触发了一个动作，也称之为事件触发。在本程序设计中，当按下按键A，触发显示心形（小）图像，当按下按键B，触发显示心形图像。使用事件触发的方式，能实现动态显示心形的效果。
### 2.2.4. 操作步骤
1. 在“显示”模块指令中找到“内置图像”，通过下拉箭头指示处的”心形”选项，可以选择不同的图案。这里我们选择默认的“心形”。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisthctpbcj30fk06074g.jpg)
2. 前后加上“显示清空”和显示生效<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gistivqq69j30bj05bwel.jpg)
3. 此时显示的是一个静态心形图像
4. 实现心动效果
5. 使用事件触发的方式，当按下按键A，触发显示心形（小）图像，当按下按键B，触发显示心形图像。如此通过控制掌控板的A、B按键达到一个“心动”的效果。<br>
6. 在“输入”模块中选择按键A触发指令，实现事件A<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gistp01xh1j30ef02jaa2.jpg)<br>   
7. 同理实现按键B触发事件
8. 事件A和事件B实现后，程序完成。运行刷入程序即可。
### 2.2.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gistxm5jd2j30ih0hq0u0.jpg)

### 2.2.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisu1lglajj30u0140e82.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisu2haapkj30u00wz4qq.jpg)

## 2.3. OLED显示外部图片
### 2.3.1. 挑战目标
上一节课程中，我们学会了怎样使用掌控板载OLED屏显示内置的pbm格式图像。
在这一节课程，我们将学习如何使用掌控板的OLED屏显示我们自己制作的bmp格式的图片，并通过按键切换显示不同的图片。
### 2.3.2. 知识点
1. 使用“画图”工具将图片转换为128*64格式的bmp图片
2. 学会图片取模的方法
3. 学会将取模的图片显示到OLED屏幕上
4. 了解变量及它的使用
### 2.3.3. 信息窗
- OLED屏幕只能显示颜色深度为1或者就是黑白模式的bmp格式，可以使用Photoshop、“画图”或者其他图片显示软件进行转换。下面以“画图”工具为例。
- 转换好格式的图片需要使用取模工具对图片进行取模。
- 转换的图片大小应该为128*24，也就是掌控板屏幕的大小。
- 所选的图片线条要分明，且颜色不能太过丰富。
### 2.3.4. 操作步骤
**1. 图片处理** <br> 
   **第一步：**<br>
   首先我们需要对图片进行转换，选择图片后右键点击，点击编辑打开画图工具，在画图工具栏中点击“重新调整大小”，在“保持纵横比”的条件下，设置图片的像素，将“垂直”改为64，“水平”改为128。<br>
   ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisx2vw38aj30eu0dcwfr.jpg)<br>
   ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisx3swq56j30gm0d2taa.jpg)  

   **第二步：** 将图片保存为bmp格式。<br>
    ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisx4qdildj30i80igjtj.jpg)<br>
    **第三步：**
    接下来使用取模工具对转换格式后的图片进行取模。网上有PCtoLCD、lcd image converter等取模软件，可根据自己喜好自行选择。以下使用的是Img2Lcd工具。       
        步骤1.打开格式为bmp的图片<br> 
        步骤2.选择参数，输出数据类型[C语言数组]、 扫描模式[水平扫描]、输出灰度[单色]、宽高[128*64]，可以适当亮度、对比度，直到图片显示清晰。<br> 
        步骤3.点击保存，打开保存的”.c”后缀的文件。
        ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisx9cx2j8j30jq0eaac9.jpg)<br>
    **第四步：**<br>
    将保存的文件用记事本程序打开，去掉红色标记的首尾两行。复制中间的16进制图像数据，这些数组就代表着图片的像素点。<br>
    ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisxfpweq1j30hw0fi0ze.jpg)<br>
**2. 编写程序**<br>
将复制的16进制图像数据粘贴在下列指令的空格处，并编写完整程序。
### 2.3.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gisxob8yw0j312o0f8tag.jpg)
### 2.3.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giswm5p3o1j30u20t6u0x.jpg)
### 2.3.7. 扩展延伸
为网站生成二维码。  
参考程序:<br> 
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gitf4ghg6aj309k06mwes.jpg)  
实现效果：
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gitfedwapwj311z0u0x6p.jpg)
## 2.4. 控制不同图像循环显示
### 2.4.1. 挑战目标
前面我们学习了如何显示单张图片，那如何通过按键切换显示不同的图像呢？今天我们就来一起探究以实现该目标吧！
### 2.4.2. 知识点
1. 掌握变量的定义和使用
2. 学会按键触发事件
3. 学会循环控制的思想
### 2.4.3. 信息窗
- 想要利用按键来切换图片，我们可以使用软件里的“变量”类的指令，通过创建一个变量num，来代表按键按下的次数。按键每按动一次，变量便会加1，根据num的数值来决定显示哪一张图片。
- 变量取名时应注意以下规则：  
1. 变量名称可以由字母，数字，下划线组成如；abcd_1；
2. 不能以数字开头，如1_abcd是错的；
3. 变量名区分大小写，如Num和num代表不同变量。
### 2.4.4. 实现步骤
1. 准备3张图像，注意需要用上一节提到的方法将图像转为16进制。<br>
2. 创建变量记录按键按下的次数。<br>     
变量→创建变量→新建变量名为“num”<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjmbm6h477j31c80qemzw.jpg)<br>
初始化变量，使它等于0<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjmbw2fv7xj30pg060jrl.jpg)
按键次数为0时，让屏幕不显示图像，即屏幕清空。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjmek72n44j30oc0c2mxz.jpg)<br>
2. 计算按键次数<br>
在程序中，我们可以利用板载的按键切换三张不同的图片。每当按键A被按下，设定的变量Num就会增加1，当变量达到4时，将变量重置为1，即从头开始显示第一张图片。我们也可以加入一个手动重置的功能，当B键被按下，变量复原为0，手达达到重置按键次数的效果。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjmenuk147j315c0e8jt5.jpg)<br>
3. 使用if条件判断语句，设置图像的显示效果。即当按键值为1，显示图像1；当按键值为2时，显示图像2，以此类推。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjmfco7q1tj316m0jgdhy.jpg)
4. 添加循环，让显示图像的效果循环执行。
### 2.4.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlqe6kjaxj30n10pw0vu.jpg)
### 2.4.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlqqhad65j31400u0x6p.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlqq6haxxj31400u0x6p.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlqqvuzthj31400u0u0x.jpg)
## 2.5. 时钟制作
### 2.5.1. 挑战目标
前面课程中我们已经学习了如何在掌控板的OLED屏中显示图像，包括内置图像和外部图像，今天我们来学习如何制作一个时钟，该时钟就像一个正常的手表一样，秒针会走，时间和网络时间同步。
### 2.5.2. 知识点
1. 学会用掌控板连接WiFi
2. 了解时区的划分
3. 掌握循环语句
4. 掌握时钟显示的方法
### 2.5.3. 信息窗
- 时区：为了解决地球的自转造成各地时间混乱问题，人们划分了时区。规定英国时间为中时区（零时区）、东1-12区，西1-12区。每个时区横跨经度15度，时间相差1小时。最后的东、西第12区各跨经度7.5度，以东、西经180度为界。
- WiFi功能模块：我们可以通过掌控板的WiFi功能模块，通过网络授时来获取国际标准时间。掌控板连接WiFi时，名称要和密码需要完全正确。以北京时间为准，时区选择东8区，授时服务器为time.windows.com。【Tips：若WiFi连接不成功，断开重新连接或者修改WiFi密码后再次运行】
- 时钟制作：初始化一个时钟--->时钟读取时间--->绘制时钟--->时钟显示生效。
- 使用一直重复执行语句，每秒获取一次时间，绘制出当前的状态，让时间不断更新。通过循环，让时钟“走”起来。
### 2.5.4. 操作步骤
1. 在【WiFi功能模块】，找到WiFi连接指令，连接WiFi，并同步网络时间<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gitwwn5bspj30co02qglu.jpg)
2. 在【显示模块】，找到初始化时钟指令，初始化时钟
3. 时钟读取时间
4. 绘制时钟</br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gitxjgs4iqj30bq04ndg1.jpg)
5. 时钟显示生效
6. 在【循环模块】，找到一直重复执行指令，通过循环，控制时钟不断更新时间，实现时钟“走起来”
### 2.5.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gitxoita7nj30cq0960tq.jpg)
### 2.5.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gity4p1rvvj30qx0m5e81.jpg)
# 3. 玩转掌控板之RGB-LED灯
## 3.1. 跑马灯
### 3.1.1. 挑战目标
我们对OLED使用已经有基础的了解，在掌控板中除了OLED会发亮外，其实还有专门亮灯的板载的RGB-LED灯，也是我们接下来学习的重点。今天我们实现跑马灯的效果，即实现三个灯依次（如间隔1s）亮起，保证每次只有一个灯亮且不断循环。我们通过循环控制模块和延时模块来实现。
### 3.1.2. 知识点
1. 认识RGB-LED
2. 点亮RGB-LED
3. 掌握延时功能
4. 掌握循环语句控制灯的循环闪烁
### 3.1.3. 信息窗
- **认识RGB-LED灯**    
mPython掌控板载3颗WS2812灯珠，WS2812是一种集成了电流控制芯片的低功耗的RGB三色灯，R代表红色，G代表绿色，B代表蓝色，可实现256级亮度显示，完成16777216种颜色的全真色彩显示，采用特殊的单线通讯方式控制RGB灯的颜色。而我们掌控板载RGB-LED灯一共三颗，灯号从左往右依次为0,1,2。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gitytm2mnej306505mwel.jpg)<br>
- **RGB-LED模块**</br>
通过使用mPyton“RGB灯”模块来控制掌控板板载RGB-LED<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gityurbi59j30hq05f3z0.jpg)<br>
- **设置灯的颜色**
点击颜色框设置灯珠的颜色，我们有单独点亮一个灯和全部点亮，可以视情况决定使用哪一种方便。</br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gityxpqlgwj309608bt8q.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gityynexuqj308g05udfv.jpg)  
除了选择颜色外，也可以通过修改RGB值改变灯珠颜色,每个值在0-255之间，通过设置不同的数值组合实现不同的颜色，通过这种方式更容易找出自己想要的颜色。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gitz1t2zruj30db028dfv.jpg)
- **关闭灯**  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gitz3943knj305z02g3yd.jpg)
- **延时指令**  
延时指令在【循环模块】中，可以设置下一个程序执行需要等待的时间。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gitz8wnmcbj30df077q3h.jpg)
### 3.1.4. 操作步骤
1. 设置灯亮起的顺序,这里按照0号、1号、2号灯的的顺序依次亮起。
2. 设置0号灯亮起，注意0号灯亮起时，另外两个灯要设置为关闭。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givulsphsqj30ge08qdgg.jpg)
3. 同理，设置1号灯和2号灯亮起。
4. 设置灯与灯之间亮起的间隔时间。
5. 设置循环，循环让灯亮起。
### 3.1.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givuhnuu28j30js0vyjuf.jpg)
### 3.1.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixgn1c17kj30s20r6hdt.jpg)
## 3.2. 双向开关灯
### 3.2.1. 挑战目标
在生活中，我们为了使用方便，常常需要使用多个开关来控制一个光源的亮灭，比如我们的房间内照明灯通常就是使用多个开关来控制，那本节课我们就来学习如何使用掌控板来做一个双向开关灯，按下A键或B键灯亮，再按A键或B键灯灭，也就是A键和B键都可以控制灯的亮灭。
### 3.2.2. 知识点
1. 了解位运算符的按位异或运算符“^”
2. 使用板载A，B键控制板载RGB灯的亮灭
### 3.2.3. 信息窗
- 逻辑运算  
逻辑运算又称布尔运算，通常用来测试真假值。最常见到的逻辑运算就是循环的处理，用来判断是否该离开循环或继续执行循环内的指令。表示方法：<br>
"∨" 表示"或"  
"∧" 表示"与"  
"┐"表示"非"    
"=" 表示"等价"  
1和0表示"真"和"假"  
(还有一种表示,"+"表示"或", "·"表示"与"）
- 异或运算<br>
在程序中我们A键和B键都可以控制灯的亮灭，即按下A键或B键灯亮，再按A键或B键灯灭，我们可以使用按位异或运算符“^”实现效果，按位异或运算是将两个运算分量的对应位按位遵照以下规则进行计算：  
0 ^ 0 = 0, 0 ^ 1 = 1, 1 ^ 0 = 1, 1 ^ 1 = 0
即相应位的值相同的，结果为 0，不相同的结果为 1。
### 3.2.4. 实现步骤
1. 创建“deng"变量。  
首先我们需要创建一个变量，用该变量来控制RGB灯的亮灭，变量名称可以自己随意，我们这里设置变量名称为“deng”。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlmshov7hj30ng0bdjs3.jpg)
2. 将变量的初始值设置为0。  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlmtmuw1xj308o02m3ye.jpg)
3. 我们通过板载A、B按键来控制灯的亮灭，输入模块里找到当按键A(B)按下指令。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjln2sidvaj30e002g3yi.jpg)<br>
下拉选项选择按键。<br>  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjln345zvjj308x042weg.jpg)<br>
4. 在数学模块里选择“异或”运算符。 <br> 
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlmmdieflj30et03faa6.jpg)<br>
下拉找到“异或”符号<br>  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlmn5xlubj309007l749.jpg)  
5. 每当按键A或者按键B被按下，将变量“deng”的值^1然后在赋值给变量“deng”
由于初始化deng变量为0，所以按键按下执行异或运算即deng^1=1；  
此时deng变量为1，按键再次按下执行异或运算deng^1=0；  
依此类推即可实现按键控制deng变量的数值。  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjln69x3v4j30e207cgm3.jpg)
6. 通过判断变量“deng”的数值来决定板载RGB灯的亮灭和OLED屏文本的显示。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlo4u80snj30fd0aqt9w.jpg)
### 3.2.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlo458kwoj30i60j5jtk.jpg)
### 3.2.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlo8gb6exj31410u0u0x.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjlo8zco94j31400u01ky.jpg)

# 4. 玩转掌控板之蜂鸣器与音乐
## 4.1. 制作音乐盒
### 4.1.1. 挑战目标
上一课中，我们学会如何测试噪音来保护我们的听力，但并不是所有的声音都为噪音，有节奏有旋律的声音往往能给带来我们欢乐，点缀我们的生活。  
本节课我们就来学习如何通过掌控板的无源蜂鸣器来播放出动人的旋律。  
掌控板板载无源蜂鸣器，其声音主要是通过高低不同的脉冲信号来控制而产生。声音频率可控，频率不同，发出的音调就不一样，从而可以发出不同的声音，还可以做出“多来米发索拉西”的效果。一起让音乐律动起来吧！
### 4.1.2. 知识点
1. 复习巩固“显示”指令的使用
2. 复习巩固“事件”指令的使用
3. 了解无源蜂鸣器
4. 学习“音乐”模块和触摸按键的使用
### 4.1.3. 信息窗
- 蜂鸣器分为有源蜂鸣器与无源蜂鸣器，这里的“源”不是指电源，而是指震荡源。有源内部带震荡源，所以只要一通电就会叫。无源内部不带震荡源，如果用直流信号无法令其鸣叫，必须用2K~5K的方波去驱动它。有源蜂鸣器往往比无源的贵，就是因为里面多个震荡电路，但程序控制方便。无源蜂鸣器的优点是：价格较低，声音频率可控，可以做出“多来米发索拉西”的效果。<br>
- 我们要用掌控板的无源蜂鸣器来播放不同旋律的音乐，因此需要按键来触发音乐的播放。<br>
- 前面的课程我们使用了板载的A，B按键，但是A,B按键数量有限，所以这次我们使用掌控板的触摸按键，通过触摸不同的按键的来播放不同的旋律，并且可以在OLED显示屏上显示一些提示文本，便于播放切换我们想要听到的旋律，同时为了不在错误的场合制造噪音，我们需要在设置一个按键控制音乐停止。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giy2xitzsgj307f06s751.jpg)
- 触摸按键从左到右依次为P键Y键T键H键O键N键<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giy2xwm36hj307f06raaf.jpg)
### 4.1.4. 操作步骤
1. 在“显示”模组中找到对应指令，首先清空OLED屏。
2. 搭建事件驱动程序。当A按键按下时，停止播放音乐，当触摸不同的键时，播放不同的音乐。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giy6ctw8ogj30ru09u0u0.jpg)<br>
在“音乐”模块中，可以选择自己喜爱的音乐。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giy6lzv8etj30me0kagn2.jpg)<br>
搭建触摸按键p的音乐播放模块。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giy6hdae6nj30jc0aot9w.jpg)<br>
3. 同理，参考步骤2将其他触摸按键对应的音乐播放程序搭建好。
4. 加上相应的提示文本，显示在OLED做作为提示信息。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giy6phh1ncj30uq0dsq5i.jpg)
### 4.1.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giy4qcclxnj30qu186457.jpg)
### 4.1.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giy6rcpkclj30si0pqhdt.jpg)
## 4.2. 歌曲弹奏：小星星
### 4.2.1. 挑战目标
伴奏音乐在舞台表演中是常见的一种增强表演艺术的手段，在平常听起来和其他音乐无异，但是放入到恰当的舞台表演，就显现出独特的魅力。我们知道掌控板上自带一个可以发出声音的蜂鸣器并且可以播放不同的音符。那么是否可以利用掌控板制作一台简易钢琴来为舞台表演伴奏呢？今天我们一起来实现这个目标吧！
### 4.2.2. 知识点
- 了解掌控板触摸按键与音符的关系
- 复习蜂鸣器、触摸按键的应用
- 学习if条件判断的使用：触摸不同的按键实现不同音符的播放
- 了解音调和音符，掌握简单音乐旋律的编程
### 4.2.3. 信息窗
- 触摸按键<br>
现在的智能手机上大多有一个触摸按键，通过手指触摸可以触发相应的功能。触摸按键可以分为四大类：电阻式、电容式、表面声波感应按键、红外线感应按键。而目前大部分的智能机都是采用电容式触摸按键。电容式触摸按键的原理是人体感应电容来检测手机是否存在，如果有手指的话，就会对电流产生一定的感应，从而可以操作智能手机。
掌控板上也有6个触摸按键，用字母“P、Y、T、H、O、N”表示，起到一种开关作用。 6个触摸按键的金色区域为可触发区域。
- 触摸键与音符<br>
掌控板上有触摸按键P、Y、T、H、O、N，当触摸P、Y、T、H、O、N时，会分别响起do、re、mi、fa、so、la不同音符的声音。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjnrqj8ei2j30s80kk0uq.jpg)    
- 声音、音符与频率<br>
我们不管是说话还是唱歌都是在发出声音，那么声音是如何产生的呢？蜂鸣器又是如何产生不同音调的声音呢？<br>  
物理中声音是由物体振动发生的，正在发声的物体叫做声源。物体在一秒钟之内振动的次数叫做频率，单位是赫兹。发出声音物体振动频率不同，可导致发出声音的音调不同，通过改变蜂鸣器发出声音的频率，就可以得到不同音调的声音。频率与音符、字母的对应关系如下表：<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjnsb5v000j30ks05g0t7.jpg)<br>
我们可以通过不断改变蜂鸣器的振动频率，从而达到改变音调，发出优美旋律的效果。<br>
- 认识音调、音符
“播放音符”指令后对应的节拍表示发音持续时间，在mPython中可以理解为1拍=1秒。例如：下图指令中，，蜂鸣器将以1（do）音调持续响1秒钟。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjnsqexq4tj30ps0bg74z.jpg)
### 4.2.4. 实现步骤
1. 在音乐模块中找到播放音符指令<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjnsw8oxwmj30wi04eq3k.jpg)
2. 添加if条件判断语句，实现通过按键触摸触发不同音符的播放![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjo2az3zkkj30ua05oq3p.jpg)
3. 添加循环，让程序重复执行
4. 设置每分钟节拍数,数字越大，音乐的节奏越快。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjo2vlp8thj30t806g0t5.jpg)
### 4.2.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjo2u5xi2jj30u00up7aj.jpg)
### 4.2.6. 实现效果
可实现小星星的弹奏。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjo3n7t3jxj30kt09rgmf.jpg)

## 4.3. 音乐钢琴（需测试windows版本能否上传图片）
### 4.3.1. 挑战目标
听了上一节课那些动听的旋律，是不是也跃跃欲试想自己来独奏一曲了呢？本节课我们就学习如果制作一个简单的音乐钢琴来实现我们的音乐梦。  
我们本节课的主题是制作钢琴，可以在掌控板的OLED屏显示模拟钢琴，并在钢琴键上显示提示音符，然后再通过触摸p、y、t、h、o、n按键，让蜂鸣器发出Do、Re、Mi、Fa、So、La的声音。  
当我们按的时候为了确定“钢琴”是否按下，按的是哪一个音符，我们还可以在触摸按键时在对应位置显示我们的模拟手指。
### 4.3.2. 知识点
1. 学习“函数”模块指令的用法
2. 复习巩固使用OLED屏显示外置图片
3. 学习控制蜂鸣器的声音频率
### 4.3.3. 信息窗
- 音乐钢琴素材  
链接: https://pan.baidu.com/s/1J8IXDRCwfcXGf_43YDiJhA  密码: q984
# 5. 玩转掌控板之传感器
## 5.1. 探测声光
### 5.1.1. 挑战目标
盛夏到了，太阳的光线越来越强烈，为了避免被晒伤，我们应该在太阳光线稍弱的时候选择外出，并且我们可以利用同样的原理来探究一下声音的大小，那我们如何知道外面的光线和声音呢？这节课我们就学习如何使用掌控板来探测光线的强弱和声音的大小。
### 5.1.2. 知识点
1. 学习“映射”模块和“int”模块的使用
2. 学习运用声音、光线传感器
### 5.1.3. 信息窗  
- 我们需要探测光线和声音的大小，所以需要使用掌控板上的麦克风和光线传感器
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givs7vrvevj30j20jan4d.jpg)
- 通过OLED屏来显示声音和光线的大小。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givsx9uyh0j31440bwwgq.jpg)
  为了更好的观察，可以绘制能反映声音和光线变化的进度条。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givsbs2lzgj311u03i3z4.jpg)
- 光线传感器的光线等级区间是0-4095，为了能更好的显示和便于观察，我们需要将区间缩小，这里我们需要使用“映射”模块。“映射”模块的作用就是将一个元素集对应到另一个元素集，可以将原元素集缩小或者放大。在“数学”模组中找到“映射”模块
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givsgacdidj30y602qdg9.jpg) 
因为光线值在变化中会有小数点，为了更好的观察，用整型字符“int”进行取整，只显示整数。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givskjscbjj30x402ejrg.jpg)
同理，声音传感器的设置和显示，和光线传感器的是一样的额。
- OLED识别的数据类型是文本格式（字符串），所以需要将整型映射的光线值、声音值转化为能够被OLED屏识别显示的文本格式。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givstbomonj31080bamz5.jpg)
### 5.1.4. 操作步骤
1. 清空OLED屏。
2. 在指定坐标或者指定行显示文字文本“光线”。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givt2ythpjj30ps03wdg6.jpg)
3. 显示能根据光线强弱来变化的数值。  
首先找到获取光线值的模块。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givt4d90axj30si03674g.jpg)
4. 为了便于OLED显示，使用“映射”，将光线值的范围从0-4095区间对应到0-100区间。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givtof44zgj30rg04cq3c.jpg)
1. 为了更好的观察，用整型字符“int”对光线进行取整，只显示整数。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givtn2oofsj30tw03cq3b.jpg)
6. 接下来我们将整型映射的光线值转化为能够被OLED屏识别显示的文本格式。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givtnz2jnpj310603k74v.jpg)  
7. 用显示文本模块将光线值显示在OLED屏对应的位置。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givtqco4gxj31is04edgw.jpg)
8. 绘制根据光线值变化的进度条。  
X坐标和y坐标确定进度条的显示位置，改变宽、高的值可以改变进度条的大小，进度设置为前面整形取整的光线值。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givtsh0l3nj31gk04iwfg.jpg)
9. 将前面的模块搭建起来，光线值的程序就写好了。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givtuiwu4bj31j00bm776.jpg)
10. 同样的方式，对照2-9步骤，写出声音值的程序。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givtweejq8j31ju0a4jty.jpg)
11. 最后加上显示生效和循环模块，整个程序完成。
### 5.1.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1giuy0jwe9yj30sp0bm0v5.jpg)
### 5.1.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1givrtjuxh6j31420u0u0x.jpg)
## 5.2. 楼道灯
### 5.2.1. 挑战目标
在上一章节中，我们简单的接触了掌控板板载的声音、光线传感器，今天，我们将学习如何应用这两个传感器，制作能够方便我们日常生活的智能电子产品——楼道灯。  
### 5.2.2. 知识点
1. 了解“和”逻辑模块
2. 掌握条件判断语句
3. 运用声音、光线传感器控制板载RGB灯
4. 掌握楼道灯的运作原理
### 5.2.3. 信息窗
- 楼道灯的运作原理  
当周围环境的光线值变暗，楼道灯附带的光线传感器探测到的光线值也随之降低，此时如果有人经过发出声音，楼道灯上的声音传感器所探测到的值就会增大(光线值小于设定的值的同时，声音值大于设定的值，便会点亮灯泡，并持续一段时间)，照亮楼梯供行人通过后，随之关闭。
- 逻辑“和”，也称逻辑“与”，即只有两个操作数都是真，结果才是真。在楼道灯设计中，只有当光线和声音这两个操作数同时满足条件（达到预设的值）时，我们的楼道灯才会打开，所以我们需要用使用逻辑区域指令的”和”。
- 条件判断语句，用来控制灯的亮/灭。
### 5.2.4. 操作步骤
1. 准备数据，在“输入”模块中找到光线和声音指令。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixf4kp2b0j30sw06kq3h.jpg)<br>
2. 设置光线值和声音值，使得二者在满足设定条件时灯亮起或关闭。即在“逻辑”模块中找到这两个指令，完成光线值和声音值的条件判断。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixf8cuxigj30ku06uq3i.jpg)
这里将条件设定为光线值小于等于200，声音值大于等于2000 （您也可以自行修改触发的阈值）<br>  
由于这两个条件是并列判断的，也就是只有当这两个条件同时触发，我们的楼道灯才会打开，所以我们需要用使用逻辑区域指令的”和”。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixfe22c5bj30sg04o3yy.jpg)<br>
3. 准备一个判断语句，用来控制灯的亮灭。即在“逻辑”模块中，找打条件判断语句，搭建起基本的条件判断和执行语句：如果两个条件都成立，点亮板载的3个RGB灯珠，持续十秒后关闭；否则灯为关闭状态。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixfo5grzej30x20fsmz4.jpg)<br>
4. 设置循环和OLED显示，进一步完善程序。<br>
### 5.2.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixf0kx3pkj30zq0te42p.jpg)
### 5.2.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixgit8bogj30qq0t2kjl.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixgjg96ecj30s00pshdt.jpg)
## 5.3. 噪音计
### 5.3.1. 挑战目标
产业革命以来，各种机械设备的创造和使用，给人类带来了繁荣和进步，但同时也产生了越来越多的噪声。噪声不但会对听力造成损伤，也对人们的生活工作有所干扰。今天我们将学习如何使用掌控板制作一个噪音计，来帮助我们判断周围的噪声大小，从而有意识地控制声音的大小，减少噪声污染。
### 5.3.2. 知识点
1. 掌握“如果...否则...”语句以及嵌套
2. 熟练运用逻辑判断指令
3. 熟练运用声音传感器
4. 学会变量的定义和运用
### 5.3.3. 信息窗
- 噪声探测计的设计，少不了会用到掌控板板载的声音传感器。我们可以通过设定声音传感器的不同触发值，将噪音分为4个等级：安静、普通、吵闹、噪音，并在噪音太大时点亮板载的RGB灯进行提示。
- 当需要重复使用某一个指标时，我们可以将该指标定义为变量，变量可以根据情境赋予不同的值。
- “如果...否则...”语句在python中表示为“if…elif…else”表达式可以是一个单纯的布尔值或变量，也可以是比较表达式或逻辑表达式，如果表达式为真，执行语句；而如果表达式为假，则跳过该语句，进行下一个 elif 的判断，只有在所有表达式都为假的情况下，才会执行 else 中的语句。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixinywkszj30mk0acq3m.jpg)
### 5.3.4. 操作步骤
1. 创建voice变量，并把声音传感器得到的值赋给该变量。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixiq4mfjoj31ae0l076l.jpg)<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixisz32q2j30ga040weo.jpg)<br>
2. 接下来，运用逻辑区域的“如果...执行...”指令。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixj79kexnj30k20fm75y.jpg)<br>
对声音值进行判断，设定第一级别的噪音等级。在声音值小于1000时，将其噪音等级设定为“安静”,并用显示指令显示出来，持续一秒。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixk5u4jkej30yu0gc40v.jpg)<br>
1. 设定第二级别的噪音等级；点击“如果，执行”判断指令右方的小齿轮，增加一个“否则如果”<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixjctvi8vj30yq0mgwh3.jpg)<br>
4. 利用逻辑区域指令的“和”指令，将第二级别的噪声数值设定为1000到2000之间，并且将其噪音等级命名为“普通”，并通过OLED显示屏显示，亮一号灯为红色作为提示，持续一秒。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gixk6vyiwtj313w0q2td5.jpg)<br>
5. 同理，设定第三噪音等级，设定范围为2000到3000之间，命名为“吵闹”，并将其显示在led显示屏上，亮1、2号灯为红色，持续一秒；第四噪音等级为大于3000，噪音等级命名为“噪音”，亮1、2、3号灯为红色，持续一秒。<br>
### 5.3.5. 参考程序（缺图）
代码库中的噪音计2
### 5.3.6. 实现效果（缺图）
## 5.4. 水平仪（未写完整）
### 5.4.1. 挑战目标
万丈高楼平地起，建造高楼就像我们搭建积木一样，只有保证建造面的水平，才能建起万丈高楼，但是水平靠我们自己是很难掌握的，因此我们需要借助工具来测量水平，本节课我们就学习如何使用掌控板制作一个简单的水平仪。
### 5.4.2. 知识点
1. 了解三轴加速度计的原理和学会使用“加速度”指令
2. 复习巩固“int”整型指令的使用
3. 复习巩固“映射”指令的使用
## 5.5. 计步器
### 5.5.1. 挑战目标
生命在于运动，健康在于锻炼，我们应该每天坚持运动才能拥有健康的身体。但是运动也要适量，过度运动反而会适得其反，所以有目标、有规划地运动是有很必要的。本节课我们就学习使用掌控板做一个计步器，来协助我们锻炼身体。
### 5.5.2. 知识点
1. 学习“当掌控板摇晃”指令的用法
2. 复习巩固“变量”的使用
3. 复习巩固“逻辑”模块的使用
4. 复习循环的嵌套的使用
5. 复习事件触发的使用
### 5.5.3. 信息窗
- 计步器的设计原理<br>
计步器的设计原理就是当按下按键，在屏幕上显示步数，并且每当我们行走时（即摇晃掌控板），屏幕上的显示步数加一。当走够一定的步数，掌控板会显示提示文本，提醒我们适当休息，如果想继续运动，再按另一个按键可以回到初始状态，重新开始下一轮计步。
- 流程图<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0pl1wkvhj30dy0k3jsd.jpg)
### 5.5.4. 操作步骤
1. 首先创建两个变量，分别命名为“step”“text”（变量名称可以自己设定），并将初始值都设置为0。  
    -  “step”变量代表行走的步数,step等于0时，步数为0（未开始计步或计步清零）；当step不等于0，表述处于计步状态，掌控版每摇晃一次，则计步+1。  
    - “text”变量控制oled的显示文本。当text等于0时，表示只显示初始提示文本信息；当text等于1时，OLED显示计步的相关信息。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0mk74c4tj308n033dfv.jpg)
1. 设置显示文本，显示文本有两种显示状态，即当“text”等于0时或者“text”等于1时,所以需要用到“如果...否则如果”指令。  
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0mn19unzj308x04iaa6.jpg)
    - ①当变量“true”等于0时，oled屏显示初始界面的显示提示文本，在第一行显示应用名称“计步器”，第二行显示运动标语（标语大家可以自由发挥哦），第三行显示提示语“按A键开始计步”，第四行显示提示语“按B键步数清零”，显示生效同时将变量“step”也就是步数清零。  ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0mpsi92gj30h208z75k.jpg)
    - ②当变量“true”等于1时，oled显示计步界面文本，显示提示文本“步数”，在提示文本后显示运动的步数“step”，在显示“step”时，需要进行“转换文本”，将格式转换为可以显示的文本格式，为了让“step”更加便于观察，可将字体设置为较为醒目的字体。  ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0mrlzo9hj30jh07xmy5.jpg)
3. 当text等于1，即OLED显示计步信息时，除了显示步数外，还可以加上一些提示信息。设置步数的目标值，在屏幕下方显示剩余步数，如果步数达到了我们的目标值，显示提示休息文本，否则提示剩余步数以及鼓励等信息，所以需要用到“如果...否则”指令。</br>步数的目标值可以根据自身情况自行决定，可预设步数为7000，这里为了测试，在条件判断时将step设置为5作为临界判断条件。<br> ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0nhczfsxj30kz08x0u5.jpg)<br> 上面用到将多个项目同时显示到一个文本的指令，点击显示文本指令上的小齿轮，将“item”拖到如图位置就可添加显示项目。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0njzbsgyj30ao08c74p.jpg)
4. 将text等于1时的这块程序搭建好。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0nmgtd42j30lr0cq766.jpg)
5. 使用事件模块指令建立触发事件。设置触发指令，按下A键，oled屏显示计步界面文本并设置变量“true”等于1；按下B键，oled屏显示初始提示文本界面，并设置变量“true”等于0。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0nroma9pj309g04zglv.jpg)
6. 实现计步和步数累加功能。行走时，掌控板会摇晃，每当掌控板摇晃一下，证明我们走了一步，将变量“step”的值加1。在"输入“模块中找到该指令。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0ntg1ylbj30de02ht8p.jpg)<br>
注意这只在计步界面，即true等于1时执行该程序。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0nvfh1p9j309t043t8w.jpg)
7. 最后，拼接所有程序模块。同时为了持续获取步数，我们最外层加上循环，至此所有程序完成。
### 5.5.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0obamah8j30jg0rv42g.jpg)
### 5.5.6. 实现效果
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0obttdojj31420u0b2a.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0oc6vegqj31420u01ky.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj0ocnjq18j31260u0b2a.jpg)
# 6. 玩转掌控板之物联网
## 6.1. 物联网应用——微信小程序
### 6.1.1. 挑战目标
随着时代的发展，物联网在生活中的应用无处不在，它能够实现物与物、物与人的泛在连接和信息交互。物联网不仅是目前科技行业的热点领域，也是传统行业关注的重点。它的存在改变了我们的生活方式，为日常生活带来了极大的便利。<br>
掌控板有多个网络服务器，如OneNet 服务器、TinyWebIO 服务器、Blynk服务器和小程序等，通过网络服务器能够实现物联网。今天我们实现通过小程序对掌控板的控制。
### 6.1.2. 知识点
1. 复习WiFi连接
2. 了解什么是物联网、物联网关键技术以及应用场景
3. 掌握通过微信小程序控制掌控板
### 6.1.3. 信息窗
物联网的应用领域涉及到方方面面，在工业、农业、环境、交通、物流、安保等基础设施领域的应用，有效的推动了这些方面的智能化发展，使得有限的资源更加合理的使用分配，从而提高了行业效率、效益。
- 什么是物联网?<br>物联网（The Internet of Things，简称IOT）是指通过 各种信息传感器、射频识别技术、全球定位系统、红外感应器、激光扫描器等各种装置与技术，实时采集任何需要监控、 连接、互动的物体或过程，采集其声、光、热、电、力学、化 学、生物、位置等各种需要的信息，通过各类可能的网络接入，实现物与物、物与人的泛在连接，实现对物品和过程的智能化感知、识别和管理。物联网是一个基于互联网、传统电信网等的信息承载体，它让所有能够被独立寻址的普通物理对象形成互联互通的网络。
- 物联网关键技术<br>
  - 射频识别技术
  - 传感网
  - M2M系统框架
  - 云计算
- 物联网的应用<br>
  - 智能交通<br>物联网技术在道路交通方面的应用比较成熟。随着社会车辆越来越普及，交通拥堵甚至瘫痪已成为城市的一大问题。对道路交通状况实时监控并将信息及时传递给驾驶人，让驾驶人及时作出出行调整，有效缓解了交通压力；高速路口设置道路自动收费系统(简称ETC)，免去进出口取卡、还卡的时间，提升车辆的通行效率;公交车上安装定位系统，能及时了解公交车行驶路线及到站时间，乘客可以根据搭乘路线确定出行，免去不必要的时间浪费。
  - 智能家居<br>智能家居就是物联网在家庭中的基础应用，随着宽带业务的普及，智能家居产品涉及到方方面面。家中无人，可利用手机等产品客户端远程操作智能空调，调节室温，甚者还可以学习用户的使用习惯，从而实现全自动的温控操作，使用户在炎炎夏季回家就能享受到冰爽带来的惬意;通过客户端实现智能灯泡的开关、调控灯泡的亮度和颜色等等; 插座内置Wifi，可实现遥控插座定时通断电流，甚者可以监测设备用电情况，生成用电图表让你对用电情况一目了然，安排资源使用及开支预算;智能体重秤，监测运动效果。内置可以监测血压、脂肪量的先进传感器，内定程序根据身体状态提出健康建议; 智能摄像头、窗户传感器、智能门铃、烟雾探测器、智能报警器等都是家庭不可少的安全监控设备，你及时出门在外，以在任意时间、地方查看家中任何一角的实时状况，任何安全隐患。看似繁琐的种种家居生活因为物联网变得更加轻松、美好。
  - 公共安全<br>近年来全球气候异常情况频发，灾害的突发性和危害性进一步加大，互联网可以实时监测环境的不安全性情况，提前预防、实时预警、及时采取应对措施，降低灾害对人类生命财产的威胁。

### 6.1.4. 操作步骤
- **小程序端**
1. 第1步<br>
打开微信搜索“掌控板物联网”小程序进行授权、登陆。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj1zhzrh89j30ku11275s.jpg)
2. 第2步<br>
添加掌控板，给掌控板取个名字，填上掌控板的mac地址。Mac地址为掌控板正面左下角那12为字母和数字。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj1zjj75adj30ku112abn.jpg)
3. 第3步<br>
配置掌控板的应用模板，添加应用。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj1zlerubij30de0oumz4.jpg)
4. 第4步<br>
给应用取个名称，添加想要的组件，系统会把默认的组件显示出来，并规定好data0到data5的name关键字，掌控板上编程要根据这些name关键字进行相应的操作。我们可以选择修改组件名字，以便我们后面查看使用。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj1znk0yy7j30ku112wg0.jpg)
5. 第5步<br>
选择应用。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj1zoepa7hj30ku112gmg.jpg)<br>
至此，小程序端的配置已经完成。请注意现在还没有和掌控板连接，所以还是显示“离线”。我们需要通过mPython给掌控板刷入程序。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj1zrzcmq4j30de0ouabl.jpg)
- **mPython端**
1. 第1步<br>
注册、登录，注意要用绑定微信的手机号进行注册，这样掌控板才能获取到小程序端配置的信息。
2. 第2步<br>
点击左边的物联网——微信小程序，将这三个块拖出排列好，这些参数都是从微信小程序上自动获取，不用修改。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj201cfnuej30hi0pd42i.jpg)

3. 设置WiFi连接<br>在第一个指令处设置你自己路由器的wifi名称和密。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj204j0vpdj30c901tq2x.jpg)<br>连接WiFi时提示连接失败，可试着修改WiFi密码以及重新烧录固件来解决。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj22p780kpj309502d0sq.jpg)
4. 逻辑代码编写
   - 这里我们可以看到多了两个变量。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj20alot5nj30c305nt94.jpg)<br>这两个变量_name表示组件名，_value表示组件的值。对应小程序上配置的组件信息。
   - 接下来就是利用这两个变量，进行逻辑代码的编写。这里以"Field"输入框组件为例。若我们希望在小程序上输入文本信息（像掌控板发送的文本信息）显示在OLED屏幕上，我们可以这样编写我们的代码。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj215qua2fj30ex05adgi.jpg)<br>
    又如我们利用开关按钮控制掌控板播放音乐。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj216pz4qbj30e407jjs8.jpg)<br>
    其他模块的逻辑代码同理，根据自己的需求来自定义。<br>
    我们还可以实现掌控板向小程序发送信息，如在程序的最后这个模块，我们实现每隔1秒收集一次掌控板声音值，并让声音值在小程序上的折线图上显示。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj21bq6ghnj30du046t8x.jpg)
5. 程序编写后，连接掌控板，并点击运行和刷入。
6. 程序刷入后，我们再回到微信小程序，等待10秒后刷新一下界面，如果“离线“变为”在线“，我们就可以通过微信小程序控制掌控板了。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj225bk5wgj30ku112wg2.jpg)<br>小程序界面，进入操作界面后就可以通过组件控制掌控板或查看掌控板反馈的数据了。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj228a32ckj31120kudh3.jpg)<br>
### 6.1.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2w0ackxaj30la0bsmz1.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2w24yuzsj30p21220y8.jpg)
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2w32a3d2j30og0imtb9.jpg)
### 6.1.6. 实现效果（缺图片、拍个视频）
## 6.2. 物联网应用——TinyWebIO
### 6.2.1. 挑战目标
掌控板有无线上网的wifi功能模块，具有连接网络的功能。我们可以通过网络将手机/电脑和掌控板连接起来，通过在网页上输入一个网址，进入到控制界面实现对掌控板的控制。
### 6.2.2. 知识点
1. 复习wiFi连接
2. 学会获取掌控板IP
3. 掌握配置TinyWebIO和启动服务器
4. 学会掌控板和TinyWebIO连接的步骤
5. 实现掌控板和TinyWebIO的信息交互
### 6.2.3. 信息窗
### 6.2.4. 实现步骤
1. 连接WiFi<br>要实现TinyWebIO对掌控板的控制，首先需要将要TinyWebIO和掌控板处于同一个网络状态。所以第一步是实现掌控板连接网络，输入WiFi名称和密码。![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2w7d1455j30kq03kglx.jpg)
2. 获取掌控板IP信息<br>
要控制掌控板，得知道掌控板的IP地址<br>
为了方便我们取读到这块掌控板的地址和服务器启用密码，将这些信息显示在OLED上！先将OLED屏幕清空，再将OLED第1行显示地址和TinyWebIO服务器端口号（TinyWebIO服务器的端口号是：8888）。这里用到了WiFi配置信息：IP指令，这个指令可以取读到掌控板的IP地址，因为获取到的数据是属于数据类型，所以需要用“转换文本”将数据类型的IP地址转换成字符串类型显示输出。再增加一个转换文本项目用来显示TinyWebIO服务器的端口号：8888。最后让OLED生效，就可以在屏幕上看到“通关钥匙”了！<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2wbaai3pj30wi0bi760.jpg)
程序运行后，OLED上显示掌控板IP信息如下：
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2wdogui5j31410u07wi.jpg)
1. 添加硬件拓展：TinyWebIO服务器<br>在功能模块栏中，点击“添加”。![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2wi1c071j30da09igm1.jpg)![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2wfz1jqlj31c70u0guh.jpg)<br>配置好之后，在功能模块区域就可以看到这个扩展。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2wmxi69wj310k0s0gqs.jpg)
2. 配置TinyWebIO，启动服务器<br>将掌控板连网，并将IP地址和服务器启用密码在OLED上显示后，开始对服务器进行功能设置。我们用到的服务器是TinyWebIO，我们可以从中选择我们会用到的功能，对它进行设置。“设置TinyWebIO客户端参数”在这条指令上已经默认了一些设置。<br>
    - TinyWebDB服务器的地址：可以直接和服务器联通。
    - 向服务器发送数据项：这个设置可以让我们在手机上取读到掌控板测量的光线值、声音值等。
    - 从服务器中读取数据：这个设置可以在手机上下达指令通过服务器传送给掌控板，让掌控板做出对应的指令动作，比如开灯、关灯、屏幕显示文字等。
    - 存取服务器的时间间隔：服务器会一直更新数据，这条指令上已经有初始的设置，但你可以根据实际情况进行修改。<br>
设置好TinyWebIO的功能后，启动TinyWebIO服务器，让它开始工作。有两个工作状况选项：前台运行、后台运行。前台运行，服务器响应速度比较快，工作效率高；而后台运行，服务器响应比较慢，工作效率低，因此我们使用前台运行服务器。至此代码编写如下：<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2wufsj8lj30w20l078z.jpg)
5. 运行程序<br>
程序运行后，在控制台可以看到掌控板的链接地址。复制该地址在浏览器中访问<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2wxyda24j30ie0983ze.jpg)
6. 实现信息交互<br>
在浏览器中访问，看到界面如下(注意电脑/手机连接的WiFi和掌控板连接的WIFI需要相同)：<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2x0niz42j31by0fgabg.jpg)点击storeavalue可以写入数据，点击getvalue可以读取数据。
    - 写入数据<br>写入数据功能实现控制掌控板输出设备，比如让掌控板第二个RGB-LED灯亮绿色。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2xg60i5jj30mu0mkabg.jpg)<br>在掌控板中看到的效果。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2xkeo5yej31400u04qq.jpg)<br>控制音乐播放，如这里播放《歌唱祖国》这首歌曲。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2y484fq2j30y80qo75v.jpg)<br>这里可能有同学会问怎么知道“标签”和“数值”设置为多少呢？这里有个小技巧。标签就看TinyWebIO的配置信息。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2y81r7flj30tm0bcmzw.jpg)这里显示的是目前支持的数据项。<br>数值的设置，在mPython中用图形化编程，后转换为代码，查看对应的值。如播放音乐，图形化指令为：<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2yggvmg1j30j802yjrk.jpg)接着点击代码，找到相应的代码，就能看到对应的标签值。<br>![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2yhlsmpuj30y2048weo.jpg)
    - 读取数据功能<br>如读取掌控板获取到的声音值![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2xr4whizj314k0j40u9.jpg)
### 6.2.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gj2ylwundvj30xm0mywiz.jpg)
### 6.2.6. 实现效果
见“实现步骤”中的说明。
## 6.3. 物联网应用——MQTT(EasyLot)
### 6.3.1. 挑战目标
通过 Easy IoT 物联网平台发送消息，在掌控板上显示效果。
### 6.3.2. 知识点
1. 了解MQTT通信机制
1. 学习Easy IoT 平台的连接
2. 掌握使用MQTT订阅主题和发布消息
### 6.3.3. 信息窗
- 什么是MQTT？<br>
MQTT（Message Queue Telemetry Transport）,遥测传输协议，提供订阅/发布模式，更为简约、轻量，易于使用，针对受限环境（带宽低、网络延迟高、网络通信不稳定），可以简单概括为物联网打造。MQTT是一种基于发布 - 订阅的“轻量级”消息传递协议，用于在TCP / IP协议之上使用，它适用于需要“小代码占用”或网络带宽有限的远程位置的连接。 能实现一对多通信（人们称之为发布或订阅型）的协议。它由3 种功能构成，分别是中介（broker）、发布者（publisher）和订阅者（subscriber）。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjia6kuf1ij30l20cmdha.jpg)
中介承担着转发MQTT 通信的服务器的作用。相对而言，发布者和订阅者则起着客户端的作用。发布者是负责发送消息的客户端，而订阅 者是负责接收消息的客户端。MQTT 交换的消息都附带“主题”地址，各个客户端把这个“主题”视为收信地址，对其执行传输消息的操作。 形象地比喻一下，中介就是接收邮件的邮箱。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjia7knkydj30lu0cydhh.jpg)
- MQTT通信的机制<br>
中介在等待各个客户端对其进行连接。订阅者连接中介，把自己想订阅的主题名称告诉中介。这就叫作订阅。 然后发布者连接中介，以主题为收信地址发送消息。这就是发布。发布者一发布主题，中介就会把消息传递给订阅了该主题的订阅者。
如上图所示，如果订阅者订阅了主题A，那么只有在发布者发布了主题A 的情况下，中介才会把消息传递给订阅者。订阅者和中介总是处于 连接状态，而发布者则只需在发布时建立连接，不过要在短期内数次发布时，就需要保持连接状态了。因为中介起着转发消息的作用，所以各 个客户端彼此之间没有必要知道对方的IP 地址等网络上的收信地址。又因为多个客户端可以订阅同一个主题，所以发布者和订阅者是一 对多的关系。在设备和服务器的通信中，设备相当于发布者，服务器则相当于订阅者。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjia8o7sxmj30m60ewjtu.jpg)
目前互联网中MQTT物联网平台多种多样,本次学习Easy IoT 如何使用MQTT订阅主题和发布消息。
### 6.3.4. 实现步骤
1. 打开DFRobot Easy IoT 物联网平台[http://iot.dfrobot.com.cn/]
2. 注册并登陆
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjiag6ilwsj31fl0u0gr3.jpg)
3. 进入工作间
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjiajdr121j31p70u07wh.jpg)
工作间说明
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjianeq321j31os0jydib.jpg)
1区域：用户密码区域，自动生成用户和密码，不能修改，mpython掌控板中的MQTT模块的用户和密码要和此处的用户和密码一致。<br>
2区域：主题区域，每一个主题代表不同类型的命令，当平台发布了该主题的命令，接收端会对应执行这个主题的程序。<br>
主题名称自动生成，无法修改，点击发送消息，进入主题，发送命令。<br>
3区域：添加新主题。<br>
4区域：重新生成用户名和密码，点击右侧眼睛显示用户名和密码。<br>
点击发送消息:<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjiarab6qoj30uk0e8ab0.jpg)
出现如下界面：<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjiasixialj31r40sx415.jpg)
4. 编写程序<br>
（1）连接WiFi
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjiax0yperj30qs04u0t7.jpg)
(2) MQTT模块搭建<br>
- 找到MQTT模块指令<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjib24ie56j30u00z6tfz.jpg)
- 配置MQTT信息，其中lot id（用户名）和lot pwd（密码）要工作间设置的用户名和密码一致。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjib5orcuij316o0cyjvy.jpg)
- 连接MQTT
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjib7ceot0j30ti04wjrg.jpg)
- 初始化主题显示的文本。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjib8v8xr1j30r004u0t5.jpg)
主题与工作间的主题对应。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjib9gg6lij30to0cyt9m.jpg)
- 设置主题的执行操作<br>
当主题接收到命令，执行对应的程序，本次程序其中一个主题接收“on”开灯并显示on，接收“off”关灯，并显示off，另一个主题为在掌控中画圆形，圆形的半径为输入的数值的大小，主题名称要与平台主题名称一致，程序如下:
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjibhauojlj30u00x1ahc.jpg)
- 掌控板一直等待主题消息，收到命令就执行对应程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjibjk4odij30kc06qt94.jpg)
(3) 运行刷入程序<br>
(4) 测试运行<br>
- 选择对应的主题，如图中的主题。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjic2qz2pyj31n20kijue.jpg)
点击发送消息，进入到发送消息界面。发送【on】
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjibyxzno0j31tg0mo41i.jpg)
按照程序的逻辑，实现的是所有RGB灯亮红色。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjic8bzaxyj31400u01ky.jpg)
当发送【off】到掌控板时，所有RGB等熄灭。<br>
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjid8ttn38j31400u0x6p.jpg)
- 选择另外一个主题，发送消息，该主题设置的程序逻辑是画圆形。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjicdjir20j31mi0nugoq.jpg)
输入整数23并发送。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjick30khxj31o20ec760.jpg)
掌控板中的显示，为一个半径是23的圆形。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjicm53pibj31410u0u0x.jpg)
输入数字56，则在掌控板中给出相应的提示。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjicndvfw4j31400u0x6p.jpg)
此外，可以在Easy IoT平台上查看发送的消息列表。
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjicoqnl95j31mc0eoabb.jpg)
### 6.3.5. 参考程序
![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gjicuor8yjj30tr1b812a.jpg)
### 6.3.6. 实现效果
见操作步骤。