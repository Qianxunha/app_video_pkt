windows_exe: windows安装包

macos_dmg: macOs安装包

app202536_101839.mp4: APP演示基本功能

cbct202536_102433.mp4: 牙齿cbct口腔全景图生成步骤颜色，三维建模

teeth: 

论文：《A fully automated method for 3D individual tooth identification and segmentation in dental CBCT》

论文链接：https://ieeexplore.ieee.org/abstract/document/9445658

CBCT数据来源：https://github.com/ErdanC/Tooth-and-alveolar-bone-segmentation-from-CBCT


论文流程：
1. 根据CBCT数据--->生成口腔全景图
2. 在口腔全景图中框选牙齿--->得到牙齿ROI数据。
3. 基于牙齿ROI数据使用nnunet模型训练。移植模型部署海思芯片；

口腔牙齿分割两种方案：
1. AI深度学习分割牙齿：通过pytorch框架，神经网络模型，从CBCT中提取牙齿，剔除牙龈。--->交互式标记使用分水岭算法分割28颗牙齿。

2. CPU分割牙齿：根据论文步骤1，2 提取到牙齿ROI，使用分水岭算法分割。

两种方案各有优缺点:

AI深度学习框架模型移植，需要考虑芯片AI框架是否支持，算子等,难度在于部署移植这块

CPU分割牙齿缺点，占用资源耗cpu，从医生使用角度，流程较多，步骤繁琐些。

APP基本功能：
1. 支持切换不同的主板ip, 切换视频画面
2. 支持拍照，录像，主机端按拍照录像按钮，客户端APP同步。
3. 支持图片编辑。
4. 支持视频回放，播放控制，指定播放位置，调节音量大小，设置静音状态。抓拍截图。
5. 支持流媒体协议，RTMP/RTSP/HTTP(APP中已屏蔽，没有放出。有接口设计）
5. 支持病例管理，登记患者信息，查询患者信息。打印报告，病例模板，设计报告。
6. 支持DICOM文件解析，CT/MR/X光等。(APP中已屏蔽，DICOM解析模块没有放出）
7. 支持DICOM文件对接医院PACS系统。
8. 支持服务器转发功能，实现视频流转发，用于医生教学，多人观看。


