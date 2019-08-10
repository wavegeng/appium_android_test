1、如果该设备已经添加处理过，则忽略，否则按照以下步骤添加新测试设备：
    a、config.yaml里首先按照格式添加设备信息，并添加相对应的测试user信息，注意serverport、bootstrappoot不能跟其它设备重复，server信息代表该测试设备在哪个机器上跑
    b、需要在prepro文件下，创建该设备的安装类继承自BaseDevicePreProcess，然后根据相应情况分别处理安装、权限等预处理流程
    c、被添加的设备，需要手动安装unlock.apk/ime.apk/setting.apk，apk文件在apk目录下
    d、被添加设备，需要在相册里添加autotest相册集，里边添加测试用的图片9张,用来测试发1张图和9张图，图片在res目录下
    e、被添加设备最好去除锁屏、密码


2、做为server的机器首先adb连接上测试机器，然后运行Server/run_server.py启动server


3、再开始进行测试,运行run_test.py












