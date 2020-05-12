# IOT-Terminal
An IOT Terminal based on M5GO(chip: ESP32). The communication system is powered by QQbot.	https://github.com/luzy99/IOT-Terminal.git

> 本项目采用的设备是M5GO（esp32芯片），采用MQTT方式与服务器通信。借助[Mirai QQ机器人框架](https://github.com/mamoe/mirai)，实现QQ远程操控物联网设备。

## 项目使用说明

1. **M5STACK部分**

   `myapp`	该部分采用C语言编写，借助Arduino及第三方库编译。

   > **下列依赖库通过Arduino库管理工具安装**
   >
   > MQTT通信库：EspMQTTClient
   >
   > HTTP库：HTTPClient
   >
   > LED灯条控制：FastLED
   >
   > 红外解码库：IRremoteESP8266
   >
   > JSON解析库：Arduino_JSON

2. **服务器部分**

   > 系统版本：CentOS 7
   >
   > MQTT Broker：EMQX

   :warning:下列代码为`Mirai QQ 机器人框架`的插件，须依赖框架使用。详细信息请点[这里](https://github.com/mamoe/mirai)。

   `MqttTrans`为利用`Mirai`提供的Java API 编写的MQTT转发插件，同时包括`JFreeChart`图表绘制模块，及JDBC数据库连接访问模块。