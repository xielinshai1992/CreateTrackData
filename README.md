# CreateTrackData

#### 介绍
创建飞行器航迹软件。航迹数据包括本机航迹、目标机ADS-B、TCAS航迹，支持网络发送。

软件采用PyQt5-GUI框架和Python3.6开发。

软件支持ADS-B的四种应用处理：

基本空中交通态势感知（Basic Airborne Situation Awareness，简称：AIRB）

目视间隔进近（Visual Separation on Approach，简称：VSA）

场面态势感知（Surface Situation Awareness，简称：SURF）

高度层变更程序（In-Trail Procedure，简称：ITP）

#### 软件架构
1.主界面UI adsb_mainForm.py

2.主函数 create_airportdata_form.py

3.本机航迹、ADS-B航迹、TCAS航迹数据接口 c_api.py

4.data_interface_pro.dll 基于ARINC735B协议数据打包数据

5.辅助工具模块 geography_analysis.py

6.网页加载 map_a.html、map_surf.html、js、css文件夹


#### 使用说明

1.安装pyqt5三方库后，python运行create_airportdata_form.py

2.导入.yaml的本机数据和目标机数据

3.点击“开始”按钮，开始仿真航迹数据并向下游UDP传输

