# 多功能传送插件 (TeleportPlugin) for DanhengServer

[![Author](https://img.shields.io/badge/Author-Aerhuo-blue.svg)](https://github.com/Aerhuo)

这是一个为 DanhengServer 开源项目编写的多功能传送插件。

## ✨ 功能

*   **/getpos**: 获取并显示你当前的精确坐标。
*   **/tp `<x> <y> <z>`**: 传送到指定的绝对坐标点。
*   **/offsettp `<子命令>`**: 执行强大的相对位移传送，非常适合进行精细的建筑定位和复制操作。

## 🔧 安装

1.  前往 [Releases](https://github.com/YourUsername/TeleportPlugin/releases) 页面下载最新的 `TeleportPlugin.dll` 文件。
2.  将下载的 `TeleportPlugin.dll` 文件放入您 DanhengServer 服务器的 `Plugins` 文件夹中。
3.  重启服务器。当您在后台日志中看到 `[TeleportExtended] [INFO] 多功能传送插件已加载！...` 的消息时，说明安装成功。

## 📖 用法

请参阅详细的 [**用户手册 (USER_MANUAL_CN.md)**](USER_MANUAL_CN.md) 来了解所有指令的详细用法和示例。

## 🚀 编译

本项目使用 .NET 8 构建。

1.  克隆本仓库。
2.  在 `libs` 文件夹中，放入所有必需的 `Danheng*.dll` 依赖文件。
3.  在项目根目录运行 `dotnet build`。
4.  生成的DLL文件位于 `bin/Debug/net8.0/TeleportPlugin.dll`。
