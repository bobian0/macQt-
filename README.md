# macQt-
mac os运行Qt项目只能后台输出，不显示ui窗口

**运行后提示内容:**

    Project WARNING: Qt has only been tested with version 10.15 of the platform SDK, you're using 12.3.
    Project WARNING: This is an unsupported configuration. You may experience build issues, and by using
    Project WARNING: the 12.3 SDK you are opting in to new features that Qt has not been prepared for.
    Project WARNING: Please downgrade the SDK you use to build your app to version 10.15, or configure
    Project WARNING: with CONFIG+=sdk_no_version_check when running qmake to silence this warning.
**解决方法：**

在pro文件内加入这两行即可

    CONFIG += skd_on_version_check
    QMAKE_MACOSX_DEPLOYMENT_TARGET = 12.3
      
![截屏2022-08-14 下午3 59 54](https://user-images.githubusercontent.com/70415754/184527901-1959b503-b6b9-41b4-9f8f-a8517249debb.png)
