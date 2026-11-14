# LeftTopCast TV

安卓电视左上角可调区域 DLNA / UPnP 视频投屏接收器，适合电视右侧损坏的情况。

- **目标**：PiliPlus / 哔哩哔哩等 DLNA 发送端，在电视左上角指定区域内播放，黑色遮盖其余区域。
- **兼容性**：Android TV / Android 5.0+（API 21+），具体由电视硬件解码器决定。
- **范围**：只能调整 **本应用内** 视频与播放控件，不改变系统桌面或 HDMI 输入画面。
- **操作**：遥控器上/下选择项目，左/右调整宽度/高度，每次 5%；默认宽度 75%、高度 75%。
- **网络**：手机和电视在同一局域网，电视打开接收器，手机选择 `LeftTopCast TV` 投屏。
- **包名**：`io.lefttopcast.tv`，不会覆盖 PiliPlus 或原版 LeanCast。

## 编译 APK

在 **Actions → Build LeftTopCast TV APK → Run workflow** 触发。成功后，会生成 `LeftTopCast-TV-DLNA-v1.apk` 文件（Actions Artifact）；也尝试在 [Releases](../../releases) 发布直接可下载的 APK。

> 第一个版本是测试版，尚未在你的具体电视上验证。Debug 签名可能使后续不同构建之间无法覆盖安装；推荐先备份你的显示设置，再进行更新。

## 上游和许可证

基于 [LeanCast](https://github.com/addozhang/leancast) (Apache-2.0)。本仓库保留自定义设置界面 `lefttopcast/MainActivity.kt` 和修改脚本 `lefttopcast/apply.py`。构建时拉取 LeanCast 源码并打补丁，不修改或依赖原有 PiliPlus 仓库。

仅供用于自己的设备进行测试。