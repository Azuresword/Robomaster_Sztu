# Robomaster_Sztu
# Snail 电机驱动操作说明

​																							--2021 Programmer Dylan

1.该电机使用pwm控制

2.电机的pwm控制初始化官方设置的DJI Assistance 2使用存在一定问题，不推荐使用

3.电机的基础配置频率500Mhz,CCR-初始值 2000，AAR-19999，ABP2 168Mhz，PSC 167

4.电机在cubemx的设置使用的pwm驱动，gpio引脚上拉，速率high/very high 舵机引脚1-4引脚在PE9，PE11，PE14，PE13，挂载在TIM1上

5.对电机的控制直接在程序中进行ccr值得设定，1001为默认初始化值，1400为推荐3m距离射速，2200为pwm进程最大值极限射速，1250以上的ccr值有效其他pwm值不可控

6.对于反转电机的控制设定，推荐直接改线，把三相电机的红蓝灰三条线中的任意两线交换位置即可
