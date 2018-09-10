# stm32isp
参照https://github.com/wengkai/stm32isp.git  这个开源项目


使用这个工具时，要根据自己开发板的电路原理图来修改main.c里面的启动引脚配置：
bootp代表boot0引脚，reset代表重启引脚。
如果电路图中两个引脚为高电平接通，则这两个配置项配置为：
config.bootp = -RTS;
config.reset = -DTR;
如果两个引脚为低电平接通，这这两个配置项配置为：
config.bootp = RTS;
config.reset = DTR;



