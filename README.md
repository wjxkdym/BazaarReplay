# Bazaar Replay 1.0.0

大巴扎操作录像插件。自动录制游戏内操作，在游戏中回放，支持 **1×／2×／4×快进、按天／小时定位、录像片段截取和结束阵容查看**。

[GitHub 正式版下载](https://github.com/wjxkdym/BazaarReplay/releases/tag/v1.0.0)

[百度网盘正式版下载](https://pan.baidu.com/s/1rOw1MlgOkHMSGVTXHrNewA?pwd=7pu1) · 提取码：`7pu1`（永久有效）

## 安装

适用 Windows Steam 版 The Bazaar **Build 26592248（1.0.13175）**，需要已安装 **BepInEx 5**。支持在该客户端播放通过兼容检查的 Build 25914521 旧录像。

1. 下载 `BazaarReplay-1.0.0-windows.zip`，完整解压。
2. 正常关闭游戏，在解压目录运行 `install.ps1`。
3. 正常启动游戏，按 **F7** 打开录像助手。

自定义游戏路径时，在 PowerShell 中运行：

```powershell
.\install.ps1 -GamePath 'G:\SteamLibrary\steamapps\common\The Bazaar'
```

安装器会备份已有插件，保留录像和设置。备份位于游戏目录的 `BazaarReplay\Backups`。

## 使用

- **自动录制**：保持“自动录制”开启，正常游戏即可；返回大厅时保存，也可点击“停止并保存”。
- **播放与快进**：在大厅打开录像库，选择录像并播放。点击“快进”切换 1×、2×、4×。
- **定位**：拖动事件进度条，或输入天数、小时跳转；也可使用按天／小时目录和战斗目录。
- **战斗复盘**：开启“每场战斗后暂停”，可以使用游戏内原生重放与战报。
- **截取录像**：选择完整录像，在“截取录像”页填写起止天数、小时，另存为独立录像。
- **结束阵容**：进入录像库默认展示末尾装备与技能；鼠标悬停查看卡牌效果，左侧可播放、收藏和删除录像。

录像保存在游戏目录的 `BazaarReplay\Recordings`。删除会移入该目录的 `.trash`，可恢复。

## 恢复与卸载

关闭游戏后运行 `restore.ps1 -BackupPath '备份目录'` 恢复备份，或运行 `uninstall.ps1` 卸载插件；录像和设置保留。

`source.zip` 提供源码，`SHA256-1.0.0.txt` 用于核验下载。开发需要 .NET SDK 10 及本机游戏程序集，运行插件无需安装 SDK。
