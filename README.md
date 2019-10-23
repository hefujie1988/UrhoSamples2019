# UrhoSharp 2019 演示

UrhoSharp 是个优秀的开源游戏引擎，但官方的演示如今要改很多东西才能运行，为了让大家玩的开心，本喵翻新了演示里最重要的部分。

## 运行指南

* 安装 [Visual Studio 2019](https://visualstudio.microsoft.com/vs/)。

### 桌面

* 通过 Installer 安装默认工作负载：.NET Core 跨平台开发。
* 在文件夹 SamplyGame\SamplyGame.Desktop 下执行 dotnet run 玩游戏。
* 在文件夹 FeatureSamples\Urho.Samples.Desktop 下执行 dotnet run 运行功能展示，输入数字如 19；在 Windows 下，在文件夹 FeatureSamples\Urho.Samples.WPF 下执行 dotnet run 运行全部功能展示。

### 移动

* 通过 Installer 安装默认工作负载：使用 .NET 的移动开发、通用 Windows 平台开发。
* 打开 SamplyGame\SamplyGame.sln，编译 SamplyGame.Droid，连接安卓设备后部署、运行。
* 打开 FeatureSamples\FeatureSamples.sln，编译 FeatureSamples.Droid，同上。

#### Urho3D 编辑器

* 下载 Urho3D 编辑器（链接见下方），运行 bin\Editor.bat，File - Open Scene (Ctrl + O)，打开示例 /UrhoAssetImporter/SampleData/MainScene.xml。

## 链接

UrhoSharp (Xamarin) 官网：https://docs.microsoft.com/zh-cn/xamarin/graphics-games/urhosharp/

Urho3D 官网：https://urho3d.github.io/

Urho3D 编辑器：https://sourceforge.net/projects/urho3d/files/Urho3D/

UrhoSharp 源码：https://github.com/xamarin/urho

Urho3D 源码：https://github.com/urho3d/Urho3D

# UrhoSharp samples

This directory contains various samples for the [UrhoSharp](http://developer.xamarin.com/guides/cross-platform/urho/) 
engine and they can be compiled for Android or iOS, or can be executed on Windows
and Mac with the published NuGet package.

# Samples

Some of the samples here include:

* FormsSamples
* FeatureSamples
* SamplyGame
* HoloLens, ARKit, ARCore
* Mixed samples

## ARKit, ARCore and HoloLens

These directories contain samples for running UrhoSharp on HoloLens, ARKit and ARCore.  
Also there is a mixed sample that shares a scene between iOS, Android and HoloLens (see Mixed/AR)

![Screenshot](ARKit/Mutant.gif)
![Screenshot](ARKit/Crowd.gif)

## FormsSamples

The 'FormsSamples' solution demonstrates how UrhoSharp can be used in Xamarin.Forms 
applications as a View element.

![Screenshot](FormsSample/Screenshots/Android.gif) ![Screenshot](FormsSample/Screenshots/Ios.gif)

## FeatureSamples

The toplevel `FeatureSamples` solution showcases 40 independent UrhoSharp
features, each one showcasing a particular element of the framework and runs
on all supported platforms. 

![Physics2D](https://habrastorage.org/files/d77/060/698/d770606980874fb6a15484d04bea6dd6.gif)
![Water](https://habrastorage.org/files/e3e/8f1/80d/e3e8f180d8b54f0989d9448c98eacd5b.png)

## SamplyGame

The `SamplyGame` directory contains a more complete game, it is a sample
inspired by the gameplay and artwork of ShootySkies and shows a more 
complete game in action, showing how to load assets, write game code and
structure a game.   It is our first game build with this, so be kind.

![Screenshot](SamplyGame/Screenshots/Video.gif)

## Structure

All solutions are structured to have their cross platform code written
in the `Core` directory, where we build a portable class library.   While
we have taken the approach of using Portable Class Libraries, you can 
also used Shared Projects.

The structure of each solution is this:

* `Assets`: Contains the shared assets that are used for the various
  samples.

* `Core`: Contains the various samples, one for each feature that is
  being showcased and it happens to be a Portable Class Library
  project, so it can be reused as-is across all supported platforms.

* `iOS`: Contains the iOS launcher.

* `Android`: Contains the Android launcher.

* `Mac`: Contains the Mac launcher (but works on Windows too).

* `WPF`: Contains the Windows launcher based on WPF.

* `WinForms`: Contains the Windows launcher based on WinForms.

## UrhoAssetImporter - a simple UrhoSharp assets viewer + AssetImporter

Supported formats:
- .obj, .dae, .fbx, .blend, .3ds, .lwo, [etc](http://assimp.sourceforge.net/main_features_formats.html). 
- Urho3D Materials, Particles, Prefabs, Models, etc

Supported platforms:
- Windows (WPF)

![Screenshot](UrhoAssetImporter/Screenshots/Screenshot2.png)
  
![Screenshot](UrhoAssetImporter/Screenshots/wpf.gif)

# To build the samples

* Windows: Use [Visual Studio 2019](https://www.visualstudio.com/).
