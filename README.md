# Up Squared Pro ITX转接板

主页：https://up-board.org/up-squared-pro/

HW Spec：https://github.com/up-board/up-community/wiki/Hardware_Specification_UPS_Pro

Pinout：https://github.com/up-board/up-community/wiki/Pinout_UPSPro

本项目为将Up Squared Pro转接到ITX规格的PCB工程

## PCB配置

- 固定UPSP的孔位
- ATX-24插座
- USB供电口 x5
- USB常电供电口 x3
- 12V 5.5x2.1插座 x3
- UPSP 12V 供电焊盘
- ATX电源供电开关
- UPSP开关

## 电源输出能力

- `+12v`:15A
- `+5v`:18A
- `+3.3v`:22A
- `+5vSB`:2A
- `-5v`:0.5A
- `-12v`:0.5A

## 笔记

### ATX-24

`PS_ON`短接到`GND`时，电源开始工作。否则，只有`5VSB`口输出。

`PWR_OK`是电源输出稳定的信号。当电源输出达到稳定状态后，会输出`5V`。一般在电源开始工作100ms-500ms后这个信号将会给出。

这里的实践将直接采用一个船型开关接到`PS_ON`的方式来控制电源。