# jenkinsPackApk
CentOS8 jenkins 安卓自动打包测试

1、jenkins搭建、启动服务

2、默认用户jenkins配置成root，避免gradle打包权限限制问题

3、下载安装android sdk，配置到环境变量/etc/profile，下载对应项目需要的SDK Platforms 和 SDK Tools (本git项目：platforms:android-30和build-tools:28.0.3）

4、登录jenkins，配置全局环境：

    Plugin Manager下载 git、gradle、jdk插件后 Global Tool Configuration会显示对应配置
    
    Global Tool Configuration 里配置git、gradle、jdk路径
    
5、jenkins创建新项目，配置环境：

git项目地址和账号配置:

<img width="712" alt="QQ20211202-174345@2x" src="https://user-images.githubusercontent.com/15667337/144397685-6eeb18dc-6493-4313-90e4-9e818c45dba2.png">

分支:

<img width="689" alt="QQ20211202-174406@2x" src="https://user-images.githubusercontent.com/15667337/144397845-a43062b3-42f6-40ec-8f84-d22a67cf0b8e.png">

打包并复制到指定文件夹：

<img width="729" alt="QQ20211202-174423@2x" src="https://user-images.githubusercontent.com/15667337/144397900-0227b5a7-741e-48f9-81a2-ca97d9568caa.png">

6.build now 运行， 从git拉取编译打包出apk，大功告成

<img width="641" alt="QQ20211202-182215@2x" src="https://user-images.githubusercontent.com/15667337/144403622-5eea151b-3af8-4365-b749-d0b4f6eff08b.png">

