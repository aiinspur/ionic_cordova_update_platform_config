
####################################项目环境配置####################################

在当前目录执行如下命令：
1. 安装node环境： npm install -d

2. 安装平台：ionic platform add android

3. 安装ionic2自定义插件：
	下载编译好的ionic-native 并替换本地的项目中的node_modules/ionic-native/dist/
	dist下载地址：https://github.com/shihujiang/ionic-native-dist.git
	
4. 安装人脸识别插件(在config.xml中配置自动安装人脸识别插件会提示错误，所以暂时通过命令单独安装改插件)
	ionic plugin add https://github.com/shihujiang/cordova-plugin-pingan-face

问题及处理方式：
	在安装人脸识别插件中可能会报错，提示xxx/xxx 文件已存在。遇到这个错误，直接删除该文件，重新之行人脸识别插件安装命令。



