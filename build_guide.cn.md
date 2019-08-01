# Planck Through Hole Kit 制作指南

![Planck THK](https://i.imgur.com/O8qh1Vv.jpg)

本文档简述[Planck Through Hole Kit](https://github.com/olkb/planck_thk
) 制作过程。

## 概要

制作过程如下

### 準備
- 准备零件

### 硬件流程
1. USBMini 接口
1. 二极管
1. LED
1. 电阻
1. 晶振
1. 电容
1. 稳压器
1. 扬声器
1. DIP开关
1. 复位开关
1. MCU热插拔基座
1. PH接口
1. ISP/JTAG接头
1. 旋钮

### ISP 刷机
1. 制作ISP 下载器
1. ISP刷固件

## 準備

### 准备零件

![Parts](https://i.imgur.com/90f6Xw5.jpg)

### PCB1个

![PCB](https://i.imgur.com/eLqk6XM.jpg)

| 名称 | 数量 |
| ---- | ---- |
| PCB | 1 |

### 袋A

![MCU](https://i.imgur.com/GWmpFJM.jpg)

| 名称 | 基板上対応位置 | 数量 |
| ---- | ---- | ---- |
| ATmega32A | MICROCONTROLLER | 1 |

### 袋C

![Rotary Encoders](https://i.imgur.com/F3mr80b.jpg)

| 名称 | 基板上対応位置 | 数量 |
| ---- | ---- | ---- |
| 旋钮 | ENCODERS | 2 |

### 袋D

![Sockets](https://i.imgur.com/c06ivUG.jpg)

| 名称 | 基板上対応位置 | 数量 |
| ---- | ---- | ---- |
| MCU热插拔座 40脚 | MICROCONTROLLER | 1 |
| DIP开关 | DIP SWITCH | 1 |
| 扬声器 | SPEAKER | 1 |
| USB Mini 口 | USB PORT | 1 |
| PH接口 | ALT USB PORT | 1 |
| JTAG针头 2×5 | JTAG HEADER | 1 |
| ISP针头 2×3 | ISP HEADER | 1 |
| 复位开关 | RESET | 1 |

### 袋E

![Diodes](https://i.imgur.com/icw75zz.jpg)

| 名称 | 基板上対応位置 | 数量 |
| ---- | ---- | ---- |
| 二极管 | D1〜D48 | 48 |

### 袋F

![Parts](https://i.imgur.com/jagOLm9.jpg)

| 名称 | 基板上対応位置 | 数量 | 備考 |
| ---- | ---- | ---- | ---- |
| 金属膜电阻 68Ω | R1, R2, R4, R5 | 4 | 青灰黒金 |
| 金属膜电阻 1.5Ω | R3 | 1 | 茶緑赤金 |
| 稳压器 | POWER REGULATOR | 1 | |
| 陶瓷电容 20pF | C1, C2 | 2 | |
| 独石电容 0.1uF | C3 | 1 | |
| 独石电容 4.7uF | C4 | 1 | |
| 晶振 | Y1 | 1 | |
| 赤色LED | PWR | 1 | |
| 緑色LED | ACT | 1 | |


## 硬件流程

在电路板的正面（上方）依次焊接下述原件

### 1. USB接口

USB Mini接口在 `USB PORT` 的位置焊接

![USB1](https://i.imgur.com/hHKRVL0.jpg)

如下述图片所示， 因为焊点之间间距较小， 请注意不要短路

![USB2](https://i.imgur.com/SRa4vzi.jpg)

### 2. 二极管

从位置 `D1` 到 `D48` 焊接48个二极管。二极管有极性， 请像照片上那样进行焊接， 黑头对准板上有标记的一端。

![Diode1](https://i.imgur.com/UNsZqq2.jpg)

因为Planck THK是完成后元件暴露在外面的构造， 需要尽可能焊接的漂亮一些。如图所示， 用面包板的一侧来弯折二极管针脚是非常合适的。


![Diode2](https://i.imgur.com/AjNaMj9.jpg)

### 3. LED

红色和绿色的LED对应板上的`PWR` 和 `ACT` 位置（也可以根据自己的喜好换成其它的颜色）。

![LED1](https://i.imgur.com/IuVnN5Q.jpg)

短脚对应负极。

![LED2](https://i.imgur.com/xHMAkXH.jpg)

### 4. 电阻

4枚68Ω电阻(青灰黒金)对应`R1`、`R2`、`R4`、`R5`标记的位置

![Resistor1](https://i.imgur.com/kc8yU0T.jpg)

![Resistor2](https://i.imgur.com/JHdIeX0.jpg)

然后，1枚1.5kΩ电阻(茶緑赤金)对应`R3`标记的位置

![Resistor3](https://i.imgur.com/1d0beHM.jpg)

### 5. 晶振

晶振安装到 `Y1` 标记的位置

![Crystal1](https://i.imgur.com/90QoaXM.jpg)

### 6. 电容

将2枚20pF陶瓷电容焊接到晶振两侧的 `C1` 和 `C2` 标记的位置。

![Capacitors1](https://i.imgur.com/Vzg3fYJ.jpg)

![Capacitors2](https://i.imgur.com/U2QsIvv.jpg)

然后0.1uF的独石电容安装到 `C3` 的位置、4.7uF的独石电容装到 `C4` 的位置。元件上标记104的是0.1uF的，而标记475的是4.7uF的。

![Capacitors3](https://i.imgur.com/LNMcGuI.jpg)

![Capacitors4](https://i.imgur.com/cyJolJi.jpg)

`C3` 和 `C4` 位置焊接完成后如图所示。

![Capacitors5](https://i.imgur.com/Wc4JNTq.jpg)

### 7. 稳压器

稳压器焊接到 `POWER REGULATOR` 标记的位置。

![Regulator1](https://i.imgur.com/w5i8tzi.jpg)

进行焊接前先用钳子弯曲针脚90度，使得插入后稳压器正好贴在PCB上。

![Regulator2](https://i.imgur.com/d1XixLC.jpg)

### 8. 扬声器

扬声器焊接在 `SPEAKER` 标记的位置。

![Speaker](https://i.imgur.com/EsVRQg8.jpg)

扬声器没有极性。

### 9. DIP开关

DIP开关 `DIP SWITCH` 的位置。注意方向，越往上数字越小。

![DIPSwitch](https://i.imgur.com/I2iqany.jpg)

### 10. 复位开关

复位开关焊接在 `RESET` 的地方。

![ResetSwitch](https://i.imgur.com/PU8yE19.jpg)

### 11. MCU热插拔基座

MCU热插拔基座在 `MICROCONTROLLER` 的位置进行焊接。注意方向，有槽口的一端和板上的标记对其，如图所示。

![Socket1](https://i.imgur.com/qskeBOt.jpg)

下图是焊好的状态。

![Socket2](https://i.imgur.com/79gqS1N.jpg)

### 12. PH接口

PH接口焊接在 `ALT USB PORT` 的位置。

![PH1](https://i.imgur.com/wPiVSy7.jpg)

※不是必须的，可以跳过。

### 13. JTAG报头和ISP报头

2×5的针头安装到 `JTAG HEADER` 的位置、2×3的针头安装到`ISP HEADER` 的位置。

![Headers](https://i.imgur.com/fXCDt0Z.jpg)

### 14. 旋钮

两个旋钮焊接到 `ENCODER 1` 和 `ENCODER 2` 标记的地方。

![Encoders](https://i.imgur.com/tVvt2F4.jpg)

## ISP 刷机

本节刷机教程参考 [qmk_firmware文档](https://beta.docs.qmk.fm/for-makers-and-modders/isp_flashing_guide)。接下来考虑使用, Ubuntu 16.04，avrdude 6.2，Pro Micro 的刷机流程 (使用其它操作系统，如Win10，OSX，以及其它ISP programmer 如 Teensy 2.0 和 USBtiny等是可行的，但需要调整下述命令里的具体指令)。

### 制作ISP下载器

使用一枚 Pro Micro。 首先将这个[hex文件](https://github.com/qmk/qmk_firmware/blob/master/util/pro_micro_ISP_B6_10.hex) 刷到Pro Micro上。可以分为以下几步:

1. 下载`pro_micro_ISP_B6_10.hex`文件
1. 将Pro Micro通过USB线链接到电脑。短接Pro Micro上的RESET和GND，使Pro Micro进入bootloader
1. 运行命令, ```ls -l \dev\tty* ``` 获取Pro Micro对应的端口，一般会是```\dev\ttyACM0```或类似的端口号
1. 运行命令 ```avrdude -p m32U4 -P <端口号> -c avr109 -U flash:w:pro_micro_ISP_B6_10.hex```

在windows下用avrdude刷机，可以参考[这篇文章](http://electronicsdesign.nl/wp/promicro_avrdude/)。
 
### ISP 刷固件
 
 首先将MCU插入插槽中，注意方向，有缺口的一端和板上标记的一端一致。
 
然后按照[qmk_firmware文档](https://beta.docs.qmk.fm/for-makers-and-modders/isp_flashing_guide)里的方式跳线链接Pro Micro和PCB的ISP报头。其中板上的ISP报头的六个口的编码如下表所示：

| RESET | SCK | MISO |
| ---- | ---- | ---- |
| GND | MOSI | VCC |

![ISP header](https://i.ibb.co/8rMKh9D/Screenshot-from-2019-08-02-01-10-30.png)

链接的方式如下
> Pro Micro 10 (B6)  <-> Keyboard RESET
> Pro Micro 15 (B1)  <-> Keyboard B1 (SCLK)
> Pro Micro 16 (B2)  <-> Keyboard B2 (MOSI)
> Pro Micro 14 (B3)  <-> Keyboard B3 (MISO)
> Pro Micro VCC      <-> Keyboard VCC
> Pro Micro GND      <-> Keyboard GND

链接完成后，将Pro Micro用USB线链接至电脑，PCB则只通过ISP报头链接Pro Micro，PCB本身不直接连电脑。进行如下操作：

- 设置Fuse位， 运行命令 ```avrdude -c avrisp -P <端口号> -p atmega32 -U lfuse:w:0xcf:m -U hfuse:w:0x90:m```
- 
