## 安裝

可以看這個網站

[Installation Guide · homuler/MediaPipeUnityPlugin Wiki (github.com)](https://github.com/homuler/MediaPipeUnityPlugin/wiki/Installation-Guide)

下面各個平台的安裝方法

我們用的是Windows 10 的方式

**網站上的內容**

![pluginWebsite](https://github.com/z22756392z/MediaPipe/blob/main/image/pluginWebsite.png)

他需要幾個安裝幾個軟體和設定才能正常使用
* python 3.9.0 , numpy
* MSYS2 ,設定環境變數
* Bazel 5.0.0[Releases · bazelbuild/bazel (github.com)](https://github.com/bazelbuild/bazel/releases?q=5.0.0&expanded=true), 設定環境變數
* Nuget 5.10.0[NuGet Gallery | Downloads](https://www.nuget.org/downloads?msclkid=3608a8abd02f11ec9f846243bd98975e), 設定環境變數
* WinSDK (windows 10)
* Bazel連結 visual stdio 和 winsdk

## 必要的安裝

* python版本3.9.0以上 下載numpy(到cmd 打 pip install numpy)
* MSYS2 安裝好後要設定環境變數 
* Bazel [Releases · bazelbuild/bazel (github.com)](https://github.com/bazelbuild/bazel/releases?q=5.0.0&expanded=true) 安裝 5.0.0的版本 同樣設定環境變數 看有沒有安裝好可以在cmd打``bazel --version``

  ![bazel](https://github.com/z22756392z/MediaPipe/blob/main/image/bazel.png)

* WinSDK 到visual stdio 點選要使用visual stdio的版本 按修改 可以點選隨便一個windows 10 SDK 只要有安裝就好 要記得版本之後會用到(這裡是: 10.0.18362.0)

![winsdk](https://github.com/z22756392z/MediaPipe/blob/main/image/winsdk.png)

* nuget[NuGet Gallery | Downloads](https://www.nuget.org/downloads?msclkid=3608a8abd02f11ec9f846243bd98975e) 下載 5.10.0的版本 同設定環境變數 (cmd打``nuget``同樣可以看有沒有成功)

* 連結 visual stdio 和 winsdk
```
  set BAZEL_VS=C:\Program Files (x86)\Microsoft Visual Studio\2019\Community
  set BAZEL_VC=C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC

  //在C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC資料夾底下檔案上的名稱(版本)

  set BAZEL_VC_FULL_VERSION=14.28.29333

  //剛剛 用visutal stdio installer 下載的winsdk版本

  set BAZEL_WINSDK_FULL_VERSION=10.0.18362.0
```

* 下載插件  `git clone https://github.com/homuler/MediaPipeUnityPlugin.git`

* 開cmd cd到clone的資料夾 跑 `python build.py build --desktop cpu --opencv=cmake -v `

## 結果
![https://github.com/z22756392z/MediaPipe/blob/main/image/result.png]
