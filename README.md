# ionic_cordova_update_platform_config
通过hook方式更改iOS的plist文件 和 android的AndroidManifest.xml


1.在ionic项目的根目录创建hooks\after_platform_add目录

2.下载update_platform_config.js到after_platform_add目录

3.在ionic项目的config.xml中配置需要修改的项，例如：
	<config-file parent="NSCameraUsageDescription" platform="ios" target="*-Info.plist">
          <string>需要用户同意</string>
        </config-file>
        <config-file parent="NSPhotoLibraryUsageDescription" platform="ios" target="*-Info.plist">
          <string>需要用户同意</string>
        </config-file>
        <config-file parent="NSLocationWhenInUseUsageDescription" platform="ios" target="*-Info.plist">
          <string>需要用户同意</string>
        </config-file>

4.执行命令：sudo ionic platform remove ios && sudo ionic platform add ios 

###说明###
该js脚本自动运行且会对config.xml进行解析，从而达到更新plist文件或AndroidManifest.xml文件。

